---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: post_20211016
title: "Program of Single Cell Omics Beijing 2021."

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
author: Zhenyu Liu
# multiple category is not supported
category: Work
# multiple tag entries are possible
tags: [Bioinformatics, Meeting]
# thumbnail image for post
img: ":post_20211016/cover.png"
# disable comments on this page
comments_disable: true

# publish date
date: 2021-10-16 08:11:06 +0900

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

Notes from Program of Single Cell Omics Beijing 2021. 

<!-- outline-end -->

---
* TOC
{:toc}

# Program of Single Cell Omics Beijing 2021

Oct. 15-16, 2021. Beijng China

## Opening

## Session 1

### **Steve Henikoff**: Single-cell Profiling of Chromatin Landscapes

### **William Greenleaf**: Exploring the Physical Genome in Health and Disease

- scATAC-Seq and scRNA-Seq of blood development and Acute leukemia

- Developing of fetal heart

  利用体内分化的ATAC数据指导体外分化，UMAP Projection

- Predict gene expression

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015100345509.png" alt="image-20211015100345509"  heigh="150" >


Q&A: 细胞周期在scRNA中影响很大，但是在scATAC中并不明显hhhh

### **Stephen Quake**: The Cell as a Bag of RNA

Tabula Organisms

- Mouse Aging Cell Atlas: Tabula Mouse

- Fly Cell Atlas

- Tabula Sapiens Project (BioRxiv)

  15 donors, 481,120 cells
  
- cross-species integration

### **Bing Ren**: A Single-Cell Atlas of Chromatin Accessibility in the Human Genome

- sciATAC-Seq of Mouse Cerebrum (Nature, 2021, Oct)

- sciATAC-Seq of fetal and adult brain

  1.2 million cREs, 222 cell types

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015103937578.png" alt="image-20211015103937578"  heigh="150" >

- scATAC of lung (covid-19)

  肺泡细胞顺式作用原件上的点突变与预后相关。

Q&A: 

1. 神经细胞的类群注释依赖先验的scRNA-Seq数据

2. scRNA鉴定的功能基因群在scATAC无法复现，scATAC更稳健，显示的是更深层的稳定结构
3. 不同组织的消化与提核？Sebastian Preissl多次优化提核条件，对于不同的组织采用了5个不同Protocol，不同的Protocol在一遍bioRxiv中有详述。

## Session 2

### **Sunney Xie**: Bisulfite-free High-coverage Detection of DNA Methylation and Hydroxyl Methylation During Early Embryo Development at the Single cell Level

- Potent Neutralizing Antibodies against Covid-19

  - High throughput screening of antibody, DXP-604不存在antibody escape现象，对所有变种病毒有效。
  - 结构：避免antibody escape的原因：DXP-604结构与ACE2结合位点类似，escape DXP-604的变体不具有感染性。

- Bisulfite-free High-coverage detection DNA Methylation and Hydroxyl Methylation at the Single cell Level

  - 不使用bisulfite的bulk方法：TET2+β-GT保护，再用APOBEC转化。需要两次纯化，coverage较低。
  - Cabernet and Cabernet -H

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015151926483.png" alt="image-20211015151926483"  heigh="150" >

  - 高转化率（>99%），高coverage，高mapping rage（~80%）。
  - sci-Cabernet-Seq，barcoded Tn5实现multiplexing。
  - Profiling 5mC and 5hmC in early mouse embryo

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015152409797.png" alt="image-20211015152409797"  heigh="150" >

Q&A: 

1. cost：成本高于scRNA-Seq，低于scWGS

### **Amos Tanay**: New Single Cell Strategies for Characterizing the Function of DNA Methylation During Gastrulation
- single cell data and model dynamics
- disturb: 敲除TET gene的mESC，注射进入ICM，产生完全敲除(TET-TKO) or 嵌合敲除的完整胚胎，再进行全胚胎的scRNA-Seq，检测各种细胞类型的比例。

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015155124866.png" alt="image-20211015155124866"  heigh="150" >

### **Ge Gao**: Multi-omics Integration and Regulatory Inference for Unpaired Single-cell Data with a Graph-linked Unified Embedding Framework

- Current challenges:
  - batch effect
  - sophisticated inter/intra-layer interactions
  - scalability to the ever-expanding data size
  - interpretability to translate computational models to biological insights
- Cell Blast: integration of scRNA-Seq

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015161508355.png" alt="image-20211015161508355"  heigh="150" >

  - Adversarial Learning to model inter-dataset batches

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015161658795.png" alt="image-20211015161658795"  heigh="150" >

  - multi-level batch effect

     情景：不同数据集内部仍然存在batch effect，如不同研究，每个研究多个个体，传统方法无法有效处理


- GLUE: Integration of multi-omics data

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015162150463.png" alt="image-20211015162150463"  heigh="150" >

​	整合的效果显著好于之前发表的其他方法：

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015162501055.png" alt="image-20211015162501055"  heigh="150" >

- [GeACT](http://geact.gao-lab.org/)

Q&A: 

1. trade off of batch effect and biological difference.

   fully-auto batch correction is impossible.



### **Rickard Sandberg**: Decoding Transcriptional Regulation and Kinetics Using Single-Cell Transcriptomics

- Current problem for scRNA-Seq experiments

  - trade off of cell number and gene number

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015164644340.png" alt="image-20211015164644340"  heigh="150" >

- Demand for scRNA-Seq technologies

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015164739765.png" alt="image-20211015164739765"  heigh="150" >


- Smart-Seq3xpress: scalable, full-coverage scRNA-Seq (bioRxiv)

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015215727125.png" alt="image-20211015215727125"  heigh="150" >

  - HEK293T K562基因数稳定在6000左右

  - cost-effiecnt: lower than Smart-Seq2 and Smart-Seq3

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015215745611.png" alt="image-20211015215745611"  heigh="150" >

  - pilot data from PBMCs (16K cells)

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015165226619.png" alt="image-20211015165226619"  heigh="150" >

    16K 细胞准确捕捉到各个亚群

- UMI and molecular spikes: accurate RNA counting in scRNA-Seq (bioRxiv)

  - 可以用于反映scRNA-Seq的准确程度

  - benchmarking UMI collapse stragies

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015165916356.png" alt="image-20211015165916356"  heigh="150" >
    
<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015170058279.png" alt="image-20211015170058279"  heigh="150" >

- BAMboozle: removes genetic variation from human sequence data for open data sharing （NC in press)
  - mask掉人类数据中个体特异的variation，从而减小data sharing带来的风险。
  
- Regulation of transcriptional burst
  - NASC-Seq2: 鉴定新合成的mRNA

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015170412704.png" alt="image-20211015170412704"  heigh="150" >
  - new RNA反映出Total RNA无法反映的异质性

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015170610190.png" alt="image-20211015170610190"  heigh="150" >

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015170650752.png" alt="image-20211015170650752"  heigh="150" >

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015170948904.png" alt="image-20211015170948904"  heigh="150" >

Q&A:

1. Smart-Seq3xpress vs Smart-Seq3
   - Smart-Seq3 没有UMI，无法绝对定量
   - Smart-Seq3xpress相比于Smart-Seq3没有明显的decreasing（lose the ability to see that you can have better data hhhhh)

2. NASC-Seq2 

### **Sten Linnarsson**: Molecular Architecture of the Developing Mouse Brain Single Cell

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211015174012879.png" alt="image-20211015174012879"  heigh="150" >

Q&A:

1. quality control of atlas-level scRNA-Seq project
   - shallow sequence对样品进行质控
   - QC 指标：Fraction of unspliced reads，质量不好的细胞or死细胞会有更高比例

## Session 3

打球去了……

### **Chen Wu**: Dynamic Molecular and Cellular Alterations in Multi-step Cancer Development

### **Muzlifah Haniffa**: Decoding the Developing Human Immune System

### **Fan Bai**: Somatic Mutagenesis in Morphologically Normal Human Tissues

### **Xuefei Zhang**: Chromatin Loop Extrusion Plays Mechanistic Roles in Antibody Diversification

## Session 4

### **Christopher A. Walsh**: The Architecture of Human Brain Somatic Mutations in Health and Disease

- pathogenic mutations in normal human brain (Cancer Discovery,2021 Aug)

  - 5% of normal humans have cancer-associated mutations

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016083904421.png" alt="image-20211016083904421"  heigh="150" >

  - pathogenic mutations appears to decrease with age

  - large scale CNV present in 5-8% of normal brains

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016084048170.png" alt="image-20211016084048170"  heigh="150" >

- 人各个lineage 的somatic mutation profile (Science,2021 Mar)

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016084431648.png" alt="image-20211016084431648"  heigh="150" >
  - 早期卵裂产生的细胞，对胚胎贡献的细胞数是高度不平均的

  - human cortex shows surprisingly integrated clonal structure

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016085012393.png" alt="image-20211016085012393"  heigh="150" >

- Neuronal genome in the aging brain (bioRxiv)

  - 神经元中的SNP会随着年龄积累(15-20 per year)
  - MDA会带来false positive SNPs，PTA显著好于MDA：扩增均匀，假阳性低
  - PTA and NanoSeq reveals increasing indels in aging neurons, possibly resulting from transcription.

- summary

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016085658174.png" alt="image-20211016085658174"  heigh="150" >

  Q&A:

  1. functional consequence of accumulated SNPs ? disease ?
  2. Enhancers are enriched for mutations.
  3. survival of mutated neurons. do the colons die? to be expored.
  4. mutation frequency of cycling and non-cycling cells.

### Chenghang Zong: Droplet Based High-Throughput Transcriptome Profiling of Individual Synapses Using Single-Cell Total-RNA-Seq
- MATQ-Drop: Droplet single-cell total-RNA-based chemistry (Unpublished)

  - high degree of morphological and electro-physiological diversity
  - challenges of single-synapse RNA-Seq
    1. synapse are fragile: **fixation** to prevent RNA leakage and degradation 
    2. low RNA abundance in single synapses: higher sensitivity
    3. local RNA splicing in synapses: **Total RNA**
  - Current scRNA-Seq methods are not applicable to synapses 
    - require fresh cee
    - poly-T primers, capture poly-A of mature RNA
    - limited intronic coverage
  - MATI-Drop protocol

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016091704036.png" alt="image-20211016091704036"  heigh="150" >

  - 测试：等量HEK293T与3T3 混合，物种特异性 > 90
  - sensitivity of MATQ-Drop

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016091850146.png" alt="image-20211016091850146"  heigh="150" >

  sensitivity 略低于Smart-Seq2，与10X类似，但是适用于fixed sample。

- Construction of cell atlas using only nascent RNA or lncRNA

  - cell atlas of nascent RNA

  - cell atlas of lncRNA

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016092200690.png" alt="image-20211016092200690"  heigh="150" >

- Transcriptome profiling of individual synaptosomes
  
  - subtypes in the synapses and other neuronal junctions
  
<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016092449573.png" alt="image-20211016092449573"  heigh="150" >
  
<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016092628731.png" alt="image-20211016092628731"  heigh="150" >
  
    
  
  - Synapse and nuclear specific RNAs
  
  - Cell-type specific intron retentions
  
<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016093242094.png" alt="image-20211016093242094"  heigh="150" >

### **Cai Long**: Spatial Multi-omics: RNA and DNA seqFISH+

- DNA and RNA Sequential Fish + (Nature, 2021)

  - seqFish

    多轮barcoding实现对mRNA的条码编码

  - RNA SeqFish+

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016094803080.png" alt="image-20211016094803080"  heigh="150" >

  - DNA and RNA SeqFish+

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016094847385.png" alt="image-20211016094847385"  heigh="150" >

- Some observations

  - non-repetitive DNA loci are located on the surface of nuclear bodies

  - actively transcribing genes appear at interfaces

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016095839850.png" alt="image-20211016095839850"  heigh="150" >

  - Chromatin interactions occur on 2D surfaces

  - "Proximity Points" anchor chromosomes  to nuclear bodies

- Summary

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016100951676.png" alt="image-20211016100951676"  heigh="150" >

Q&A

1. detection of enhancer RNA

### **Longzhi Tan**: Mapping the Dynamics of the Linear and 3D Genome of Single Cells in the Developing Brain
- Challenges of 3D Genome structure

  - high heterogeneity among cells: single cell resolution
  - low DNA concentration and complicated structure

- Previous work

  - DipC, Science, 2018
  
    > [Three-dimensional genome structures of single diploid human cells](https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=za9F5FgAAAAJ&citation_for_view=za9F5FgAAAAJ:YsMSGLbcyi4C)
    >
    > L Tan*, D Xing*, CH Chang, H Li, XS Xie
    >
    > Science 361 (6405), 924-928
  
  - LIANTI, Science, 2017
  
    > [Single-cell whole-genome analyses by linear amplification via transposon insertion (LIANTI)](https://scholar.google.com/citations?view_op=view_citation&hl=zh-CN&user=za9F5FgAAAAJ&citation_for_view=za9F5FgAAAAJ:Tyk-4Ss8FVUC)
    >
    > C Chen*, D Xing*, L Tan*, H Li*, G Zhou, L Huang, XS Xie
    >
    > Science 356 (6334), 189-194

- 3D genome and trasncriptome of developing mouse brain

  - 利用scRNA可以准确鉴定发育各个阶段的细胞类型。

  - 利用3D genome 可以降维聚类，但需要scRNA帮助进行cell typing。

  - 3D基因组的变化与RNA的变化显著相关

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016103056888.png" alt="image-20211016103056888"  heigh="150" >

  - 发育中，很多基因的空间位置向内部移动

- Summary

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016103235727.png" alt="image-20211016103235727"  heigh="150" >

Q&A:

1. 测序深度与cell type resolution:

   - 区分大的细胞类型3k-5k contact

   - 具体的神经细胞亚群20k contact

2. Cell Cycle

   - cortex 不分裂，影响不大
   - 部分galia存在细胞周期，且对3D基因组的影响很明显，需要解决

## Session 5

### **Guoji Guo**: Inferring Genetic Models from Cell Landscapes

- Microwell-Seq (Cell, 2018)

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016153458157.png" alt="image-20211016153458157"  heigh="150" >

  - gentle to cell (no FACS)
  - low cost
  - high throughput

- Microwell-Seq 2.0 (in press)

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016153652426.png" alt="image-20211016153652426"  heigh="150" >

  - random primer, higher sensitivity
  - higher throughput

- Cell Landscape Project

  - Questions: how many cell types? how cell fate determined?

  - Human Cell landscape (Nature. 2020)

  - Mouse Cell landscape: 120,000 cells

  - Observations: 

    - Immune-related stromal and epithelial cells

    - transitional cells

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016154501659.png" alt="image-20211016154501659"  heigh="150" >
      

  - How is cell fate regulated?

    - Entropy Reduction
    - lineage specific and common TF dynamics

- Predicting probability of expression by deep learning

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016155230935.png" alt="image-20211016155230935"  heigh="150" >

  ​	overall AUC在0.8左右

Q&A:

1. doublet and transitional cells. 

   pre-barcoding，多重barcode，无法百分百 保证不存在doublet

### **Alexander van Oudenaarden**: Ribosomal Profiling in Single Cells

- Ribosome profiling provides attractive approach to measure translation

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016161208420.png" alt="image-20211016161208420"  heigh="150" >

- scRibo-Seq: Experimental Procedure

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016161414221.png" alt="image-20211016161414221"  heigh="150" >

- **ribosomal protected fragments**(RPF) are enriched in coding sequencing and have 3-nt periodicity

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016161545823.png" alt="image-20211016161545823"  heigh="150" >

- Arg-codon-pausing predominately occurs during expression of histone genes

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016162257676.png" alt="image-20211016162257676"  heigh="150" >

- Pronounced GAA stalling is observed during mitosis, and affects many genes 

- Summary

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016162914292.png" alt="image-20211016162914292"  heigh="150" >

Q&A

1. how many cells to sequence?

   单细胞分辨率，稳健结果1k~2k cells

### **Xiaoqun Wang**: The Diversity of Neurogenesis and Evolution in Human Cerebral Cortex

不感兴趣  at all...

### **Wolf Reik**: Single Cell Multi-Omics Landscape of Development and Ageing

- Conceptual limitations of single-cell genomics

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016171401783.png" alt="image-20211016171401783"  heigh="150" >

  

## Session 6

### **Yanyi Huang**: Sequencing Trace Amount of Nucleic Acids: for Mini-bulk and Single-cell Samples

吃饭去了

Q&A

1. FISH validation of CNVs
2. Cause of CNV in normal somatic cells

### **Fuchou Tang**: Decoding the Mechanisms of Human Development and Diseases by Single cell Genomics Approaches

- Large-scale single cell RNA-Seq of human FGCs and their niche cells

  > ### [Single-cell RNA-seq analysis maps development of human germline cells and gonadal niche interactions](https://www.sciencedirect.com/science/article/pii/S1934590917300784)
  >
  > [L Li](https://scholar.google.com.hk/citations?user=T8mqisMAAAAJ&hl=zh-CN&oi=sra), [J Dong](https://scholar.google.com.hk/citations?user=DfkHKmEAAAAJ&hl=zh-CN&oi=sra), L Yan, J Yong, X Liu, Y Hu, [X Fan](https://scholar.google.com.hk/citations?user=rvv3Q6AAAAAJ&hl=zh-CN&oi=sra), X Wu… - Cell stem cell, 2017 

  - new: 10X and experimental validation (unpublished)

  - loss of X chromosome

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016200859986.png" alt="image-20211016200859986"  heigh="150" >

- SCAN-Seq(Plos Biology, 2021)

  > ### [Single-cell RNA-seq analysis of mouse preimplantation embryos by third-generation sequencing](https://journals.plos.org/plosbiology/article?id=10.1371/journal.pbio.3001017)
  >
  > X Fan, D Tang, Y Liao, [P Li](https://scholar.google.com.hk/citations?user=UwqMLUYAAAAJ&hl=zh-CN&oi=sra), Y Zhang, M Wang… - PLoS …, 2020 - journals.plos.org
  - SCAN-Seq2

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016201651771.png" alt="image-20211016201651771"  heigh="150" >

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016201704384.png" alt="image-20211016201704384"  heigh="150" >

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016201714740.png" alt="image-20211016201714740"  heigh="150" >

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016201723415.png" alt="image-20211016201723415"  heigh="150" >

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016201735074.png" alt="image-20211016201735074"  heigh="150" >

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016201800319.png" alt="image-20211016201800319"  heigh="150" >

​		当时数据质量这么好……泪目。

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016202427254.png" alt="image-20211016202427254"  heigh="150" >

- SMOOTH-Seq (Genome Biology, 2021)

  > ### [SMOOTH-seq: single-cell genome sequencing of human cells on a third-generation sequencing platform](https://link.springer.com/article/10.1186/s13059-021-02406-y)
  >
  > X Fan, [C Yang](https://scholar.google.com.hk/citations?user=CJpcEFcAAAAJ&hl=zh-CN&oi=sra), W Li, X Bai, X Zhou, H Xie, L Wen… - Genome biology, 2021 - Springer
  - SMOOTH-Seq2

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016202536518.png" alt="image-20211016202536518"  heigh="150" >

  Identify the 'dark matter' in the genome!

Q&A:

1. better cell typing on isoform level? To be tested on tissue sample.
2. Long WGS on cancers? In progress.

### **Zemin Zhang**: Dynamic Changes of Tumor Infiltrating Immune Cells During Immunotherapies

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016203411325.png" alt="image-20211016203411325"  heigh="150" >

- Early work on infiltrating myeloid cells cross cancer types
- Immunotherapy is all about modulating tumor micro-environment (TME)

- mechanisms of T cell exhaustion in lung cancer

  - responsive tumors shows preferential decrease of terminal Tex cells

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016204039661.png" alt="image-20211016204039661"  heigh="150" >

  - identify Tex/tumor responsive T cell subset by Tex TCR

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016204208814.png" alt="image-20211016204208814"  heigh="150" >

  - Tex precursor (Texp) accumulates in responsive tumor after treatment

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016204330021.png" alt="image-20211016204330021"  heigh="150" >

  - Mechanisms for the formation and accumulation of Texp cells

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016204509264.png" alt="image-20211016204509264"  heigh="150" >

  - Summary

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016204749825.png" alt="image-20211016204749825"  heigh="150" >

- Triple negative breast cancer (TNBC)

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016204946940.png" alt="image-20211016204946940"  heigh="150" >

  - Experiment Design

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016205046331.png" alt="image-20211016205046331"  heigh="150" 

  - single profiling

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016205142400.png" alt="image-20211016205142400"  heigh="150" >

  - CXCL13+ T cells play a key role

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016205326511.png" alt="image-20211016205326511"  heigh="150" >

  - B cells were enriched in responders of the combination therapy

  - B cells were highly correlated with CXCL13+ T cells in TME

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016205502470.png" alt="image-20211016205502470"  heigh="150" >

  - Pro-inflammatory macrophages play roles in T cell recruitment

  - CXCL13+ T cells were highly correlated with Mφ

  - Summary

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016205726165.png" alt="image-20211016205726165"  heigh="150" >

- Overview of functional properties of immune cells in TME

<img src="https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20211016/image-20211016205821740.png" alt="image-20211016205821740"  heigh="150" >

Q&A:

1. Dynamic changes of stromal cells (fibroblast) during treatment.
2. Texp: tumor reactive, molecular mechanisms to be determined.

## Ending

