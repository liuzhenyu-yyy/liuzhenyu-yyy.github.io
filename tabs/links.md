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
    header: "Links"
    info: "Some links to other websites that might be useful."

  # To change order of the Categories, simply change order. (you don't need to change list order.)
  category:
    - title: "Publication"
      type: id_publication
      color: "#8dd3c7"
    - title: "Affiliation"
      type: id_affiliation
      color: "#80b1d3"
    - title: "Others"
      type: id_others
      color: "#cccccc"

  list:
    -
    # Publication
    - type: id_publication
      title: "Cell Discovery"
      url: "https://www.nature.com/articles/s41421-022-00500-4"
      info: "High-throughput and high-sensitivity full-length single-cell RNA-seq analysis on third-generation sequencing platform. PMID: 36631434"
    - type: id_publication
      title: "Genomics, Proteomics & Bioinformatics"
      url: "https://www.sciencedirect.com/science/article/pii/S1672022922000882"
      info: "Single-cell sequencing reveals clearance of blastula chromosomal mosaicism in In Vitro fertilization babies. PMID: 35944838"

    # Affiliation
    - type: id_affiliation
      title: "BIOPIC"
      url: "https://biopic.pku.edu.cn/en/"
      info: "Biomedical Pioneering Innovation Centre (BIOPIC), Peking University, where our laboratory is located."
    - type: id_affiliation
      title: "School of Life Sciences"
      url: "http://bio.pku.edu.cn/"
      info: "School of Life Sciences, Peking University, where I get my Ph.D. training."
    - type: id_affiliation
      title: "Yuanpei College"
      url: "https://yuanpei.pku.edu.cn/"
      info: "Yuanpei College, Peking University, where I spent my undergraduate career."
    - type: id_affiliation
      title: "Peking University"
      url: "https://english.pku.edu.cn/"
      info: "Peking University is a public research university in Beijing, China. The university is funded by the Ministry of Education."

    # Others
    - type: id_others
      title: "TangLab Quota"
      url: "https://liuzhenyu-yyy.shinyapps.io/tanglab_quota/"
      info: "A shiny app to visualize quota usage for each user from Tang Lab on PKUHPC."
---
