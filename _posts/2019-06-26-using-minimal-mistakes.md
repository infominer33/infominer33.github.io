---
layout: single
title:  "Contributors Guide: Using Minimal Mistakes"
description: "Contributing to the InfoHub via GitHub, Jekyll and Minimal Mistakes."
excerpt: >
  This guide will introduce you to how some of these sites operate, to encourage participation. You are presented with an overview of how I'm using Minimal Mistakes, and Publishing Content for Free via GitHub Pages.
header:
  image: https://imgur.com/xeWd7Zz.png
  teaser: https://infominer.id/assets/img/minimal-mistakes-teaser.png
  og_image: https://infominer.id/assets/img/minimal-mistakes-teaser.png
  caption: "Minimal Mistakes Setup and [Quick-Start](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)."
tags: 
  - INFOHUB
  - PUBLIC-DOMAIN
  - OPEN-SOURCE
  - SOURCECRYPTO
  - DECENTRALIZED-ID
  - JEKYLL
  - CSS
  - JAVASCRIPT
  - CONFIGURATION
  - MINIMAL-MISTAKES
  - SETUP
  - GITHUB-PAGES
  - WEB-WORK
toc_sticky: false
classes: wide
#authors: 
#  - "<a href='https://infominer.id'>Infominer</a>"
#  - "<a href='https://www.caballerojuan.com'>JuanSC</a>"
permalink: using-minimal-mistakes/
categories: [InfoHub, SourceCrypto, Web-Work-Tools, DIDecentral, Learn-Crypto-Trading, Contributors-Guide]
published: true
last_modified_at: 2019-06-25T11:22:33-23:00
---

## Using Minimal Mistakes

Each site is set up a little different, and will have its own version of this post, eventually.

More info on using GitHub Pages, and Minimal Mistakes.

* [github-pages-starter-pack/#minimal-mistakes](https://web-work.tools/github-pages-starter-pack/#minimal-mistakes)

If you peruse the resource linked above, you'll find there are a number of integrations and potential use-cases that I've yet to explore, practically speaking.

## [infominer33/infominer33.github.io](https://github.com/infominer33/infominer33.github.io)

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

So, I'm not 100% but it seems that we have some default fonts installed, based upon the most popularly supported?

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


### _config.yml

This is the configuration file for Infominer.id.

Every site using Jekyll must have a `_config.yml`.


<script src="https://gist.github.com/infominer33/infominer33.github.io/raw/master/_config.yml"></script>


### Gemfile

These Gem settings are necessary to build the site locally, when testing larger changes.

<script src="https://gist.github.com/infominer33/infominer33.github.io/raw/master/Gemfile"></script>


## Content

### Posts

Posts are the blog posts... straight-forward enough.

You might recall from earlier, but there were default settings for posts in the config.

```yaml
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

```yaml
---
layout: single # this is the layout I always use, except in special cases.
title:  "Contributors Guide: How I use Minimal Mistakes - 2019"
description: "Contributing to the InfoHub via GitHub Pages, Jekyll and Minimal Mistakes."
excerpt: >
  This guide will introduce you to how some of these sites operate, to encourage participation. You are presented with an overview of how I'm using Minimal Mistakes, and Publishing Content for Free via GitHub Pages.
```

The `excerpt` is what social media uses in the preview, when sharing... and it also is used in the blog feed for preview text.


```yaml
header:
  teaser: https://imgur.com/xeWd7Zz.png
  image: https://infominer.id/assets/img/minimal-mistakes-teaser.png
  caption: "Minimal Mistakes Setup and [Quick-Start](https://mmistakes.github.io/minimal-mistakes/docs/quick-start-guide/)."
```

The `teaser` image is used in the blog feed, and for related posts.
`image` is for the header image. `og_image` may be optionally used, if you want a different social media image than your header image.

The only way to have a uniform capitalization guide I could live with is to capitalize all tags, and capitalize categories as would be officially recognized, or simply first letter capital.

```yaml
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

## Responsive Video Embeds

* [minimal-mistakes/docs/helpers/#responsive-video-embed](https://mmistakes.github.io/minimal-mistakes/docs/helpers/#responsive-video-embed)

I primarily use the youtube video helper. 

```liquid
{% raw %}{% include video id="XsxDH4HcOWA" provider="youtube" %}{% endraw %}
```

```liquid
{% raw %}{% include video id="212731897" provider="vimeo" %}{% endraw %}
```

```liquid
{% raw %}{% include video id="1u41lIbMLbV53PvMbyYc9HzvBug5lNWaO" provider="google-drive" %}{% endraw %}
```

You could also introduce a video header, if you have a high quality video.

### Header Video - Front Matter

```yaml
header:
  video:
    id: 212731897
    provider: google-drive
```

## Embed Gist or GitHub Files

`<script src="https://gist.github.com/infominer33/infominer33.github.io/raw/master/Gemfile"></script>`

I'm using this line of code to embed files.


## Syntax Highlighting

![](https://imgur.com/46fWL5t.png)

* [jekyllrb.com/docs/liquid/tags/#code-snippet-highlighting](https://jekyllrb.com/docs/liquid/tags/#code-snippet-highlighting)
* [minimal-mistakes/markup-syntax-highlighting/](https://mmistakes.github.io/minimal-mistakes/markup-syntax-highlighting/)
  * [help.github.com / creating-and-highlighting-code-blocks](https://help.github.com/en/articles/creating-and-highlighting-code-blocks)


In this document I'm highlighting code syntax, and for certain code, the codeblock markdown doesn't work unless you indicate the syntax.

![](https://imgur.com/uIw9IqD.png)

### Raw Liquid Code-Blocks

![](https://imgur.com/Gn2RWmN.png)


## Featured Posts

This technique can be used to introduce feature rows or individual feature images in any post or layout. In fact, an entire page could be built with just these settings.

You may include these variables:

>* `image_path` - Required - Full path to image eg: /assets/images/filename.jpg. Use absolute URLS for those hosted externally.
>* `image_caption` - Optional - Caption for image, Markdown is supported eg: `“Image from Unsplash”
>* `alt` - Optional - Alternate text for image.
>* `title` - Optional - Content block title.
>* `excerpt` - Optional - Content block excerpt text. Markdown is allowed.
>* `url` - Optional - URL that the button should link to.
>* `btn_label` - Optional - Button text label. 	more_label in UI Text data file.
>* `btn_class` - Optional - Button style. See [utility classes](https://mmistakes.github.io/minimal-mistakes/docs/utility-classes/) for options.


More information: [minimal-mistakes/docs/helpers/#feature-row](https://mmistakes.github.io/minimal-mistakes/docs/helpers/#feature-row)

### [infominer33.github.io/index.html](https://github.com/infominer33/infominer33.github.io/blob/master/index.html)


Frontmatter for feature images:

```yaml
intro:
  - image_path: https://infominer.id/assets/img/infohub-contributors-thumb.png
    alt: "Contributors Guide"
    title: "Contributors Guide: Introduction"
    excerpt: "This contributors introduction is to encourage participation, with minimal barriar to entry. Quickstart for [GitHub](https://github.com/infominer33), [Twitter](https://twitter.com/SourceCrypto), and [Discord](https://discord.gg/29mZwPQ) Contributions."
    url: "/contributors-intro/"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row:
  - image_path: "https://sourcecrypto.pub/bitcoin-history/assets/img/elems10.png"
    alt: "erights.org - CapTP Ops: provideFor() ‘98"
    title: "Bitcoin History - Smart Contracts"
    excerpt: "From Szabo and E Lang - to Ethereum, the DAO, Smart Signatures, and the Cambrian Explosion."
    url: "https://sourcecrypto.pub/bitcoin-history/smart-contracts/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: "https://sourcecrypto.pub/images/thecryptoconomy-podcast_guy-swann.png"
    alt: "Down the @TheCryptoconomy Rabbithole"
    title: "Guy Swan - @TheCryptoconomy Essential Episods"
    excerpt: "Audio for Hundreds of Essential Bitcoin Articles. @TheCryptoconomy - Guy Swan..... These Podcasts are essential. So I made an index of them, organized by topic."
    url: "https://sourcecrypto.pub/blog/thecryptoconomy-podcast-deep-dive/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: "https://web-work.tools/images/github-pages.jpeg"
    alt: "GHPages Starter Pack"
    title: "GitHub Pages Starter Pack"
    excerpt: "Publishing a Website via GitHub pages is free, and easy. Everything you need to get going in one place + extended resources."
    url: "https://web-work.tools/github-pages-starter-pack/"
    btn_label: "Read More"
    btn_class: "btn--primary"
feature_row2:
  - image_path: "https://web-work.tools/images/pgp-og.png"
    alt: "cypherpunk essentials"
    title: "Using PGP, Escrow, and Cryptocurrency Keysignatures"
    excerpt: "Asymmetric Encryption: Phil Zimmerman, PGP, Bitcoin and Ethereum key-signatures, Escrow, SSL, Various Apps and Resourses."
    url: "https://web-work.tools/practical-public-key-crypto/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: "https://sourcecrypto.pub/rare-digital-art/img/Salvador-Pepe-rare-Pepe-auction-1-13-18.jpeg"
    alt: "Digital Rare"
    title: "Rare Pepe - Bitcoin History"
    excerpt: "Starting in October 2014, users on the /r9k/ (robot9000) board on 4chan began referring to original illustrations and photoshops of Pepe the Frog as 'Rare Pepes'; sharing the 'rare' images of Pepe as if they were trading cards, some of which were posted with watermarks to retain their value."
    url: "https://sourcecrypto.pub/bitcoin-history/rare-pepe/"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: "https://web-work.tools/images/content-creation.png"
    alt: "Resources for Content Creation"
    title: "Resources for Content Creation"
    excerpt: "All kinda tools for images and editing and handy stuff to assist with content creation."
    url: "https://web-work.tools/content-creation/"
    btn_label: "Read More"
btn_class: "btn--primary"
```

### Home Layout

You can see in this markup exactly how my home-page is generated:

<script src="https://gist.github.com/infominer33/infominer33.github.io/raw/master/_layouts/home.html"></script>



## Social Share

I modified this to include the 'Edit this page' button, and some cryptocurrency addresses.


<script src="https://gist.github.com/infominer33/infominer33.github.io/raw/master/_includes/social-share.html"></script>


## Thank You for Stopping By

conclusion soon