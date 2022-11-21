---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: post_20221014
title: "Program of Single Cell Omics Beijing 2022."

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
author: Zhenyu Liu
# multiple category is not supported
category: Work
# multiple tag entries are possible
tags: [Bioinformatics, Meeting]
# thumbnail image for post
img: ":post_20221014/cover.jpg"
# disable comments on this page
comments_disable: true

# publish date
date: 2022-10-14 08:11:06 +0900

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

Notes from Program of Single Cell Omics Beijing 2022. 

<!-- outline-end -->

* TOC
{:toc}

# Program of Single Cell Omics Beijing 2022

Oct. 13-14, 2022. Beijng China

## Opening

## Session 1

Moderator: Xiaoliang Sunney Xie

![image-20221013104825659](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013104825659.png)

### **Bing Ren**: Illuminating the Dark Matter in Human DNA with Single-cell Epigenomics Analysis

- background: "risk variants associated with gene expression regulation"

  ![image-20221013104254925](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013104254925.png)

- Method development (sci-based):

  - Experimental: snATAC-Seq, snMethyl-HiC, Paired-Tag/Seq

  - Computational: SnapATAC, SnapHiC

    ![image-20221013105131216](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013105131216.png)

- Predicting disease-associated cell types

  Utilize GWAS data, analysis enrichment in cell types by intersecting with cCREs.

  ![image-20221013105850435](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013105850435.png)

![image-20221013105926574](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013105926574.png)

- Identify key regulatory elements associated with disease

- Summary:

![image-20221013110318805](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013110318805.png)

- Q&A:
  - Associated cCREs with genes

### **Jay Shendure**: Reconstruction & Recording of Mammalian Development

- background: development of single-cell methods

- scRNA-seq of ~2 million cells in one experiment (sc-based, $384 ^ 3$ )

  ![image-20221013112557477](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013112557477.png)

- Epithelial development

  ![image-20221013112701901](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013112701901.png)



## Session 2

Moderator: Fuchou Tang

![image-20221013113006379](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013113006379.png)

### **Bart Deplancke**: Engineering Next-generation Single Cell Phenomics     Technologies

- DisCo

- Live-seq 

  - minor perturbation on target cells

  - sequential Live-seq: state transition of the same cell

    ![image-20221013155506466](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013155506466.png)

  - transcriptomic recorder

### **Rickard Sandberg**: Scalable Full-length scRNA-seq for Temporal Analyses of Transcription and Dissections of Cell States and Subtypes

- NASC-seq2: single-cell nascent RNA sequencing 

  ![image-20221013161723120](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013161723120.png)

  - Co-bursting: do nearby genes burst independently?

    ![image-20221013162052659](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013162052659.png)

  - general independent transcription of two alleles

    ![image-20221013162407531](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013162407531.png)

  - co-bursting outliers :

    ![image-20221013162527330](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013162527330.png)

- Smart-seq3xpress: scalable, cost efficient

questions:

pseudo-gene expression and duplicated genes may contributed to co-bursting outliers. mentioned pseudo-gene expression. however, the investigation of pseduo-gene influenced by the high sequence similarity, specific steps to resolve this.

### **Angela Ruohao Wu**: Multi-step Single-cell Multi-omics Methods for Simultaneous Dissection of Phenotype and Genotype  Heterogeneity from Frozen Tumors

- Mouse Lemur Single Cell Atlas

  ![image-20221013164210589](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013164210589.png)
  
- scONE-seq: one tube single-cell WGS and RNA-sequeicing

  - single-cell multi-omics is especially useful for cancer analysis.

  - existing single-cell DNA&RNA methods:

    ![image-20221013164720689](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013164720689.png)

  - principles of scONE-seq

    ![image-20221013164806662](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013164806662.png)

  - performance:

    RNA (total RNA):

    ![image-20221013164937465](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013164937465.png)

    CNV:

    ![image-20221013165115827](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013165115827-16656510770611.png)

  - discoveries:

    a novel tumor sub-clone in astrocytoma

    ![image-20221013165506031](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013165506031.png)

    Tumor cells with minor difference on transcription identified from CNV information,

    ![image-20221013165838767](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013165838767.png)

  - summary

    ![image-20221013170129976](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013170129976.png)

### **Guoji Guo**:Mapping Cell Landscapes at Single cell Level

- background: equation for cell fate decision

- Microwell-seq

  ![image-20221013171252054](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013171252054.png)

- Microwell-seq 2.0

  ![image-20221013171408431](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013171408431.png)

- human atlas
  - inflamed structural (endothelial, epithelial, stromal) cells, validated *in vivo*.

- mouse atlas

- lifespan cell landscape analysis

  ![image-20221013171855788](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013171855788.png)

  - inflammation in structural cells
  - mitochondria metabolism

- how cell types are regulated?

  - TF dynamics

  ![image-20221013172440815](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013172440815.png)

  - Cross-species analysis of common TFs during differentiation

- Nvwa

  ![image-20221013172827826](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013172827826.png)

  

### **Chenghang Zong**: Total-RNA Based scRNA-seq Allows Genome-wide       Identification of Transcriptional and Post-transcriptional Regulation

- background: Total-RNA based single-cell RNA-seq

  ![image-20221013174643712](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013174643712.png)

  chemistry of MATQ-seq:

  ![image-20221013174751062](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013174751062.png)

- SMART-MATQ seq

  ![image-20221013174909036](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013174909036.png)

  include intron (nascent), more appropriate for RNA velocity.

- characterize the cell dynamics in cell cycle

  ![image-20221013175307403](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013175307403.png)

- differential gene expression along certain trajectory:

  - method: tradeSeq (2020, Nat commu)

  - compare DEG of  mature and nascent RNAs defines 3 types of distinct cell cycle genes (CCGs)

    ![image-20221013175527200](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013175527200.png)

  - Novel cell cycle genes

    ![image-20221013175908999](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013175908999.png)

  - dynamic modules in different CCGs

    ![image-20221013180053256](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221013180053256.png)

    

Question: 

- during CCG identification, the significance of type III CCGs? (nascent only) how to explain stochastic fluctuation or some biological mechanisms.
- why identify novel CCGs in type I? since type 1 could be detected by mature RNA alone. 

附赠一个彩蛋hhhh

![image-20221014161343076](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014161343076.png)

## Section 3

Moderator: Yanyi Huang

![image-20221014093438690](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014093438690.png)

### **Ning Jenny Jiang**: High-throughput and High-Dimensional Single T Cell Profiling

- pMHC generation by IVTT

- TetTCF-seqHD

  ![image-20221014095053647](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014095053647.png)

- performance on CD8+ T cells

- conclusions

  ![image-20221014100035359](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014100035359-16657128363801.png)

### **Yanyi Huang**: Improving the Information Efficiency for Fast and Spatially Resolved Sequencing

- ECC sequencing methods:

- bit-seq

  ![image-20221014102317219](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014102317219.png)

### **Fuchou Tang**: Single Cell Omics Sequencing Technologies: The Next  Generation

- SCAN-seq: full-length scRNA-Seq
- SCAN-seq2: higher throughput
- SMOOTH-seq2: scWGS sequencing
- single-cell assembly

### **Zemin Zhang**: Dynamic Changes of The Tumor Micro-environment During Immunotherapies

- background: tumor microenvironmnt

  ![image-20221014111325598](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014111325598.png)

- composition: certain cell types

  ![image-20221014111458791](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014111458791.png)

  ![image-20221014111600587](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014111600587.png)

- heterogenity:

  - pan-cancer analysis of infiltrating myeloid cells

    ![image-20221014111735356](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014111735356.png)

  - pan-cancer analysis of infiltrating T cells

    ![image-20221014111810332](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014111810332.png)

- Temporal dynamics

  - dynamics of T cells

    ![image-20221014111847298](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014111847298-16657175299453.png)

  - dynamics of LAMP3+ DCs in TAMs in HCC

    ![image-20221014111920663](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014111920663.png)

- **clinical relavance**

  - responsive tumor showed decrease of terminal Tex

    ![image-20221014112136958](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014112136958.png)

### **Xiaoqun Wang**: Spatial Mutli-omics Sequencing the Developing Human  Cerebellum

## Session 4

Moderator: Yanyi Huang

![image-20221014113343017](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014113343017.png)

### **Alexander van Oudenaarden**: Acceleration of Genome Replication Uncovered by Single-cell Nascent DNA Sequencing

- question: measure velocity of genome replication![image-20221014153223277](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014153223277-16657328365585.png)

    - single-molecule methods

    - single-molecule measurement differs from single-cell measurement

      ![image-20221014153556341](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014153556341.png)

- scEdUseq: single-cell measurement replication speed

  ![image-20221014153722898](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014153722898.png)

  concord with previous repilcation start sites

  ![image-20221014153907123](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014153907123.png)

- single pulse and pair pulse

  ![image-20221014154313554](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014154313554.png)

  ![image-20221014154355545](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014154355545.png)

- replication velocity increase with s-phase progression

  ![image-20221014154554385](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014154554385.png)

  this might be correlated with transcription (increase after inhibition)

  ![image-20221014154731763](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014154731763.png)

- mechanism:

  - hyposis:

    ![image-20221014154825042](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014154825042.png)

  - inhibit transcription lead to increased DNA damage

    ![image-20221014154851696](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014154851696.png)

- conclusions

  ![image-20221014155141927](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014155141927.png)

### **David Weitz**: Applications of Single Microbe Sequencing

- background: single microbe sequencing

  ![image-20221014160623546](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014160623546.png)

- Msc RNA-seq(fixed cells)

  - workflow
  
    ![image-20221014160842215](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014160842215.png)

  - single-cell selection:

    ![image-20221014160952722](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014160952722.png)

  - performance:

    ![image-20221014161137818](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014161137818.png)

  - filter out rRNA using DASH

    ![image-20221014161236942](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014161236942-16657351572781.png)

    ![image-20221014161303916](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014161303916.png)

  - biological question: drug treatment of E coli, time series

    ![image-20221014161542168](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014161542168.png)

  - benchmark

    ![image-20221014161745227](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014161745227.png)

- Microbe-Seq genome sequencing 

  ![image-20221014162037046](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014162037046.png)

  - work flow

    ![image-20221014161945581](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014161945581.png)

  - performance

    ![image-20221014162153557](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014162153557.png)

    ![image-20221014162159169](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014162159169.png)

  - single-strain sequencing

    ![image-20221014162449709](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014162449709.png)

  - phages associated with strain

    ![image-20221014162709883](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014162709883.png)

### **Amos Tanay**: Single Cell Models for Deciphering the Birth of Cell-type  Specific Epigenetics During Gastrulation

![image-20221014163715048](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014163715048.png)

- What is an atlas?

  - dimensional reduction embeddings?
  - gene expression profiles?
  - A group of linked quantitative distributions over all genes !

  ![image-20221014163916493](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014163916493.png)

- how to use atalses in 2020:  query projection on atlas

  ![image-20221014164014068](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014164014068.png)

  - for known cell types:

    ![image-20221014164445876](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014164445876.png)

  - for novel cell types:

    ![image-20221014164504959](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014164504959-16657373197333.png)

- how to use atlas in 2022: model dynamics of cells.
![image-20221014164845083](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014164845083.png)

### **Ge Gao**: Rationally Design Generative Models for Delineating the  Regulator Map in silico

- background: gene expression regulation

  ![image-20221014170755658](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014170755658.png)

- intuition: learn the regulating mechanisms from data

  ![image-20221014171047147](https://raw.githubusercontent.com/liuzhenyu-yyy/liuzhenyu-yyy.github.io/main/assets/img/posts/post_20221014/image-20221014171047147.png)









