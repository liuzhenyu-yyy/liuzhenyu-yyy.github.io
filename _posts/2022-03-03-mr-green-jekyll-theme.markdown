---
# multilingual page pair id, this must pair with translations of this page. (This name must be unique)
lng_pair: id_Mr_Green_Jekyll_Theme
title: Mr. Green Jekyll Theme

# post specific
# if not specified, .name will be used from _data/owner/[language].yml
author: Mr. Green's Workshop
# multiple category is not supported
category: jekyll
# multiple tag entries are possible
tags: [jekyll, new feature]
# thumbnail image for post
img: ":mock1.jpg"
# disable comments on this page
#comments_disable: true

# publish date
date: 2022-03-03 12:32:10 +0900

# seo
# if not specified, date will be used.
#meta_modify_date: 2022-03-03 12:32:10 +0900
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
published: false
---


### Introduction

<!-- outline-start -->

[Mr. Green](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme) is a multilingual theme generated with [Jekyll](https://jekyllrb.com/) and fully compatible with [GitHub Pages](https://pages.github.com/).

<!-- outline-end -->

I was going to make my website and thought if I did it as a template, I could share it with the open source community. That's why I decided to build it as a theme. I've worked so hard to make this possible so I'm happy if you consider [supporting me](#you-can-support-my-work). Thanks.

### Features

- Multilingual web site
  - English (default), Japanese, Brazilian Portuguese
- Recommended language offer feature
- Auto Navigation Button adder with icon enable disable options
- Layouts for `Home`, `About`, `Archives`, `Post-list`, `Links`, `Projects` and more
- Color scheme switching options (Dark light)
- Auto Contact option adder
- Auto image referrer (no need to add full path for images. Just add `:` in front of it.)
- image lazy loader, image viewer
- Cool Footer with creative commons licensing
- Movable Table of Contents modal box for Posts
- Post Share Options
- Post-listing by Category or Tags
- Comments for posts
  - [Disqus](https://disqus.com)
- Selectable numbered pagination or scroll to load type
- Sitemap feature
- Search Engine Optimization (SEO)
  - [Schema Markup](https://schema.org)
  - [Open Graph](https://ogp.me/)
  - [Twitter](https://developer.twitter.com/en/docs/twitter-for-websites/cards/overview/summary)
- Analytics (Google Analytics)
- Cookie consent feature
- Site Search feature
- Code Compression for small footprint (`HTML` `JS` `SCSS`)
- Mobile App support
- Mobile device friendly (Tested on Android and IOS)
- Well organized folder structure for developers (Tested on Chrome, Safari, FireFox)

### Installation

#### Github pages

1. [Fork the repo](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/fork).
1. Edit \_config.yml and change `url` like below and push changes.

   ```yaml
   url: "https://your_github_user_name.github.io"
   ```

1. Rename the repo name to `your_github_user_name.github.io`
1. Check Deploy status `Actions` tab on the repo.
1. When it's turned to green, your site is up and running at `https://your_github_user_name.github.io`

#### Local build

1. [Install Jekyll](https://jekyllrb.com/docs/installation/) to your OS
1. Clone or [download](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/releases/latest) the repo, in command prompt go to the folder run `bundle install` command
1. Build using `bundle exec jekyll serve --watch --host 0.0.0.0 --safe` command
    - with `--host 0.0.0.0` parameter you can access web server from same lan.
    - with `--safe` parameter you can make sure no 3rd party plugin added. (for Github pages development)
1. Your page will be up and running at the `0.0.0.0:4000/` address.

### Documentation

Check out [Mr. Green theme tutorials playlist](https://www.youtube.com/playlist?list=PLAymxPbYHgl-fFy5can7uZBMJtFWVcphD) on YouTube

### Credits

I want to thank these projects that gave me an opportunity to build my web site.

- [Jekyll](https://jekyllrb.com/) is a static site generator. It takes text written in your favorite markup language and uses layouts to create a static website. You can tweak the site’s look and feel, URLs, the data displayed on the page, and more. It is a wonderful project which is maintained by volunteers.

- [GitHub Pages](https://pages.github.com/) Hosted directly from your GitHub repository. Just push the changes and the site will be automatically generated.

Some of the sites that I find useful while I'm working on this project. [links page](https://jekyll-theme-mrgreen-demo.mrgreensworkshop.com/tabs/links.html)

### You Can Support My Work

Creating projects starting from nothing takes a great amount of time. Much appreciated if you consider supporting me so that I can continue projects like this and creating new contents for everyone.

- You can support me on [GitHub Sponsors](https://github.com/sponsors/MrGreensWorkshop "Support me on GitHub Sponsors") (monthly or one time)
- You can be one of my patrons on [Patreon](https://patreon.com/MrGreensWorkshop "Be my Patron") (monthly)
- You can tip me via [Ko-fi](https://ko-fi.com/MrGreensWorkshop "Tip Me via Ko-fi") (one time)

### Contribute

Pull Requests are welcome. Please check the instructions in the Issues and Pull Request templates.

### Contributors

Thank you for your contributions!

- Brazilian Portuguese translation by [Vitor DallAcqua](https://github.com/fandangos).

### License

As it says in the [MIT license](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/LICENSE.txt), you can use this theme anywhere as long as you include the license and copyright notice.

`Copyright (c) 2022 Mr. Green's Workshop https://www.MrGreensWorkshop.com`

Please add link to my page or leave the "Pwrd by Mr. Green" link in the footer so I can get credit for my work.

Thank you!

### Other Licenses

Mr. Green Jekyll Theme incorporates libraries written below. Without these libraries, I couldn't make this project possible.

| Library                              | file |
| :----------------------------------- | ---- |
| [jQuery v3.6.0](https://github.com/jquery/jquery/tree/3.6.0), Copyright [OpenJS Foundation](https://openjsf.org) and other contributors. jQuery is distributed under the terms of the MIT License. | [jquery-3.6.0.min.js](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/assets/js/jquery-3.6.0.min.js) |
| [Bootstrap v3.3.7](https://github.com/twbs/bootstrap/tree/v3.3.7), Copyright (c) 2011-2016 Twitter, Inc. Bootstrap is distributed under the terms of the MIT License. | [bootstrap.min.js](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/assets/js/bootstrap.min.js), [bootstrap.min.css](assets/css/bootstrap.min.css) |
| [Bootstrap Table of Contents v0.4.1](https://github.com/afeld/bootstrap-toc/tree/v0.4.1), Copyright (c) 2015 Aidan Feldman Aidan Feldman. Bootstrap Table of Contents is distributed under the terms of the MIT License. | [bootstrap-toc.min.js](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/assets/js/bootstrap-toc.min.js), [bootstrap-toc.min.css](assets/css/bootstrap-toc.min.css) |
| [Font Awesome v4.7.0](https://github.com/FortAwesome/Font-Awesome/tree/v4.7.0), Copyright (c) 2017 Dave Gandy. The Font Awesome font is distributed under the terms of the [SIL OFL 1.1](http://scripts.sil.org/OFL). Font Awesome CSS, LESS, and Sass files are distributed under the terms of the [MIT License](https://opensource.org/licenses/mit-license.html). | [font-awesome.min.css](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/assets/css/font-awesome.min.css), [FontAwesome](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/assets/fonts/) |
| [Lozad.js v1.16.0](https://github.com/ApoorvSaxena/lozad.js/tree/v1.16.0), Copyright (c) 2017 Apoorv Saxena. Lozad.js is distributed under the terms of the MIT License. | [lozad.min.js](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/assets/js/lozad.min.js) |
| [Magnific Popup v1.1.0](https://github.com/dimsemenov/Magnific-Popup/tree/1.1.0), Copyright (c) 2014-2016 Dmitry Semenov, http://dimsemenov.com. Magnific Popup is distributed under the terms of the MIT License. | [jquery.magnific-popup.min.js](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/assets/js/jquery.magnific-popup.min.js), [magnific-popup.css](assets/css/magnific-popup.css) |
| [Simple-Jekyll-Search v1.9.2](https://github.com/christian-fei/Simple-Jekyll-Search/tree/v1.9.2), Copyright (c) 2015 Christian Fei. Simple-Jekyll-Search is distributed under the terms of the MIT License. | [simple-jekyll-search-1.9.2.min.js](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/assets/js/simple-jekyll-search-1.9.2.min.js) |
| [Compress HTML in Jekyll v3.1.0](https://github.com/penibelst/jekyll-compress-html/tree/v3.1.0), Copyright (c) 2014 Anatol Broder. Compress HTML in Jekyll is distributed under the terms of the MIT License. | [compress.liquid](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme/blob/main/_layouts/util/compress.liquid) |

[Mr. Green Jekyll Theme](https://github.com/MrGreensWorkshop/MrGreen-JekyllTheme)

### Other Licenses

test