---
layout: post
title: "Leveling Up - What I've been working on lately."
description: "What I've been up to since my last post a year ago. On learning some Ruby, some Python and starting a decentralized-id newsletter with Identity Woman."
thumbnail: "assets/img/long-and-winding-road.png"
author: infominer
feature-img: "assets/img/long-and-winding-road.png"
img: #"https://imgur.com/QzUQ3fF.png"
permalink: /still-plugging-away/
excerpt_separator: <!--more-->
toc: false
last_modified_at: 2020-11-11T11:22:33-23:00
date: 2020-11-12
---

It's been a year since my last post... Overwhelmed by trying to keep up with the fast flows of information, and my own internal processes, I took a break from social media, stopped working on most of the projects I had begun, and turned inward. I've also been busy leveling up, and discovering my potential.

**So what exactly have I doing with all that time?**

<!--more-->

## Managing Emotions

If you haven't been following my story, so far, the short version is that I quit drinking a few years ago, and all of this info-gathering has been an important part of my recovery process, and a path to creating a new life. 

All the same, however far along I had come in my work, and self-education, I still had the challenges processing every day emotions, which I'd been primarily avoiding by processing as much information on valuable topics as possible.

Turning that around, I shifted most of my info-gathering from blockchain, cryptocurrencies and decentralized-identity, to focus more on mental hygiene and emotional agility.

The most valuable information I've encountered in that regard is [Marshall Rosenberg's Nonviolent Communication](https://www.cnvc.org/training/resource/book-chapter-1).

> We're interested, in nonviolent communication, with the kind of honesty that supports people connecting with each other in a way that makes compassionate giving inevitable, that makes it enjoyable for people to contribute to each other's well being. - Marshall Rosenberg

I've got a couple projects brewing on that topic, and will write more about that later, so don't want to take too much space for that now. 

In brief, I can say that spending time with the teachings of Marshall Rosenberg has made a significant contribution to my mental health and emotional wellbeing.

If you're curious to learn more, I called a session at my first IIW on the topic, you can check out the [notes for that session on the IIW Wiki](https://iiw.idcommons.net/Introduction%5CDiscussion_-_Marshall_Rosenberg%27s_Nonviolent_Communication_(perhaps_discussing_integration_with_standards_processes)), which provides a high-level overview, and lots of links.

## Working with Identity Woman

I'd been chatting with [Kaliya Identity Woman](https://identitywoman.net/) on and off for around a year, after initially contacting her about the potential for our collaborating on decentralized identity. At some point she proposed the idea of writing a newsletter together. 

Instead of jumping in head first, like I usually do, we've spent a lot of time figuring out ways to do that sustainably.

### Planet Pluto Feed Reader

One of the most promising projects I found, through that pursuit, is [Planet Pluto Feed Reader](https://github.com/web-work-tools/awesome-planet-pluto), by Gerald Bauer. 

> In online media a planet is a feed aggregator application designed to collect posts from the weblogs of members of an internet community and display them on a single page. - [Planet (Software)](https://en.wikipedia.org/wiki/Planet_(software))

For the uninitiated, I should add that websites generate RSS feeds that can be read by a newsreader, allowing users to keep up with posts from multiple locations without needing to visit each site individually. You very likely use RSS all the time without knowing, for example your podcast player depends on RSS feeds to bring that content directly to your phone.

What [Pluto Feed reader](https://github.com/feedreader/) does is just like your podcast app, except, instead of an application on your phone that only you can browse, it builds a simple webpage from the feeds you add to it, that can be published on GitHub, your favorite static web-hosting service, or on your own server in the cloud.

![](https://raw.githubusercontent.com/planet-templates/planet-hacker/master/screenshot.png)

Pluto is built with [Ruby](https://www.ruby-lang.org/en/), using the [ERB templating](https://www.stuartellis.name/articles/erb/) language for [web-page design](https://github.com/planet-templates).

One of the cool things about ERB, is it lets you use any ruby function in your web-page template, supporting any capability you might want to enable while rendering your feed. This project has greatly helped me to learn the basics of Ruby, while customizing its templates to suit my needs.

### Feed Search

I use the [RSSHub Radar](https://github.com/DIYgod/RSSHub-Radar) browser extension to find feeds for sites while I'm browsing. However, this would be a lot of work if you're adding a bunch of sites, and you're not guaranteed it will even find the feed.

I found a few simple python apps that find feeds for me. They aren't infallible, but they do allow me to find feeds for multiple sites at the same time, all I have to do is format the query and hit enter.

As you can see below, these are not fully formed applications, just a few lines of code. To run them, it's necessary to install [Python](https://www.python.org/downloads/), install the package with [pip](https://pypi.org/project/pip/) (`pip install feedsearch-crawler`), and type python at the command prompt, which takes you to a Python terminal that will recognize these commands.

From there you can type\paste python commands for demonstration, practice, or for simple scripts like this. I could also put the following scripts into their own feedsearch.py file and type `python feedsearch.py`, but I haven't gotten around to doing anything like that.

Depending on the site, and the features you're interested in, each of these feed seekers has their merits.

#### Feedsearch Crawler

[DBeath/feedsearch-crawler](https://github.com/DBeath/feedsearch-crawler)

```
from feedsearch_crawler import search
import logging
logging.basicConfig(filename='example.log',level=logging.DEBUG)
import output_opml
list = ["http://bigfintechmedia.com/Blog/","http://blockchainespana.com/","http://blog.deanland.com/"]
for items in list:
    feeds = search(items)
    output_opml(feeds).decode()
    logger = logging.getLogger("feedsearch_crawler")
```

#### Feed seeker 

[mitmedialab/feed_seeker](https://github.com/mitmedialab/feed_seeker)

```
from feed_seeker import generate_feed_urls
list = ["http://bigfintechmedia.com/Blog/","http://blockchainespana.com/","http://blog.deanland.com/"]
for items in list:
    for url in generate_feed_urls(items):
        print(url)
```

### GitHub Actions

Pluto Feed Reader is great, but I needed to find a way for it to run a regular schedule, so I wouldn't have to run the command every time I wanted to check for new feeds. For this, I've used [GitHub actions](https://github.com/actions/setup-python).

This is an incredible feature of GitHub that allows you to spin up a virtual machine, install an operating system, dependencies supporting your application, and whatever commands you'd like to run, on a schedule.

```
name: Build BlogCatcher
on:
  schedule:
    # This action runs 4x a day.
    - cron:  '0/60 */4 * * *'
  push:
    paths:
    # It also runs whenever I add a new feed to Pluto's config file.
    - 'planetid.ini'
jobs:
  updatefeeds:
    # Install Ubuntu
    runs-on: ubuntu-latest
    steps:
    # Access my project repo to apply updates after pluto runs
    - uses: actions/checkout@v2
    - name: Set up Ruby
      uses: ruby/setup-ruby@v1
      with:
        ruby-version: 2.6
    - name: Install dependencies
      # Download and install SQLite (needed for Pluto), then delete downloaded installer
      run: | 
        wget http://security.ubuntu.com/ubuntu/pool/main/s/sqlite3/libsqlite3-dev_3.22.0-1ubuntu0.4_amd64.deb
        sudo dpkg -i libsqlite3-dev_3.22.0-1ubuntu0.4_amd64.deb
        rm libsqlite3-dev_3.22.0-1ubuntu0.4_amd64.deb
        gem install pluto && gem install nokogiri && gem install sanitize
    - name: build blogcatcher # This is the command I use to build my pluto project
      run: pluto b planetid.ini -t planetid -o docs
    - name: Deploy Files # This one adds the updates to my project
      run: |
        git remote add gh-token "https://github.com/identosphere/identity-blogcatcher.git"
        git config user.name "github-actions[bot]" # I use the GitHub Actions bot here.
        git config user.email "41898282+github-actions[bot]@users.noreply.github.com"
        git add .
        git commit -a -m "update blogcatcher"
        git pull
        git push gh-token master
```

### Identosphere Blogcatcher

[![](/assets/img/identosphere-blogcatcher.png)](https://identosphere.net/blogcatcher)

[Identosphere Blogcatcher](https://identosphere.net/blogcatcher) ([source](https://github.com/identosphere/planetid-reboot)) is a feed aggregator for personal blogs of people who've been working in digital identity through the years, inspired by the original [Planet Identity](https://web.archive.org/web/20161029051802/http://planetidentity.org/).

We also have a page for [companies](https://identosphere.net/blogcatcher/companies/), and another for [organizations](https://identosphere.net/blogcatcher/organizations/) working in the field. 

### Identosphere Weekly Highlights

Last month, [Kaliya](https://twitter.com/identitywoman) suggested that since we have these pages up and running smoothly, we were ready to start our newsletter. This is just a small piece of the backend information portal we're working towards, and not enough to make this project as painless and comprehensive as possible, but we had enough to get started.

Every weekend we get together, browse the BlogCatcher, and share the content that we're most exciting, or simply catches our interest, related to decentralized-identity.

We'll be publishing our 6th edition, at the start of next week, and our numbers are doing well!

![](/assets/img/identosphere-stats.png){: .center-image }

This newsletter is free, and a great opportunity for us to work together on something consistent, while working on a few other ideas in the works.

<center><iframe src="https://identosphere.substack.com/embed" width="480" height="320" style="border:1px solid #EEE; background:white;" frameborder="0" scrolling="no"></iframe></center>

#### [Support us on Patreon](https://www.patreon.com/identosphere)

While keeping the newsletter free, we are accepting contributions via Patreon. 

<a href="https://www.patreon.com/identosphere"><img src="/assets/img/identosphere-patreon.png" align="center" alt="Become a patron"></a>

So far, we have enough to cover a bit more than server costs, and this will ideally grow to support our efforts, and enable us to sustainably continue developing these open informational projects.

## Python, Twitter Api, and GitHub Actions

Since we're publishing this newsletter, and I've gotten a better handle on my inner state, I decided it was time to come back to twitter. However, I knew I couldn't do it the old way, where I manually re-tweeted everything of interest, spending hours a day scrolling my feed trying to stay abreast of important developments.

Instead, I decided to dive into the twitter api. The benefits of using twitter programmatically can't be understated. For my first project, I decided to try an auto-poster, which could enable me to keep an active twitter account, without having to regularly pay attention to twitter.

I found a simple guide [How To Write a Twitter Bot with Python and tweepy](https://dototot.com/how-to-write-a-twitter-bot-with-python-and-tweepy/) composed of a dozen lines of python. That simple script posts a tweet to your account, but I wanted to post from a pre-made list, and so figured out how to read from a [yaml](https://yaml.org/) file, and then used [GitHub actions](https://github.com/actions/setup-python) to run the script on a regular schedule.

While that didn't result in anything I'm ready to share here, quite yet, somewhere during that process I realized that I could write python. After playing around with Ruby, in ERB, to build the BlogCatcher, and running various python scripts that other people wrote, tinkering where necessary, eventually I had pieced together enough knowledge I could actually write my own code!

### Decentralized ID Weekly Twitter Collections

With that experience as a foundation I knew I was ready to come back to twitter, begin trying to make make a more efficient use of its wealth of knowledge, and see about keeping up my accounts without losing my hair.

I made a script that searches twitter for a variety of keywords related to decentralized identity, and write the tweet text and some other attributes to a csv file. From there, I can sort through those tweets, and save only the most relevant, and publish a few hundred tweets about decentralized identity to a weekly twitter collection, that we're using as part of the backend for our newsletter.

Soon these will be regularly published to [decentralized-id.com](https://decentralized-id.com), which i found out is an approved method of re-publishing tweets, unlike the ad hoc method I was using before, sharing them to discord channels (which displays the preview image \ text), exporting their contents and re-publishing that.

I also intend to share the source, for all that, after I've gotten the kinks worked out.

#### Twitter collections I've made so far

* [Self Sovereign ID 101](https://twitter.com/DecentralizeID/timelines/1322735918386733057)
* [October Week 5 #SSI #DID](https://twitter.com/DecentralizeID/timelines/1322785746915307520)
* [November Week 1 #SSI #DID](https://twitter.com/DecentralizeID/timelines/1325219075463712769)

### Decentralized-ID.com

Now we have a newsletter, and are seeking patrons, it seemed appropriate to work on developing [decentralized-id.com](https://decentralized-id.com/posts/), cleaning up some of its hastily thrown together parts, and adding a bunch of content to better represent the decentralized identity space.

That said, I've not given up on [Bitcoin](https://bitcoinfo.xyz), or [Crypto](https://sourcecrypto.pub). On the contrary, I'm sure this work is only expanding my future capacity to continue working to fulfil the original vision of those resources.

## Web-Work.Tools

With the information and skills i've gathered over the past year, [web-work.tools](https://web-work.tools) was starting to look pretty out of date, relative to the growth of my understanding.

I updated [GitHub Pages Starter Pack \ Extended Resources](https://web-work.tools/jamstack/github-pages-starter-pack/) quite a lot to reflect those learnings, and separate the wheat from the chaff of the links I gathered when I was first figuring out how to use GitHub pages.

## Thanks for stopping by!

<center>
<h3>Subscribe for Updates</h3>
<form class="staticman" method="POST" action="https://identosphere.net/staticman/v2/entry/infominer33/subscribe/master/subscribe">
    <input name="options[redirect]" type="hidden" value="https://infominer.xyz/subscribed">
    <input name="options[slug]" type="hidden" value="infohub">
    <input name="fields[name]" type="text" placeholder="Name (optional)"><br>
    <input name="fields[email]" type="email" placeholder="Email"><br>
    <input name="fields[message]" type="text" placeholder="Areas of Interest (optional)"><br>
    <input name="links" type="hidden" placeholder="links">
    <button type="submit">Subscribe</button>
</form>
</center>