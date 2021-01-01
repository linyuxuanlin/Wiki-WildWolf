---
title: "RBYDex"
date: 2018-05-10T13:47:36-05:00
draft: false
showonlyimage: false
image: "/headers/rbydex.png"
weight: 300
---

An app to keep track of your in-game Pokédex in the red, blue and yellow versions of the Pokémon game. 

<!--more-->

[You can download the app for Android here](https://play.google.com/store/apps/details?id=bul.ikana.rbydex)

## A long journey

I am a big fan of the Pokémon games. I got a game boy color and the blue version in 1998, and since then, I have played each new generation of games whenever it comes out. Each new version of the game brings great improvements to the series. Right now, we are on the seventh generation, and a lot of things have changed for the better.

![](/content/rbydex01.png)
<small>The Pokémon games have changed a lot in more than 20 years</small>

As a fan of the games, it has been an incredible journey. So great, that sometimes you start to forget how much certain things have improved. On February 2016, the first generation of the games (blue, red and yellow) were released again, but this time for the Nintendo 3DS. Playing this games again after so many years was such a nostalgia shot, for a while. After a few hours playing the game, it started becoming annoying. The first generation of the games is not only [the generation with more glitches and bugs](https://bulbapedia.bulbagarden.net/wiki/List_of_glitches_in_Generation_I), but it also missed very important features.

One of that features was an UX improvement introduced in the second generation. Whenever you battled a wild Pokémon, a handy indicator was shown next to the Pókemon name if you have already caught that Pokémon before. This may sound trivial, but having _"Gotta catch 'em all"_ as one of the goals of the game, it was extremely useful knowing if you already have caught that Pokémon before or not.

![](/content/rbydex02.png)
<small>This little pokeball indicator tells you if you already have caught that Pókemon when you find one in the wild</small>

The first generation of the games lacked this feature, so you basically had to learn by heart which ones you already had. When I was a kid, I wrote them in a notebook. But I have grown, and I got skills. It came to me.

>**Can I make an app to keep track of my current Pokédex completion, using my smartphone as a companion screen for the game?** 

## Help yourself first

At the beginning, I was planning on doing a simple app for my personal use. Nothing more than a glorified todo list. And I did. And it was great. But as I kept playing the games, more annoying stuff started to appear. _"Can this Pokémon learn this attack?"_, _"How does it evolves?"_, _"Where do I find a Pikachu?"_. Everytime I was wondering about something like this, I had to google it. After I while, I got tired of changing from the app to google to search what I needed. I started adding to the app all the information I though I was going to need eventually. And after a while, I had the perfect companion app for playing Pokémon Red, Blue and Yellow.

The app was exactly what I needed, and helped me not just finishing the game (which was easy anyways), but helped me what I could not do as a kid: **"Catch 'em all"**. Ater I finished my in-game Pokédex, it was clear that this app was an useful tool, so I made a bit of cleanup, and I uploaded it to Google Play.

## So, how is the app made?

<div class="stack-icons">
	<img src="/icons/android.svg">
	<img src="/icons/cordova.svg">
	<img src="/icons/ionic.svg">
	<img src="/icons/angular.svg">
	<img src="/icons/js.svg">
</div>

The app was made using [ionic v1](https://ionicframework.com/docs/v1/). This version of ionic still used AngularJS 1.5. I built this app only for Android even though Ionic and Cordova make it very easy to deploy to iOS too. I have a windows machine and I develop in linux, so I had no apple computer at hand to release it to iOS.

This was also a little experiment in finding the ["Hybrid sweet spot"](https://signalvnoise.com/posts/3743-hybrid-sweet-spot-native-navigation-web-content) as described by Basecamp. This sweet spot looks for "Native Navigation, web content". Doing this only with ionic is not possible, as it uses the default AngularJS router, and as such, it uses web navigation. One option, as proposed by Basecamp, was making native shells to contain the web views and natively navigate between them. But this defeats the whole point of using AngularJS as a framework, as it will make extremely hard to share data between the views.

So I found a simple option in the shape of a plugin. The [<i class="fa fa-github"></i> Native Page transitions](https://github.com/Telerik-Verified-Plugins/NativePageTransitions) cordova plugin by [Telerik](https://www.telerik.com/) (the company behind NativeScript). This plugin made native transitions using a simple but ingenious workaround. Whenever navigation was triggered, the plugin took a screenshot of the site, then uses a native transition to switch between this bitmap to the new webview. This allows to do conceptually fake but technically true native transitions using ionic and cordova. Besides techonology, users have the feeling of a true native app even if all of the views are packaged HTML.

## Success

For such a niche app, it was a huge success. As of May 2018, it has 46 reviews, over 4,000 downloads and an average score of 4.5. All of this without any kind of marketing. I just uploaded it to the store, without expecting nothing. It even gave me an small but non negligible income from ads. 

This shows an important lesson about software. Better tools are developed when you live and understand the problem than when you are only told about the problem second hand. I know it's hard, but we should try to be as involved as possible in the problems of our users whenever we are developing even the most trivial piece of software.