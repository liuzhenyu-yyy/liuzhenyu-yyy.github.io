---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: post_20201207
title: "Construct pipeline for high throughput SCAN-seq2."

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
author: Zhenyu Liu
# multiple category is not supported
category: Work
# multiple tag entries are possible
tags: [Bioinformatics, Project]
# thumbnail image for post
img: ":post_20201214/cover.jpg"
# disable comments on this page
comments_disable: true

# publish date
date: 2020-12-14 08:11:06 +0900

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-02-10 08:11:06 +0900
# check the meta_common_description in _data/owner/[language].yml
#meta_description: ""

# optional
# if you enabled image_viewer_posts you don't need to enable this. This is only if image_viewer_posts = false
#image_viewer_on: true
# if you enabled image_lazy_loader_posts you don't need to enable this. This is only if image_lazy_loader_posts = false
#image_lazy_loader_on: true
# exclude from on site search
#on_site_search_exclude: true
# exclude from search engines
#search_engine_exclude: true
# to disable this page, simply set published: false or delete this file
#published: false
---

<!-- outline-start -->
Some records on constructing the bioinformatic pipelines for SCAN-seq2 data processing.

<!-- outline-end -->

---

# Background

SCAN-Seq is a new scRNA-Seq technology developed by our lab, which utilizes third generation sequencing (TGS, also know as single molecule real-time sequencing) methods to detect full length mRNAs in single cell. The original paper should be published soon.

Although SCAN-Seq provide relatively high through put (96 cell per sample) and good quality results, we still sought to further optimize this TGS-based scRNA-Seq technology. Our new protocol, which has not been named yet, showed a significant improvement in both throughput and accuracy. 

However, due to the higher error rate of TGS and more complicated library construction protocol,  processing these scRNA-Seq data requires a very different bioinformatics pipeline. After trying several different methods, I finally found a satisfactory pipeline to generate UMI count matrix from multiplexed Nanopore fastq data. After confirming the reliability of this method, Dr. Tang encouraged me to build a standard pipeline for convenience of the whole lab. It took me several days to organize my initial scripts into a  standard pipeline, which should be easy to read and use. Now I believe that every member in the lab could utilize this pipeline with a single line of command.

When I first moved to Tang lab, I was very impressed by the standard pipelines constructed by seniors in the lab. I learned a lot while reading the scRNA-Seq pipeline written by Dr. Ji Dong and scMALBAC pipeline written by Dr. Shuhui Bian. It's really lucky to have these pre-built pipelines because you could start analysis immediately after receiving the data. They are also excellent materials to learn basic methods for genomic data analysis. It was at that time that I suddenly have a strong wish to generate a new pipeline for the lab. I believe this could really provide convenience to all members in the lab. Now I might be able to say that I've realized this little goal. 

To help develop high throughput version of SCAN-Seq was the very first project I participate in at Tang Lab. It really means something special to me. Thanks to the great effort of Yuhan and Zhang Yu, we developed satisfactory pipelines for HTP SCAN-Seq, both experimental and computational. And I think it really worthwhile that I should record these experiences behind this pipeline, including all the trails and errors. 

# Experimental Improvements

Pre-existing full length transcriptome technologies all have similar shortcuts:

- relatively low throughput;
- rely heavily on simultaneous Illumina NGS sequencing for demultiplexing and quantification;
- no unique molecular identifier (UMI) to remove PCR duplications.

Our motivation is to develop a new experimental procedure that could overcome or bypass the limitations listed above. Yuhan and Zhang Yu did great works exploring the proper conditions of each experimental step. Finally, we did get very high-quality full length transcriptome data at single cell resolution. Details of the experimental protocol are not published yet and thus omitted in this blog.

# Computational Pipelines

Computational pipeline of TGS-based scRNA-Seq are quite different from that of NGS-based. Main problems came from the relative high error rated of Nanopore Sequencing. The identification of anchor sequence, barcode sequence, UMI sequence and poly-A tail all suffered greatly from the sequencing err, and brand new computational methods are required to handle these sequences properly. We tested several combinations of different computational tools and finally adopted a pipeline that we believe to have the best performance. Here I will briefly record some trails and errors we have made and describe our recommended way of processing Nanopore-based multiplexed scRNA-Seq data.

## Step 1 Demultiplexing

Demultiplexing refers to the process of classifying reads based on which cell they come from.  Actually demultiplexing the fastq data before processing is not necessary nor recommended for NGS-based method, since this will require processing each cell independently and thus wasting lot of time and computational resources. The standard scRNA-Seq pipeline of Tang Lab, which is constructed by Ji Dong and further modified by Jiansen, processes reads from all cells together and did not split barcode information until generating the output UMI count matrix. This method is both accurate and effective, however, not very applicable to our Nanopore-based high throughput method because:

1. barcode sequences are added to both 5' and 3' of cDNA to reach higher multiplexing level;
2. location of barcodes are not always fixed due to the nature of Nanopore Sequencing;
3. identification of barcode is not accurate due to the high error rate of Nanopore sequencing  

Limited by these features above, a independent demultplexing step before further processing is required.

We demultiplex the fastq data using [Nanoplexer](https://github.com/hanyue36/nanoplexer), which was developed specifically for demultiplexing Nanopore barcode sequence data. Since our reads are double-barcoded, we adopted a two-step demultiplexing procedure:

``` shell
# for 5' barcode
nanoplexer -b Barcode${bc}.fastq\
	 -p 01.demultiplex\
	 -t $threads\
	 $raw_fastq
# for 3' barcode
nanoplexer -b ../Barcode.3plus.fa\
         -p Barcode$bc\
         -t $threads\
         Barcode${bc}.fastq
```

This would generated a single fastq data for each cell and could be used for downstream analysis. Another important thing to notice is that we use 24 bp barcode sequence, however, due to the high error rate of Nanopore sequencing and the algorithms of Nanoplexer, **we would always add extra 4 bp in the anchor sequence next to barcode to guarantee a better performance of demultiplexing**.

## Step 2 Processing of Each Single Cells

After demultiplexing we could run primary pipeline for each single cell, with the input being the initial fastq file and the output being the quantification of each transcript and gene. The primary include four main parts:

- Quality control of reads
- Identify full length cDNA and trim poly-A
- Remove PCR duplication
- Map to reference transcriptome and quantify each transcript and gene

### 1. Quality Control of Reads

First we filtered low-quality reads based read length and quality score, this could be easily accomplished using [NanoFilt](https://github.com/wdecoster/nanofilt) with a single command:

````shell
NanoFilt -q $Q_score -l $length ${cell}.fastq > ${cell}_clean.fastq
````

We generate utilize a q-score of 7 as threshold, which would results in  < 20% per base error rate in the filters reads.

We could also generate a statistic summary of reads quality for each cell using [NanoStat](https://github.com/wdecoster/nanostat):

```shell
NanoStat --fastq ${cell}_clean.fastq -t $threads -o ./ -n ${cell}_stat.txt
```



### 2. Identify full length cDNA and trim poly-A

In the library construction we add adaptor sequence to both ends of full length cDNA, we could use these sequences to identify full length cDNA. This step relies on known adaptor sequences at both ends and could be accomplished using [Pychoper](https://github.com/nanoporetech/pychopper) developed by ONT:

``` shell
cdna_classifier.py \
        -m edlib \
        -b ${primer_dir}/${primer_3plus}.primers.fa \
        -c ${primer_dir}/primer_config.txt \
        -u unclassified.fq -w rescued.fq -A aln_hits.bed \
        -S cdna_classifier_report.tsv -r cdna_classifier_report.pdf \
        -t $threads \
        ${cell}_clean.fastq \
        ${cell}_full_length.fastq
```

Then we further filtered the length of full length cDNA, here we utilize [seqkit]([SeqKit - Ultrafast FASTA/Q kit (shenwei.me)](https://bioinf.shenwei.me/seqkit/)):

``` shell
seqkit seq -m 108 -g ${cell}_full_length.fastq > ${cell}_full_length_filtered.fastq
```

Now we have reads with the structure: $ 5'-cDNA-ployA-UMI$, next we extract the UMI sequence with [UMI-tools](https://github.com/CGATOxford/UMI-tools):

``` shell
umi_tools extract --bc-pattern=NNNNNNNN \
                  --3prime \
                  --stdin=${cell}_full_length_filtered.fastq \
                  --stdout=${cell}_full_length_filtered.extract.fastq
```

Technically now we should have only cDNA-polyA sequence, and the UMI should be stored in the reads name. However, visual inspection demonstrated that ~20% of the reads didn't ends with A. This is possibly due to the insertion in the UMI sequence while sequencing. To address, we cut extra 4 bp at the 3; end of the reads and then trim ploy-A tail:

``` shell
awk '{sub(/.{4}$/,"")}1' ${cell}_full_length_filtered.extract.fa > ${cell}_full_length_filtered.fa

awk '{gsub(/A+$/, "");print}' ${cell}_full_length_filtered.fa > ${cell}_full_length_trim_ploya.fa
```

Now we have clean full length cDNA reads, which could be directly mapping to the reference transcritpome or genome.

### 3. Remove PCR duplications

This is the most difficult part while constructing the pipeline. Our pre-experiment generated a astonishing number of reads: ~700,00,000 reads for 32 cell, which should includes a great number of  duplication events that should be dealt with extra caution. At first we sought to remove duplication using only UMI sequence, which is how we deal with UMIs in NGS-based multiplexed RNA-Seq (`umi_tools count`). This results in an unreasonable number of detected UMIs each cell (500,000 for 8 bp UMI) and poor correlation among cells. This poor performance could be easily understood for several reason. Firstly the high error rate of Nanopore sequencing result in lot of errors in the UMI sequence itself, generating lot of "new UMIs" that didn't exist;. Secondly while mapping to reference transcriptome, same reads could easily be mapped to different isoforms of the same gene, resulting in a lot of secondary alignments. If PCR duplication of same cDNA molecule are mapped to different isoforms, they'll be regarded as tow different UMIs due to the 'per contig' tag in UMI-tools. These questions add great difficulty to handle UMIs properly.

We also tested some other method such as mapping to genome, deduplication per gene, and then annotate the alignments to different transcript. However, annotating alignment to transcript could be very inaccurate and usually requires further alignments. After trying several method it suddenly came to me that we might be able to handle duplications using both UMI sequence and mapping coordinates, which could be used done in the `dedup` mode of UMI-tools.

Actually in the [documentation of UMI-tools count mode](https://umi-tools.readthedocs.io/en/latest/reference/count.html) there are clear explanations about the difference between `count` and `dedup`:

> This tool is only designed to work with library preparation methods where the fragmentation occurs after amplification, as per most single cell RNA-Seq methods (e.g 10x, inDrop, Drop-seq, SCRB-seq and CEL-seq2). Since the precise mapping co-ordinate is not longer informative for such library preparations, it is simplified to the gene. This is a reasonable approach providing the number of available UMIs is sufficiently high and the sequencing depth is sufficiently low that the probability of two reads from the same gene having the same UMIs is acceptably low.
>
> If you want to count reads per gene for library preparations which fragment prior to amplification (e.g bulk RNA-Seq), please use `umi_tools dedup` to remove the duplicate reads as this will use the full information from the mapping co-ordinate. Then use a read counting tool such as FeatureCounts or HTSeq to count the reads per gene.

It is quite clear that for Nanopore-based method, cDNA are not fragmented so the mapping coordinate should be very informative on identifying PCR duplications. So we moved to `umi_tools dedup` to remove duplications.

Since `umi_tools dedup` required mapping coordinates, we first alignment reads to reference transcriptome using [minimap2](https://github.com/lh3/minimap2) and then run `umi_tools dedup`:

``` shell
# 1. mapping all reads to reference cDNA
minimap2 -t $threads\
         -ax map-ont\
         -N 100\
         -p $ratio\
         ${Database_dir}/minimap_ref/${ref}/*.cdna.all.mmi\
         ${cell}_full_length_trim_ploya.fa |\
         samtools view -bS > ${cell}_cdna.bam

# 2. sort and index bam
samtools sort ${cell}_cdna.bam -o ${cell}_cdna.sort.bam
samtools index ${cell}_cdna.sort.bam

# 3. remove PCR duplication using mapping position and UMI
umi_tools dedup --per-gene \
                --per-contig \
                --stdin=${cell}_cdna.sort.bam \
                --stdout=${cell}_cdna.dedup.bam

```

Technically speaking, the bam output of `umi_toos dedup` should be enough for umi counting because it contains the mapping results of each reads and doesn't have PCR duplications. If we use some simple counting software such as *HTSeq* or *FeatureCounts* we could get the transcript-by-cell matrix and then convert to gene-by-cell matrix for downstream analysis. However, it has been reported that [Salmon](https://combine-lab.github.io/salmon/) performs better than these counting softwares on quantification of gene expression and is strongly advised for TGS based method. So we decided to adopt Salmon in or pipeline. However, the accurate quantification of salmon requires the correct Flags in the sam file, which indicated the properties of reads including mapping results, reads pairs... The  `uim_tools dedup`  command would remove not only duplicated reads but also secondary alignments, which is not required for downstream counting but is required for the correct quantification of Salmon. We came up with a simple solution to address this problem: extract unique reads from the output file and realign it to generate a sam file with proper Flags as the input of Salmon. This would definitely takes more time but guaranteed the reliability of our outputs.

### 4. Map to Reference Transcriptome and Quantification of Expression

As described above we extract unique reads sequence in the fasta format from the output of `umi_tools dedup`:

```shell
samtools fasta ${cell}_cdna.dedup.bam > ${cell}.dedup.fa
```

and then realign them to the reference transcriptome:

``` shell
minimap2 -t $threads\
         -ax map-ont\
         -N 100\
         -p $ratio\
         ${Database_dir}/minimap_ref/${ref}/*.cdna.all.mmi\
         ${cell}.dedup.fa |\
         samtools view -bS > ${cell}_cdna.dedup.bam
```

Finally we quantify the expression level of each transcript and gene with salmon:

``` shell
salmon quant -p $threads --noErrorModel -l U\
         -t ${Database_dir}/minimap_ref/${ref}/*.cdna.all.fa\
         -a ${cell}_cdna.dedup.bam\
         -o ${cell}_cdna_salmon_quant\
         -g ${Database_dir}/minimap_ref/${ref}/TranscriptID_GeneID_from_cDNA_fasta.txt
```

## Step 3 Summarize All Cells

The primary pipeline is designed for each single cell. However, our expected output of the pipeline is the gene/transcript-by-cell matrix. So we need to bind the expression profile of each file to generate a single matrix.  This could be easily accomplished with custom codes. Apart from the UMI count matrix, we also want to generate a statistic summary of this experiment, including the initial read count, QC read count, mapping rate, UMIs count, etc.  All these information could be extracted from the log files with simple text processing tools such as `grep` and `awk`. Details of the code are not shown here.



This computation pipeline may seems a little complicated and requires several independent step to finally get all the output properly. To make it easier to use, I constructed a relatively simple script to submit all the computational jobs mentioned above in a single command. The orders and dependencies among jobs are delicately arranged to guarantee the proper working of the pipeline. To run the pipeline, all the user need to do is to run:

```shell
./RUN.HTP_UMI_SCANSeq.sh
```

or 

``` shell
sh RUN.HTP_UMI_SCANSeq.sh
```

I constructed and tested the pipeline on the High Performance Computing Platform of CLS, which is use Slurm workload manager. Currently I haven't write a SGE version of the pipeline so we could not run the pipeline on the server of our lab.

# Future Improvements

Single-cell full length RNA Seq with UMI is still a technological problem to the field. Currently we have some computational tools to process Nanopore data under its high sequencing rate. For example, Nanoplexer could handle long barcode sequence in Nanopore reads correctly and generate satisfactory results. However, we definitely need more tools for TGS data processing, both for mapping and quantification, as well as UMI processing. **The frequent sequencing error in UMI could result in very strong disturbance in both identification and quantification of UMI**. Current publications all chose to ignore the sequence err in UMI as we did for NGS-based method. We all know that this is not reasonable however, have no good solution to it yet. I think this is the most important problem to be addressed in the processing of TGS scRNA-Seq data.

Another possible improvement is to omit the demultiplex step and process all the reads together, as we did for NGS-based data. This could definitely improve computational efficiency. However, I don't have very good ideas how to achieve that. We might need to wait for some time to see what powerful tools bioinformatics programmers could bring us.

  <p align="right">Zhenyu</p>

  <p align="right">at Peking University Library</p>

  <p align="right">2020.12.14</p>