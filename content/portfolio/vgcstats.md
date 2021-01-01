---
title: "VGCStats"
date: 2018-05-10T13:47:36-05:00
draft: false
showonlyimage: false
image: "/headers/vgcstats.png"
weight: 100
---

A website that gathers statistics about official tournaments of the Pokémon Videogame Championship. 

<!--more-->

[You can see the website here](https://vgcstats.com)

## So, Pokémon, huh?

Yes. Believe it or not, Pokémon is more than the japanese cartoon than moved the whole world in the 90's. Pokémon started as a videogame in 1996, and one of the things that made this videogame so popular was the ability to challenge your friends to a Pokemón battle. In 2009, the first world championship of Pokémon battles was held in San Diego, California, way before esports were even a thing. After that, it has been held each year in different cities. In 2017, more than 900 people from more than 40 countries gathered in Anaheim, California looking for the World Champion title.

![](/content/vgcstats01.jpg)
<small>The 2017 Pokémon World Champions. Photo by [Nintendo Insider](https://www.nintendo-insider.com/new-world-champions-triumph-at-the-2017-pokemon-world-championships/).</small>

To qualify to the world championship, players must earn Championship Points throughout the year playing in different official events all around the world. Each year, the ruleset for the battles are different. This may change because a new version of the game was released, or just because some rules were added to make the game more balanced, more exciting or simply for marketing reasons. This means, every season has its own flavor. And making a team of 6 Pokémon out of the 807 currently available while considering these rulesets may seem like something impossible. That is where VGCStats comes. 

VGCStats is a database of which pokemon are being used in official tournaments, and how well they are doing. Its main feature is showing how many championship points players have earned using that particular Pokémon. It also shows the standings for each official tournament and which teams were used by each of the players. There is also an option to add VODs, or Videos On Demand, so players can actually watch the matches of that tournament.

![](/content/vgcstats02.jpg)
<small>The top four pokemon, as of May 19th, 2018</small>

This project has been helpful to players which use it to build their teams and be prepared for whatever they could find in other teams (watch PokeAlex, one of the top players from Spain, [ <i class="fa fa-youtube-play"></i>talking about the website](https://www.youtube.com/watch?v=hk4FntlUHDw])), for streamers ([<i class="fa fa-twitter"></i>This is a tweet](https://twitter.com/NBDwee/status/972594234006974464) from Duy Ha, a Pokémon Video Game commentator) and even for press (Game Haus made an article [using stats from our website](https://thegamehaus.com/youre-not-running-porygon2-plus-araquanid-youre-throwing-duos-newfound-success-2018/2018/04/14/). This is the first of [many](https://thegamehaus.com/mega-aerodactyl-went-from-0-championship-points-to-over-700-in-one-day/2018/04/24/))

As of May 19th 2018, the site has welcomed about 11,000 players from almost 100 countries since its launch on january 16th 2018. Huge success!

## Was there nothing like this before?

Well, kinda. VGCStats as a project was not really my idea. The idea was from [ProfShroomish](https://twitter.com/profshroomish), who made the [<i class="fa fa-twitter"></i>VGCStats twitter account](https://twitter.com/vgcstats), in which he posted the results he gathered in graphics he made. He was gathering all the data in a simple spreadsheet, so it came to my mind. 

>**Is there a simple way in which we can show this data not in a spreadsheet, but in a website?** 

I made a prototype in a night and the next day I was slipping into his DMs sending my proposal. After that, we started working on the project. Nowadays ProfShroomish still gathers the data and feeds the spreadsheet, while I am focused on developing and mantaining the site.

## So, how is the site made?

<div class="stack-icons">
	<img src="/icons/sheets.svg">
	<img src="/icons/vue.svg">
	<img src="/icons/js.svg">
	<img src="/icons/bootstrap.svg">
	<img src="/icons/github.svg">
</div>

All the data lives in a Google spreadsheet. Pokémon, teams, events, players, everything is there. There is no further backend involved. All ETL of the data is made client-side using ES6 functions like map, reduce and filter. 

The site is a single-page application made with [Vue](https://vuejs.org/). Before making this site, I had never touched Vue before, but it was way too easy and I quickly fell in love. I made the prototype in under two hours. I use [Vue Router](https://router.vuejs.org/en/) to manage navigation between the sections. The filtering of the data makes heavy use of Vue's reactivity. Whenever a value is changed in the filters, Vue automatically changes the data shown in the site.

Style is mostly vanilla Bootstrap 4, using [Bootstrap Vue](bootstrap-vue.js.org) for some components.

The site's code is available on [<i class="fa fa-github"></i>github](https://github.com/bul-ikana/vgcstats), and the site itself is hosted on github pages.

## What is next?

VGCStats is a live project, with features and changes being delivered week after week. As the season evolves the metagame changes, so we try to keep the site relevant adding features helpful to the players. There is still a long way to go, and this is thanks to everyone that uses the site.

