---
title: "LeafBook"
date: 2018-05-08T13:54:36-05:00
draft: false
image: "/headers/leafbook.png"
showonlyimage: false
weight: 200
---

A simple note taking app 🍃
<!--more-->

[You can check LeafBook here](https://leafbook.netlify.com/#/)

## What is LeafBook?

LeafBook is a simple app to take notes. You can create any book by name and add notes called leaves in each of them. There is no login, so you can have access to your notes in every device just by remembering your book name.

I made this out of the sheer necessity of having a simple way to share links and other stuff (like pokemon team pastes) in many devices without having to login into any account. 

![](/content/leafbook01.png)

## So, how is the site made?

<div class="stack-icons">
	<img src="/icons/laravel.svg">
	<img src="/icons/vue.svg">
	<img src="/icons/bootstrap.svg">
	<img src="/icons/netlify.svg">
</div>

The site is a Single Page application made on Vue. The backend is a simple API made on Laravel. It uses Vuex to manage state, and severla other utility libraries. You can check more of it in the [project repo](https://github.com/bul-ikana/leafbook). 

Currently, the site is hosted in Netlify.
