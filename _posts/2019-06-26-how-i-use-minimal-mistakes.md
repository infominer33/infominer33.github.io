---
layout: single
title:  "Contributors Guide: How I use Minimal Mistakes - 2019"
description: "Contributing to the InfoHub via GitHub Pages, Jekyll and Minimal Mistakes."
excerpt: >
  This guide will introduce you to how some of these sites operate, to encourage participation. You are presented with an overview of how I'm using Minimal Mistakes, and Publishing Content for Free via GitHub Pages.
header:
  teaser: https://imgur.com/xeWd7Zz.png
  image: https://infominer.id/assets/img/minimal-mistakes-teaser.png
  caption: "Minimal Mistakes Setup and [Quick-Start](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)."
tags: 
  - INFOHUB
  - CONTRIBUTORS-GUIDE
  - PUBLIC-DOMAIN
  - OPEN-SOURCE
  - SOURCECRYPTO
  - DECENTRALIZED-ID
  - JEKYLL
  - MINIMAL-MISTAKES
  - SETUP
  - GITHUB-PAGES
  - WEB-WORK
authors: 
  - "<a href='https://infominer.id'>Infominer</a>"
  - "<a href='https://www.caballerojuan.com'>JuanSC</a>"
permalink: using-minimal-mistakes-config/
categories: [InfoHub, SourceCrypto, Web-Work-Tools, DIDecentral, Learn-Crypto-Trading]
published: true
last_modified_at: 2019-06-25T11:22:33-23:00
---

## [github.com/infominer33/infominer33.github.io](https://github.com/infominer33/infominer33.github.io)

![](https://imgur.com/iOb9STH.png)


## Directory Structure

```
minimal-mistakes
├── _data                      # data files for customizing the theme
|  ├── navigation.yml          # main navigation links
|  └── ui-text.yml             # text used throughout the theme's UI
├── _includes
|  ├── analytics-providers     # snippets for analytics (Google and custom)
|  ├── comments-providers      # snippets for comments
|  ├── footer                  # custom snippets to add to site footer
|  ├── head                    # custom snippets to add to site head
|  ├── feature_row             # feature row helper
|  ├── gallery                 # image gallery helper
|  ├── group-by-array          # group by array helper for archives
|  ├── nav_list                # navigation list helper
|  ├── toc                     # table of contents helper
|  └── ...
├── _layouts
|  ├── archive-taxonomy.html   # tag/category archive for Jekyll Archives plugin
|  ├── archive.html            # archive base
|  ├── categories.html         # archive listing posts grouped by category
|  ├── category.html           # archive listing posts grouped by specific category
|  ├── collection.html         # archive listing documents in a specific collection
|  ├── compress.html           # compresses HTML in pure Liquid
|  ├── default.html            # base for all other layouts
|  ├── home.html               # home page
|  ├── posts.html              # archive listing posts grouped by year
|  ├── search.html             # search page
|  ├── single.html             # single document (post/page/etc)
|  ├── tag.html                # archive listing posts grouped by specific tag
|  ├── tags.html               # archive listing posts grouped by tags
|  └── splash.html             # splash page
├── _sass                      # SCSS partials
├── assets
|  ├── css
|  |  └── main.scss            # main stylesheet, loads SCSS partials from _sass
|  ├── images                  # image assets for posts/pages/collections/etc.
|  ├── js
|  |  ├── plugins              # jQuery plugins
|  |  ├── vendor               # vendor scripts
|  |  ├── _main.js             # plugin settings and other scripts to load after jQuery
|  |  └── main.min.js          # optimized and concatenated script file loaded before </body>
├── _config.yml                # site configuration
├── Gemfile                    # gem file dependencies
├── index.html                 # paginated home page showing recent posts
└── package.json               # NPM build scripts
```


## Configuration

This will be most useful if you decide to clone and work on the theme locally. I have cloned the minimal mistakes theme, and am running it directly via jekyll. I have not used the remote theme or the gem-based theme method, for this particular repository.

These _config.yml and Gem settings ar particular to that method. You should even be able to copy all the files from the minimal mistakes to your own empty repository, and noticing my configuration settings be able to create your own site. However, [Minimal Mistakes Quickstart Guide](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/) is quite adequate to the task.

This guide is designed to familiarize those interested in contributing to the InfoHub, so that you may see how it is put together.


### [_config.yml](https://github.com/infominer33/infominer33.github.io/blob/master/_config.yml)

```
# Review documentation to determine if you should use `theme` or `remote_theme`
# https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/#installing-the-theme

# I'm using Neither, since this is a copy of the entire theme, and relies only on Jekyll to build, using remote or gem-based keeps your files up to date if you're not customizing most of them.
# theme                  : "minimal-mistakes-jekyll"
# remote_theme           : "mmistakes/minimal-mistakes"

minimal_mistakes_skin    : "mint" # "air", "aqua", "contrast", "dark", "dirt", "neon", "mint", "plum", "sunrise"

# Site Settings
locale                   : "en-US"
title                    : "InfoHub"
title_separator          : "|"
name                     : "⧉ Infominer"
description              : "Infominer on Bitcoin History, Self-Sovereign Identity, Blockchain Development and other Web Technologies."
url                      : "https://infominer.id"
baseurl                  : ''
repository               : "infominer33/infominer33.github.io"
github                   : [metadata]
teaser                   : "/assets/img/info-og.png"
logo                     : "/assets/icons/android-chrome-512x512.png"
masthead_title           : "Research Driven Content"
words_per_minute         : 200
search                   : true
search_provider          : lunr 
search_full_content      : false # note! This is important. setting to True will jakc up your site unless it is small.


# Social Sharing
twitter:
  username               : "infominer33"
#  title                  : "DIDecentral ⧉ Identity Decentralized"
#  description            : "Resources for Creating a Vendor Agnostic, User-Controlled, Identity Layer for the Internet."
#  image                  : "https://decentralized-id.com/images/IDecentralized.png"
#  card                   : "summary_large_image"
  card                   : "summary"

og_image                 : "https://infominer.id/assets/img/info-og.png"

# Analytics
analytics:
  provider               : google # false (default), "google", "google-universal", "custom"
  google:
    tracking_id          : UA-132558656-1
    anonymize_ip         : true

# Site Author
author:
  name             : "Infominer"
  avatar           : "https://i.imgur.com/S1UmInX.gif"
  #"/assets/img/infullminer.png"
#  bio              : 
#  location         : "I spend most of my time right here."
#  email            : infominer@protonmail.com
  links:
    - label: "Email"
      icon: "fas fa-fw fa-envelope-square"
      url: "mailto:infominer@protonmail.com"
    - label: "Keybase"
      icon: "fab fa-fw fa-keybase"
      url:  "https://keybase.io/infominer"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/infominer33/"
    - label: "Twitter"
      icon: "fab fa-fw fa-twitter-square"
      url: "https://twitter.com/infominer33"
    - label: "Discord"
      icon: "fab fa-fw fa-discord"
      url: "https://discord.gg/ahTuPMY"
    - label: "Telegram"
      icon: "fab fa-fw fa-telegram"
      url: "https://t.me/InfoMiner33"
   # - label: "Bitcoin"
    #  icon: "fab fa-fw fa-bitcoin"
     # url: 

# Site Footer
footer:
  links:
    - label: "Inf⧉Hub"
      icon: "fa fa-fw fa-cube"
      url: "https://infominer.id"
    - label: "Email"
      icon: "fas fa-fw fa-envelope-square"
      url: "mailto:infominer@protonmail.com"
    - label: "Keybase"
      icon: "fab fa-fw fa-keybase"
      url:  "https://keybase.io/infominer"
    - label: "GitHub"
      icon: "fab fa-fw fa-github"
      url: "https://github.com/infominer33/"
    - label: "Twitter"
      icon: "fab fa-fw fa-twitter-square"
      url: "https://twitter.com/infominer33"
    - label: "Discord"
      icon: "fab fa-fw fa-discord"
      url: "https://discord.gg/ahTuPMY"
    - label: "Telegram"
      icon: "fab fa-fw fa-telegram"
      url: "https://t.me/InfoMiner33"
    
    

# Outputting
permalink: /:categories/:title/ # https://jekyllrb.com/docs/permalinks/
paginate: 9 # amount of posts to show
paginate_path: /page:num/
timezone: # https://en.wikipedia.org/wiki/List_of_tz_database_time_zones


# Plugins (each plugin must be listed in the Gem to work when building locally)
plugins:
  - jekyll-paginate
  - jekyll-sitemap
  - jekyll-gist
  - jekyll-feed
  - jemoji
  - jekyll-include-cache
  - jekyll-optional-front-matter
  - jekyll-readme-index
  - jekyll-redirect-from
  - jekyll-mentions

  
jekyll-mentions:
  base_url: https://twitter.com

# mimic GitHub Pages with --safe
whitelist:
  - jekyll-paginate
  - jekyll-sitemap
  - jekyll-gist
  - jekyll-feed
  - jemoji
  - jekyll-include-cache
  - jekyll-optional-front-matter
  - jekyll-readme-index
  - jekyll-redirect-from
  - jekyll-mentions



# Defaults
defaults:
  # _posts
  - scope:
      path: ""
      type: posts
    values:
      layout: single
      author_profile: true
      read_time: true
      comments: # true
      share: true
      related: true
      sidebar:
        title: "⧉Info⧉"
        nav: "infonav"
      toc: true
      toc_label   : "Contents"
      toc_icon    : "link"
      toc_sticky  : true
```

You'll notice that I have different settings for each web-site, and that [there are more](https://github.com/infominer33/infominer33.github.io/blob/master/_config.yml) that come standard in minimal mistakes, which I have not modified or included here.

Those are the settings I think are most important to show you how I've used them.

### [Gemfile]() 

These Gem settings are necessary to build the site locally, when testing larger changes.

```
source "https://rubygems.org"

gem "github-pages", group: :jekyll_plugins


# If you have any plugins, put them here!
group :jekyll_plugins do
  gem "jekyll-paginate"
  gem "jekyll-sitemap"
  gem "jekyll-gist"
  gem "jekyll-feed"
  gem "jemoji"
  gem "jekyll-include-cache"
  gem "jekyll-target-blank"
  gem "jekyll-optional-front-matter"
  gem "jekyll-readme-index"
  gem "jekyll-redirect-from"
  gem "jekyll-seo-tag"
  gem "jekyll-mentions"
  gem 'jekyll-algolia'
  gem "html-proofer"
end
```
## Directory Structure


## Content

### Posts

You