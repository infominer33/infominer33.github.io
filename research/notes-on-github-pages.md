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

*\*note: indicating layout only necessary in the index.md*

of course there are other steps, as explained in the links below, but if you don't do those two steps than you will be sad if you want link previews (rich snippets) when you share your links on various apps and sites.

Minimum effort... you can have a web-page up and running in an hour or so.. 

—[**infominer**](https://infominer.id)

## Markdown

* [Mastering Markdown](https://guides.github.com/features/mastering-markdown/)
* [Markdown Cheet-Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
* [unicode-table.com/en/#miscellaneous-symbols-and-pictographs](https://unicode-table.com/en/#miscellaneous-symbols-and-pictographs) - cause I don't know where else to put this.
* [htmldog.com - HTML5 and CSS Beginner Tutorials](https://htmldog.com/guides/html/beginner/) Lets get real... a simple page  that just displays information isn't enough. Once you want to configure specific elements you're gonna have to learn HTML and CSS... or maybe you're like me and just want to learn as little as possible to add a feature (in this case, sidebar navigation)... next thing you know "wait, when did I decide to learn HTML5 and CSS?"

## Github Pages

* [http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/](http://ragupappu.com/2015/04/22/setup-website-using-github-pages-and-jekyll/)
* [Getting Started with Github Pages - Part 1 - Publishing a single Page](https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-1-Publishing-a-single/ba-p/237)
* [Getting Started with GitHub Pages - Part 2](https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-2-Using-an-official/ba-p/2030)
* [Getting started with GitHub Pages: Part 3 -- Local development with GitHub Pages](https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-3-Local-development-with/ba-p/2292)
* [Getting started with GitHub Pages: Part 4 -- Customizing your Pages site](https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-4-Customizing-your-Pages/ba-p/4058)
* [Adding Jekyll Plugins to a GitHub Pages Site - help.github.com](https://help.github.com/en/articles/adding-jekyll-plugins-to-a-github-pages-site)
* [Setting up You GitHub Pages Site Locally with Jekyll](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll)
* [GitHub Pages —github.community](https://github.community/t5/GitHub-Pages/bd-p/pages)
* [https://pages.github.com/versions/](https://pages.github.com/versions/)
* [Creating Custom 404 page](https://help.github.com/en/articles/creating-a-custom-404-page-for-your-github-pages-site)
* [Jekyll Redirect Plugin](https://help.github.com/en/articles/redirects-on-github-pages)

## Jekyll

* [Jekyll - Cheat Sheet](https://devhints.io/jekyll)
* [/jekyll/jekyll/blob/master/README.markdown](https://github.com/jekyll/jekyll/blob/master/README.markdown)
* [jekyllrb.com/docs/plugins/installation/](https://jekyllrb.com/docs/plugins/installation/)
* [Jekyll - Pagination Docs](https://jekyllrb.com/docs/pagination/)
* [Jekyll - Navigation Tutorial](https://jekyllrb.com/tutorials/navigation/)
* [https://superdevresources.com/share-buttons-jekyll/](https://superdevresources.com/share-buttons-jekyll/)

## Liquid
You can only ignore those squiggly braces that make up much of your site templates for so long.

<img src="https://i.imgur.com/jMtd9WR.png"/>

* [Jekyll Variables and Liquid Template Tags-Cheatsheet](https://simpleit.rocks/ruby/jekyll/templates/jekyll-variables-and-liquid-template-tags-cheatsheet/)
* [Introduction to Liquid for Jekyll](https://learn.cloudcannon.com/jekyll/introduction-to-liquid/)
* [https://blog.webjeda.com/jekyll-liquid/](https://blog.webjeda.com/jekyll-liquid/)

## Themes

* [pages.github.com/themes/](https://pages.github.com/themes/) - even though this page says only those themes are available for github pages its not true. Hard to point you, because figuring out a theme is a personal journey.
* [github.blog/2017-11-29-use-any-theme-with-github-pages/](https://github.blog/2017-11-29-use-any-theme-with-github-pages/)
* [pmarsceill.github.io/just-the-docs/](https://pmarsceill.github.io/just-the-docs/)
* [pages-themes/leap-day/assets/js/main.js](https://github.com/pages-themes/leap-day/blob/master/assets/js/main.js)

## Front Matter

* [Front Matter](https://jekyllrb.com/docs/front-matter/)
* [YAML front matter in Jekyll](http://simpleprimate.com/blog/front-matter)
* [YAML tutorial in the context of Jekyll](https://idratherbewriting.com/documentation-theme-jekyll/mydoc_yaml_tutorial)


## SEO and Rich Snippets

* [Search Engine Optimization for Github Pages - help.github.com](https://help.github.com/en/articles/search-engine-optimization-for-github-pages)
* [/jekyll/jekyll-seo-tag](https://github.com/jekyll/jekyll-seo-tag)
* [/pmarsceill/jekyll-seo-gem](https://github.com/pmarsceill/jekyll-seo-gem)
* [Open Graph Tags, Twitter Cards, Rich Pins](https://warfareplugins.com/open-graph-tags-twitter-cards-rich-pins/)
* [A basic tutorial on "How to get the most out of embeds?" for a discord-friendly website!](https://www.reddit.com/r/discordapp/comments/82p8i6/a_basic_tutorial_on_how_to_get_the_most_out_of/)
  * https://discordapp.com/developers/docs/resources/channel#embed-limits
* [Tips to Optimize Jekyll SEO](https://blog.webjeda.com/optimize-jekyll-seo/)
* [http://iframely.com/debug](http://iframely.com/debug)

## Twitter 

* [Twitter Card Validator](https://cards-dev.twitter.com/validator)
* [About Cards - developer.twitter.com](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)

## Git

* [davfre/git_cheat-sheet.md](https://gist.github.com/davfre/8313299)
* [education.github.com - GIT CHEAT SHEET](https://education.github.com/git-cheat-sheet-education.pdf)
* [Writing Effective Commits](https://chris.beams.io/posts/git-commit/)

## SSH

* [Connecting to GitHub with SSH](https://help.github.com/en/articles/connecting-to-github-with-ssh)
* [Generating a new SSH key and adding it to the SSH agent](https://help.github.com/en/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
* [Adding a new SSH key to your GitHub Account](https://help.github.com/en/enterprise/2.15/user/articles/adding-a-new-ssh-key-to-your-github-account)
* [How to manage multiple GitHub accounts on a single machine with SSH keys](https://medium.freecodecamp.org/manage-multiple-github-accounts-the-ssh-way-2dadc30ccaca)

---

## [Home](https://infominer.id)
