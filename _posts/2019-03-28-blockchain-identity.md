---
layout: post
title: Blockchain Identity Reources - TOML
description: The beginnings of a tagged database for blockchain identity related resources.
thumbnail: "assets/img/blockchain-id_feature.png"
feature-img: "assets/img/infoblank.png"
permalink: posts/blockchain-identity/
canonical_url: 'https://infominer.xyz/posts/blockchain-identity/'
date: 2019-03-28
tags: ["DecentralizeID"]
last_modified_at: 2023-02-26
excerpt: > 
  The inspiration for my work in digital identity might easily trace back to The Original Blockchain Identity list on GitHub, originally compiled by Markus Sabadello.

  /peacekeeper/blockchain-identity 
  
  I leaned heavily on that resource when first learning about decentralized identity and blockchain. 
---

This is among my earliest posts, and came at a time when I first began to think about how can this project evolve into the future, beyond lists of links gathered and organized by hand?

## Knowledge Defies Categorization

Part of the challenge I encountered is that information wont be neatly divided into categories. Fields of knowledge are all overlapping, and a given post will fit within multiple categories.

What I came to understand is that I should use some type of structured data, so that I required only a single entry of an item in the data file, for it to be featured within multiple categories, once the finished product was rendered.

## Infominer meets Structured Data

When I began, I didn't really know much about types of data.

I decided upon TOML because it's user-friendly, and easy to read. Once data is structured in this way, it can be transformed to JSON, or whichever format works best for a given project.

This page has two toml files from [infominer33/SourceCrypto](https://github.com/infominer33/SourceCrypto) embedded into it, marking a beginning in my effort to enhance my curation and publishing through automation.

I've always been good with a computer, but this was entering me into an entirely new domain. At the time of publication is when I began learning how to publish websites and use developers tools.

## Future Direction

* ~~some simple way to check [didecentral.github.io](https://decentralized-id.com) against these lists, and output a list of links that have yet to be included.~~
* ~~an app that will take a list of links as the input and output a toml file with title\description automatically populated based on metadata..~~

(Crossing out these items, as now I can manage these tasks with python)

I suppose it would make the most sense to prioritize those objectives, rather than constructing everything by hand.

> Scraping a list of links from wherever I want is simple.. so really the two things are checking a list of links against a toml file(s), outputting any links not found in the db already. Another script to construct a toml file grabbing metadata.

At this time I didn't come to the logical conclusion of how easy it could have been to generate content based on the files embedded here. I was just getting in way over my head, and was hopeful someone coder would catch my enthusiasm and make the code for me.

Ultimately it has worked out fine and in 2023, finally coming around to this idea: full-circle.

### Algorithmic tagging

> what's really missing is tagging all of these resources by authors, co-authors, references/citations
>
> once this is done, topical tags can be derived algorithmically\
> [Enabling Author-Centric Ranking of Web Content](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.397.8960&rep=rep1&type=pdf) - @MaciekLaskus on twitter

Once I get the infrastructure in place that will be next on my list. Even simply downloading all of the links and generating a keyword list for each could get us a long way.

## Blockchain Identity - Data

The inspiration for my work in digital identity might easily trace back to *The Original* Blockchain Identity list on GitHub, originally compiled by [Markus Sabadello](https://github.com/peacekeeper/).

- [/peacekeeper/blockchain-identity](https://github.com/peacekeeper/blockchain-identity)
  
I leaned heavily on that resource when first learning about decentralized identity and blockchain. 
  
After making some progress on decentralized-id.com, I went back over that whole repository, fixing any broken links and pulling in relevant data, at the end of 2018.

### blockchain-id.toml

* [SourceCrypto/_data/toml/blockchain-id.toml](https://github.com/infominer33/SourceCrypto/blob/master/_data/toml/blockchain-id.toml)

<script src="https://gist.github.com/infominer33/69dc7970a4ff9503de38916c46034bf6.js"></script>

### blockchain-id2.toml

* [SourceCrypto/_data/toml/blockchain-id2.toml](https://github.com/infominer33/SourceCrypto/blob/master/_data/toml/blockchain-id2.toml)

<script src="https://gist.github.com/infominer33/22a0ea812f04459f88a5418ffde1a32c.js"></script>