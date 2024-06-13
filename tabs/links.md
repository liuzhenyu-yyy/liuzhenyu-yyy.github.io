---
layout: links
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_links

# publish date (used for seo)
# if not specified, site.time will be used.
#date: 2022-03-03 12:32:00 +0000

# for override items in _data/lang/[language].yml
#title: My title
#button_name: "My button"
# for override side_and_top_nav_buttons in _data/conf/main.yml
#icon: "fa fa-bath"

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-03-03 12:32:00 +0000
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


# you can always move this content to _data/content/ folder
# just create new file at _data/content/links/[language].yml and move content below.
###########################################################
#                Links Page Data
###########################################################
page_data:
  main:
    header: "Publications"
    info: "Marks: co-first author†, corresponding author&#42;."

  # To change order of the Categories, simply change order. (you don't need to change list order.)
  category:
    - title: "2024"
      type: id_2024
      color: "#8da0cb"
    
    - title: "2023"
      type: id_2023
      color: "#fc8d62"

    - title: "2022"
      type: id_2022
      color: "#66c2a5"

  list:
    -
    # Research article
    - type: id_2024
      title: "Single-Cell Chromatin Accessibility Analysis Reveals the Epigenetic Basis and Signature Transcription Factors for the Molecular Subtypes of Colorectal Cancers"
      author: "<b>Liu, Z.</b>†, Hu, Y.†, Xie, H.†, Chen, K.†, Wen, L., Fu, W., Zhou, X.&#42;, Tang, F.&#42;"
      info: "<i>Cancer Discovery</i>, 2024"
      url: "https://doi.org/10.1158/2159-8290.CD-23-1445"
      pdf: "/assets/publication/CD-23-1445R1_Merged_PDF.pdf"

    - type: id_2023
      title: "High-throughput and high-sensitivity full-length single-cell RNA-seq analysis on third-generation sequencing platform"
      author: "Liao, Y.†, <b>Liu, Z.</b>†, Zhang, Y.†, Lu, P., Wen, L., Tang, F.&#42;"
      info: "<i>Cell Discovery</i>, 2023"
      url: "https://doi.org/10.1038/s41421-022-00500-4"
      pdf: "/assets/publication/s41421-022-00500-4.pdf"

    - type: id_2022
      title: "Single-cell Sequencing Reveals Clearance of Blastula Chromosomal Mosaicism in In Vitro Fertilization Babies"
      author: "Gao, Y.†, Zhang, J.†, <b>Liu, Z.</b>†, Qi, S.†, Guo, X., Wang, H., Cheng, Y., Tian, S., Ma, M., Peng, H., Wen, L., Tang, F.&#42;, Yao, Y.&#42"
      info: "<i>Genomics, Proteomics & Bioinformatics</i>, 2022"
      url: "https://doi.org/10.1016/j.gpb.2022.07.004"
      pdf: "/assets/publication/1-s2.0-S1672022922000882-main.pdf"
---
