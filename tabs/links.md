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
    info: "Marks: co-first author†, corresponding author<sup>*<\sup>."

  # To change order of the Categories, simply change order. (you don't need to change list order.)
  category:
    - title: "Research article"
      type: id_aritcle
      color: "#8dd3c7"

  list:
    -
    # Research article
    - type: id_aritcle
      title: "https://doi.org/10.1158/2159-8290.CD-23-1445"
      url: "https://doi.org/10.1158/2159-8290.CD-23-1445"
      info: "<b>Liu, Z.</b>†, Hu, Y.†, Xie, H.†, Chen, K.†, Wen, L., Fu, W., Zhou, X.<sup>*</sup>, Tang, F.<sup>*</sup>, 2024. Single-Cell Chromatin Accessibility Analysis Reveals the Epigenetic Basis and Signature Transcription Factors for the Molecular Subtypes of Colorectal Cancers. <i>Cancer Discovery</i> OF1–OF24."

    - type: id_aritcle
      title: "/assets/publication/s41421-022-00500-4.pdf"
      url: "https://doi.org/10.1038/s41421-022-00500-4"
      info: "Liao, Y.†, <b>Liu, Z.</b>†, Zhang, Y.†, Lu, P., Wen, L., Tang, F.<sup>*</sup>, 2023. High-throughput and high-sensitivity full-length single-cell RNA-seq analysis on third-generation sequencing platform. <i>Cell Discovery</i> 9, 5."

    # Others
    - type: id_aritcle
      title: "/assets/publication/1-s2.0-S1672022922000882-main.pdf"
      url: "https://doi.org/10.1016/j.gpb.2022.07.004"
      info: "Gao, Y.†, Zhang, J.†, <b>Liu, Z.</b>†, Qi, S.†, Guo, X., Wang, H., Cheng, Y., Tian, S., Ma, M., Peng, H., Wen, L., Tang, F.<sup>*</sup>, Yao, Y.<sup>*</sup>, 2022. Single-cell Sequencing Reveals Clearance of Blastula Chromosomal Mosaicism in In Vitro Fertilization Babies. <i>Genomics, Proteomics & Bioinformatics</i> 20, 1224–1231."
---
