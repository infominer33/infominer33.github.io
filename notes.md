---
title: Notes and Resources—Getting Started w GitHub Pages
Desciption: If you know markdown then you can do this. To get started all you need is a repository called `projectname.github.io` and a readme.md
image: "https://infominer.id/images/github-pages.jpeg"
---

# notes on how to set up a github webpage w jekyll

If you know markdown then you can do this. To get started all you need is a repository called `projectname.github.io` and a readme.md.  Go into settings and use the theme chooser. In order to set up rich snippets, so your preview image embeds on various platforms, you need to do a little additional configuring.

* create an index.md 

Although pages will create an index.html from your readme, it will not behave as expected if you try to do any configuration or additional optimization.

in that index.md you need to include front matter:

`---`\
`layout: default`\
`---`

*\*note: indicating layout only necessary in the index.md*

of course there are other steps, as explained in the links below, but if you don't do those two steps than you will be sad if you want link previews on various apps and sites.

Minimal barriar to entry, you can have a web-page up and running in a day or so.

## Jekyll

### Github 

* [Getting Started with GitHub Pages - Part 2](https://github.community/t5/Support-Protips/Getting-started-with-GitHub-Pages-Part-2-Using-an-official/ba-p/2030)
* [Adding Jekyll Plugins to a GitHub Pages Site - help.github.com](https://help.github.com/en/articles/adding-jekyll-plugins-to-a-github-pages-site)
* [/jekyll/jekyll/blob/master/README.markdown](https://github.com/jekyll/jekyll/blob/master/README.markdown)
* [Setting up You GitHub Pages Site Locally with Jekyll](https://help.github.com/en/articles/setting-up-your-github-pages-site-locally-with-jekyll)
* [GitHub Pages —github.community](https://github.community/t5/GitHub-Pages/bd-p/pages)
* [https://pages.github.com/versions/](https://pages.github.com/versions/)

### Jekyll 

* [talk.jekyllrb.com - jekyll-slate-theme/2668](http://talk.jekyllrb.com/t/jekyll-slate-theme/2668)
* [https://jekyllrb.com/docs/plugins/installation/](https://jekyllrb.com/docs/plugins/installation/)
* [https://jekyllrb.com/docs/pagination/](https://jekyllrb.com/docs/pagination/)

## SEO and Rich Snippets

* [Search Engine Optimization for Github Pages - help.github.com](https://help.github.com/en/articles/search-engine-optimization-for-github-pages)
* [/jekyll/jekyll-seo-tag](https://github.com/jekyll/jekyll-seo-tag)
* [/pmarsceill/jekyll-seo-gem](https://github.com/pmarsceill/jekyll-seo-gem)
* [Open Graph Tags, Twitter Cards, Rich Pins](https://warfareplugins.com/open-graph-tags-twitter-cards-rich-pins/)
* [A basic tutorial on "How to get the most out of embeds?" for a discord-friendly website!](https://www.reddit.com/r/discordapp/comments/82p8i6/a_basic_tutorial_on_how_to_get_the_most_out_of/)
* [Tips to Optimize Jekyll SEO](https://blog.webjeda.com/optimize-jekyll-seo/)
* [http://iframely.com/debug](http://iframely.com/debug)

### Twitter

* [Twitter Card Validator](https://cards-dev.twitter.com/validator)
* [About Cards - developer.twitter.com](https://developer.twitter.com/en/docs/tweets/optimize-with-cards/overview/abouts-cards)
