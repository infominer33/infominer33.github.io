---
title: Notes and Resources—Get Started w GitHub Pages
description: Publishing a Website via GitHub pages is free, and easy. Buy a domain name w Bitcoin (not required) and lets go.
image: "https://infominer.id/images/github-pages.jpeg"
redirect_from:
  - notes.html
  - notes-on-github-pages.html
---

# notes on how to set up a github webpage w jekyll

I like github for its support of open source information exchange, free and easy web-publishing... 

## Introduction


If you know [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) then you can do this. To get started all you need is a repository called `username.github.io`. 

You can have only one page per account, and the repository has to contain your account name. I'm infominer33 on github so my website repository is `infominer33.github.io`.

Now I'm realizing you can also make [web-pages for any of your repositories](https://kbroman.org/simple_site/pages/project_site.html).. 

At the very minimum all you need is a readme.md... but that's if you don't care about link previews and all the little things that make a site feel legit. 

Go into settings and use the theme chooser. In order to set up rich snippets, so your preview image embeds on various platforms, you need to do a little additional configuring.

* create an index.md 

Although pages will build an index.html from your readme.md, pages will not behave as expected if you try to do any configuration or additional optimization with only readme.md.

in that index.md you need to include front matter:

```
---
layout: default
---
```

*\*afaikt - indicating layout only necessary in the main index.md*

of course there are other steps, as explained in the links below, but if you don't do those two steps than you will be sad if you want link previews (rich snippets) when you share your links on various apps and sites.

Minimum effort... you can have a web-page up and running in an hour or so.. 

—[**infominer**](https://infominer.id)

## The basics

### Markdown 

* <a href="https://guides.github.com/features/mastering-markdown/" target="_blank">Mastering Markdown</a>
* <a href="https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet" target="_blank">Markdown Cheet-Sheet</a>


### Github Pages

* <a href="http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/" target="_blank">http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/</a>
* <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-1-Publishing-a-single/ba-p/237" target="_blank">Getting Started with Github Pages - Part 1 - Publishing a single Page</a>
* <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-2-Using-an-official/ba-p/2030" target="_blank">Getting Started with GitHub Pages - Part 2</a>
* <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-3-Local-development-with/ba-p/2292" target="_blank">Getting started with GitHub Pages: Part 3 -- Local development with GitHub Pages</a>
* <a href="https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-4-Customizing-your-Pages/ba-p/4058" target="_blank">Getting started with GitHub Pages: Part 4 -- Customizing your Pages site</a>
* <a href="https://help.github.com/en/articles/adding-jekyll-plugins-to-a-github-pages-site" target="_blank">Adding Jekyll Plugins to a GitHub Pages Site - help.github.com</a>
* <a href="https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll" target="_blank">Setting up You GitHub Pages Site Locally with Jekyll</a>
* <a href="https://github.community/t5/GitHub-Pages/bd-p/pages" target="_blank">GitHub Pages —github.community</a>
* <a href="https://pages.github.com/versions/" target="_blank">https://pages.github.com/versions/</a>
* <a href="https://help.github.com/en/articles/creating-a-custom-404-page-for-your-github-pages-site" target="_blank">Creating Custom 404 page</a>
* <a href="https://help.github.com/en/articles/redirects-on-github-pages" target="_blank">Jekyll Redirect Plugin</a>

### Jekyll

* <a href="https://devhints.io/jekyll" target="_blank">Jekyll - Cheat Sheet</a>
* <a href="https://github.com/jekyll/jekyll/blob/master/README.markdown" target="_blank">/jekyll/jekyll/blob/master/README.markdown</a>
* <a href="https://jekyllrb.com/docs/plugins/installation/" target="_blank">jekyllrb.com/docs/plugins/installation/</a>
* <a href="https://jekyllrb.com/docs/pagination/" target="_blank">Jekyll - Pagination Docs</a>
* <a href="https://jekyllrb.com/tutorials/navigation/" target="_blank">Jekyll - Navigation Tutorial</a>
* <a href="https://superdevresources.com/share-buttons-jekyll/" target="_blank">https://superdevresources.com/share-buttons-jekyll/</a>


### Themes

* <a href="https://pages.github.com/themes/" target="_blank">pages.github.com/themes/</a> - even though this page says only those themes are available for github pages its not true. Hard to point you, because figuring out a theme is a personal journey.
* <a href="https://github.blog/2017-11-29-use-any-theme-with-github-pages/" target="_blank">github.blog/2017-11-29-use-any-theme-with-github-pages/</a>
* <a href="https://pmarsceill.github.io/just-the-docs" target="_blank">pmarsceill.github.io/just-the-docs/</a>
* <a href="https://github.com/pages-themes/leap-day/blob/master/assets/js/main.js" target="_blank">pages-themes/leap-day/assets/js/main.js</a>
* <a href="https://pages-themes.github.io/leap-day" target="_blank">pages-themes.github.io/leap-day/</a>

### Front Matter

* <a href="https://jekyllrb.com/docs/front-matter/" target="_blank">Front Matter</a>
* <a href="http://simpleprimate.com/blog/front-matter" target="_blank">YAML front matter in Jekyll</a>
* <a href="https://idratherbewriting.com/documentation-theme-jekyll/mydoc_yaml_tutorial" target="_blank">YAML tutorial in the context of Jekyll</a>


### SEO and Rich Snippets

* <a href="https://help.github.com/en/articles/search-engine-optimization-for-github-pages" target="_blank">Search Engine Optimization for Github Pages - help.github.com</a>
* <a href="https://github.com/jekyll/jekyll-seo-tag" target="_blank">/jekyll/jekyll-seo-tag</a>
* <a href="https://github.com/pmarsceill/jekyll-seo-gem" target="_blank">/pmarsceill/jekyll-seo-gem</a>
* <a href="https://warfareplugins.com/open-graph-tags-twitter-cards-rich-pins/" target="_blank">Open Graph Tags, Twitter Cards, Rich Pins</a>
* <a href="https://www.reddit.com/r/discordapp/comments/82p8i6/a_basic_tutorial_on_how_to_get_the_most_out_of/" target="_blank">A basic tutorial on "How to get the most out of embeds?" for a discord-friendly website!</a>
  * <a href="https://discordapp.com/developers/docs/resources/channel#embed-limits" target="_blank">discordapp.com/developers/docs/resources/channel#embed-limits</a>
* <a href="https://blog.webjeda.com/optimize-jekyll-seo/" target="_blank">Tips to Optimize Jekyll SEO</a>
* <a href="http://iframely.com/debug" target="_blank">http://iframely.com/debug</a>
* [realfavicongenerator.net](https://realfavicongenerator.net) — before you go down a rabbithole... make sure your image is 225x225px (for fb\og)... and for the facebook open graph, don't use the metatags in your template, instead put that info in your config.yml
  > The strict minimum for the master picture is 70x70. Your picture is 225x225, which is ok. However, it is recommended to use a picture of at least 260x260. If you still want to use your picture, some of the derivated favicons will not be generated, such as the high resolution tile for Windows 8 / IE 11.
* <a href="http://ogp.me" target="_blank">ogp.me</a> - Open Graph Webpage (really good resource for Facebook and beyond. great links at bottom.)

### Twitter 

* <a href="https://cards-dev.twitter.com/validator" target="_blank">Twitter Card Validator</a>
* <a href="https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards" target="_blank">About Cards - developer.twitter.com</a>

## Advance

### HTML - CSS

* <a href="https://unicode-table.com/en/#miscellaneous-symbols-and-pictographs" target="_blank">unicode-table.com/#miscellaneous-symbols-and-pictographs</a> 
  - cause I don't know where else to put this.
* <a href="https://htmldog.com/guides/html/beginner/" target="_blank">htmldog.com - HTML5 and CSS Beginner Tutorials</a> 
  * Lets get real... a simple page  that just displays information isn't enough. Once you want to configure specific elements you're gonna have to learn HTML and CSS... or maybe you're like me and just want to learn as little as possible to add a feature (in this case, sidebar navigation)... next thing you know "wait, when did I decide to learn HTML5 and CSS?"
* <a href="https://www.w3schools.com/w3css/w3css_sidebar.asp" target="_blank">/w3css/w3css_sidebar.asp</a>
* <a href="https://www.w3.org/wiki/The_web_standards_model_-_HTML_CSS_and_JavaScript" target="_blank">The_web_standards_model_-_HTML_CSS_and_JavaScript</a>
* <a href="https://developer.mozilla.org/en-US/docs/Learn" target="_blank">Learn web development - developer.mozilla.org</a>
* <a href="https://codepen.io/maziarzamani/pen/eJKGvj" target="_blank">Flat CSS Sidebar</a>
* <a href="https://developer.mozilla.org/en-US/docs/Learn/HTML/Introduction_to_HTML/The_head_metadata_in_HTML" target="_blank">The Head - Metadata in HTML</a>

### Liquid
You can only ignore those squiggly braces that make up much of your site templates for so long.

<img src="https://i.imgur.com/jMtd9WR.png"/>

* <a href="https://simpleit.rocks/ruby/jekyll/templates/jekyll-variables-and-liquid-template-tags-cheatsheet/" target="_blank">Jekyll Variables and Liquid Template Tags-Cheatsheet</a>
* <a href="https://learn.cloudcannon.com/jekyll/introduction-to-liquid/" target="_blank">Introduction to Liquid for Jekyll</a>
* <a href="https://blog.webjeda.com/jekyll-liquid/" target="_blank">https://blog.webjeda.com/jekyll-liquid/</a>


### Git

* <a href="https://gist.github.com/davfre/8313299" target="_blank">davfre/git_cheat-sheet.md</a>
* <a href="https://education.github.com/git-cheat-sheet-education.pdf" target="_blank">education.github.com - GIT CHEAT SHEET</a>
* <a href="https://chris.beams.io/posts/git-commit/" target="_blank">Writing Effective Commits</a>

### SSH

* <a href="https://help.github.com/en/articles/connecting-to-github-with-ssh" target="_blank">Connecting to GitHub with SSH</a>
* <a href="https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent" target="_blank">Generating a new SSH key and adding it to the SSH agent</a>
* <a href="https://help.github.com/en/enterprise/2.15/user/articles/adding-a-new-ssh-key-to-your-github-account" target="_blank">Adding a new SSH key to your GitHub Account</a>
* <a href="https://medium.freecodecamp.org/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca" target="_blank">How to manage multiple GitHub accounts on a single machine with SSH keys</a>

---

## [Home](https://infominer.id)
