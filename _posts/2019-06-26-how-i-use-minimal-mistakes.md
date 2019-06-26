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
permalink: how-i-use-minmal-mistakes/
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

### CSS - Stylesheets

At the moment, I'm quite CSS agnostic. One things at a time.. However, you might be interested in working on it. This is how the sytlesheets are named \ organized.

* [mmistakes.github.io/minimal-mistakes/docs/stylesheets/](https://mmistakes.github.io/minimal-mistakes/docs/stylesheets/)
The theme’s assets/css/main.css file is built from several SCSS partials located in _sass/ and is structured as follows:

```

minimal-mistakes
├── _sass
|  └── minimal-mistakes
|     ├── vendor               # vendor SCSS partials
|     |   ├── breakpoint       # media query mixins
|     |   ├── magnific-popup   # Magnific Popup lightbox
|     |   └── susy             # Susy grid system
|     ├── _animations.scss     # animations
|     ├── _archive.scss        # archives (list, grid, feature views)
|     ├── _base.scss           # base HTML elements
|     ├── _buttons.scss        # buttons
|     ├── _footer.scss         # footer
|     ├── _masthead.scss       # masthead
|     ├── _mixins.scss         # mixins (em function, clearfix)
|     ├── _navigation.scss     # nav links (breadcrumb, priority+, toc, pagination, etc.)
|     ├── _notices.scss        # notices
|     ├── _page.scss           # pages
|     ├── _print.scss          # print styles
|     ├── _reset.scss          # reset
|     ├── _sidebar.scss        # sidebar
|     ├── _syntax.scss         # syntax highlighting
|     ├── _tables.scss         # tables
|     ├── _utilities.scss      # utility classes (text/image alignment)
|     └── _variables.scss      # theme defaults (fonts, colors, etc.)
├── assets
|  ├── css
|  |  └── main.scss            # main stylesheet, loads SCSS partials in _sass


```

>To make basic tweaks to theme’s style Sass variables can be overridden by adding to `<your_project>/assets/css/main.scss`. For instance, to change the link color used throughout the theme add:

```
$link-color: red;
```

I've done nothing about fonts](https://www.smashingmagazine.com/2015/11/using-system-ui-fonts-practical-guide/) yet, but I mean to.

* [smashingmagazine.com/2015/11/using-system-ui-fonts-practical-guide](https://www.smashingmagazine.com/2015/11/using-system-ui-fonts-practical-guide/)
* [web.archive.org - medium.com/designing-medium/system-shock-6b1dc6d6596f](https://web.archive.org/web/20160209004426/https://medium.com/designing-medium/system-shock-6b1dc6d6596f)
  >The obvious way to use system fonts in CSS is to… just list all of the ones you can imagine by name:
  >
  >font-family: "San Francisco", "Roboto", "Segoe UI";
  >
  >(The way CSS works, if the first font is not present, the second one will be tried, and so on. Since it’s not common for an operating system to have more than one of these fonts installed, only one will be selected.)
  >
  >We also need to take care of the older systems, including a fallback to use a generic sans serif font if nothing matches before:
  >
  >font-family: "San Francisco", "Roboto", "Segoe UI", "Helvetica Neue", "Lucida Grande", sans-serif;
  >

So, I'm not 100% but it seems that we have some default themes installed, based upon the most popularly supported?

### JavaScript

* [mmistakes.github.io/minimal-mistakes/docs/javascript/](https://mmistakes.github.io/minimal-mistakes/docs/javascript/)

```
minimal mistakes
├── assets
|  ├── js
|  |  ├── plugins
|  |  |   ├── gumshoe.js                     # simple scrollspy
|  |  |   ├── jquery.ba-throttle-debounce.js # rate-limit functions
|  |  |   ├── jquery.fitvids.js              # fluid width video embeds
|  |  |   ├── jquery.greedy-navigation.js    # priority plus navigation
|  |  |   ├── jquery.magnific-popup.js       # responsive lightbox
|  |  |   └── smooth-scroll.js               # make same-page links scroll smoothly
|  |  ├── vendor
|  |  |   └── jquery
|  |  |       └── jquery-3.4.1.js
|  |  ├── _main.js                           # jQuery plugin settings and other scripts
|  |  └── main.min.js                        # concatenated and minified theme script
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

### [Gemfile](https://github.com/infominer33/infominer33.github.io/blob/master/Gemfile)

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



## Content

For now, all we need to worry about is posts and pages.

### Posts

Posts are the blog posts... straight-forward enough.

You might recall from earlier, but there were default settings for posts in the config.

### Defaults
```
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

I'll be honest, I haven't intentionally set up defaults for posts and pages... I've mostly been doing everything manually. Eventually I'll go through and clean all that up so the default settings are default, and there are minimal manual settings in the frontmatter.

### Front Matter

I'll use this post as an example, and give a more detailed explanation here, where you are most likely to need one, should you decide to contribute a 'finished' piece of content.

**Every Post or Page must have front matter.** Without front-matter, jekyll won't read it. That's why you might see empty front-matter in some of the source files.

```
---
layout: single # this is the layout I always use, except in special cases.
title:  "Contributors Guide: How I use Minimal Mistakes - 2019"
description: "Contributing to the InfoHub via GitHub Pages, Jekyll and Minimal Mistakes."
excerpt: >
  This guide will introduce you to how some of these sites operate, to encourage participation. You are presented with an overview of how I'm using Minimal Mistakes, and Publishing Content for Free via GitHub Pages.
```

The `excerpt` is what social media uses in the preview, when sharing... and it also is used in the blog feed for preview text.


```
header:
  teaser: https://imgur.com/xeWd7Zz.png
  image: https://infominer.id/assets/img/minimal-mistakes-teaser.png
  caption: "Minimal Mistakes Setup and [Quick-Start](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)."
```
The `teaser` image is used in the blog feed, and for related posts.
`image` is for the header image. `og_image` may be optionally used, if you want a different social media image than your header image.

The only way to have a uniform capitalization guide I could live with is to capitalize all tags, and capitalize categories as would be officially recognized, or simply first letter capital.

```
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
permalink: how-i-use-minmal-mistakes/
categories: [InfoHub, SourceCrypto, Web-Work-Tools, DIDecentral, Learn-Crypto-Trading]
published: true
last_modified_at: 2019-06-25T11:22:33-23:00
---
```

If you edit an existing post, you can add your name in the authors front matter like i've done here.  Permalink is the way I decide which is the official link, and I set canonical once I feel good about the name structure.

### Featured Posts

.... coming soon! how to add content as the featured post above or below the blogfeed.