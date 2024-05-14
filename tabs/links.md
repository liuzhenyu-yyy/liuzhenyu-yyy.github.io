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
    info: "Publications I've co-authored, grouped by areas of research. Click for more information."

  # To change order of the Categories, simply change order. (you don't need to change list order.)
  category:
    - title: "Cancer Biology"
      type: id_cancer
      color: "#8dd3c7"
    - title: "Methodology"
      type: id_method
      color: "#80b1d3"
    - title: "Others"
      type: id_others
      color: "#cccccc"

  list:
    -
    # Cancer
    - type: id_cancer
      title: "CRC scATAC-seq"
      url: "https://aacrjournals.org/cancerdiscovery/article-abstract/doi/10.1158/2159-8290.CD-23-1445/735072/Single-cell-chromatin-accessibility-analysis"
      info: "<u><b>Liu, Z.</b>, Hu, Y., Xie, H., Chen, K.</u>, Wen, L., Fu, W., Zhou, X., and Tang, F. (2024). Single-cell chromatin accessibility analysis reveals the epigenetic basis and signature transcription factors for the molecular subtypes of colorectal cancers. <i>Cancer Discov.</i> 10.1158/2159-8290.CD-23-1445."

    # Methodology
    - type: id_method
      title: "SCAN-seq2"
      url: "https://www.nature.com/articles/s41421-022-00500-4"
      info: "<u>Liao, Y., <b>Liu, Z.</b>, Zhang, Y.</u>, Lu, P., Wen, L., and Tang, F. (2023). High-throughput and high-sensitivity full-length single-cell RNA-seq analysis on third-generation sequencing platform. <i>Cell Discov.</i> 9, 5. 10.1038/s41421-022-00500-4."

    # Others
    - type: id_others
      title: "IVF embryo CNV"
      url: "https://academic.oup.com/gpb/article/20/6/1224/7274159"
      info: "<u>Gao, Y., Zhang, J., <b>Liu, Z.</b>, Qi, S.</u>, Guo, X., Wang, H., Cheng, Y., Tian, S., Ma, M., Peng, H., et al. (2022). Single-cell Sequencing Reveals Clearance of Blastula Chromosomal Mosaicism in In Vitro Fertilization Babies. <i>Genomics Proteomics Bioinformatics</i> 20, 1224-1231. 10.1016/j.gpb.2022.07.004."
---
