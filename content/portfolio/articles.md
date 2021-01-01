---
title: "VGCStats Articles"
date: 2018-10-13
draft: false
image: "/headers/articles.png"
showonlyimage: false
weight: 101
---

An articles section for the VGCStats website.
<!--more-->

VGCStats has grown. As we said in a tweet from its [official account](https://twitter.com/vgcstats/status/1042128425190928387):

> *"We feel VGC Stats has transitioned from a personal project to something bigger, a VGC community utility."*

One feature we wanted to offer was having a section with articles, team reports, or simply general news. Thanks to some of the top player of the Pennsylvania Regional Championships, we had our first relevant content.

Team reports are important for the Pokémon competitive community. They not only show in detail the team used to get a top placing in the tournament. They also give great insights in the strategy and mindset of the player piloting that team. Team reports help new players and veternas alike, so hosting them in VGCStats makes the site an even better tool for the community.

![](/content/articles01.png)

## So, how is the site made?

<div class="stack-icons">
	<img src="/icons/hugo.svg">
	<img src="/icons/bootstrap.svg">
	<img src="/icons/netlify.svg">
</div>

The articles section is different from the site itself. The articles section is an static site generated using [Hugo](https://gohugo.io/), and hosted in [Netlify](https://www.netlify.com/). The theme is independent and it is added as a submodule.

### The theme

The theme is based on [Hugo Cards](https://hugo-cards-site.netlify.com/). The main difference is, of course, aesthetic. I included the menu used for the VGCStats site, and tweaked a bit the colors. Another difference is that I has to use Bootstrap 4 instead of boostrap 3, which is used in Hugo Cards.

### The base of the theme

Hugo Cards is a Hugo theme I ported from [Webjeda cards](https://webjeda.com/cards/), a Jekyll theme. I liked the theme a lot to be the base for the articles sections, so I ported it to Hugo. All the original features of the theme were ported. You can read a bit more about this theme in its [own article](/portfolio/hugo-cards)

### The original theme

Webjeda cards is a Bootstrap based Jekyll theme developed by [Webjeda](https://twitter.com/webjeda). 