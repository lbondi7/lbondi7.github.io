---
layout: post
title:  "Text Based Adventure Game Dev Diary: Post Mortem"
date:   2018-11-16
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Text Based Adventure Dev Diary, Post Mortem]
img: /Uni/LLP/TxBsdAdvenBlog/coverPage.png
thumb: /Uni/LLP/TxtBsdAdv/coverPageSmall.png
published: true
---

<!--more-->
# Text Based Adventure Game

<center>
<figure>
    <a href="/assets/img/blog/Uni/LLP/TxBsdAdvenBlog/TBAG.gif"><img src="/assets/img/blog/Uni/LLP/TxBsdAdvenBlog/TBAG.gif"></a>
    <figcaption>This just shows a snippet of the game.</figcaption>
</figure>
</center>

## Pros
<ul>
    <li>The scene manager worked well was my code for the game was separate from my menu so it was much cleaner.</li>
    <li>Reading in from txt files worked well and how I stored the room information was highlighted by my lecturer.</li>
    <li>The changing between rooms worked well as instead of having each room as a separate game object. Instead I instantiated 1 and updated its values as the player explored the ship.</li>
    <li>The astectics were also highlighted as different and very cool. I was going for a kind of a 80's computer terminal vibe that is seen in films like alien to go along with my abandoned spaceship theme. I then settled on a fallout design because it fitted perfectly with what I wanted and I also love the fallout games so it was kind of a homage to them.</li>
</ul>

## Cons
<ul>
<li>Some of my naming of variables was a bit unclear so people reading for the first time my not be sure what each one does.</li>
    <li>I had a bit of code which used multiple if statements instead of else if which isn't good for optimisation.</li>
    <li>My classes knew about each other which they shouldn't so I will change that from now on.</li>
    <li>Even though it was a text based adventure game, the lack of images meant there was a lot of dead space on the screen but I will ultilise it next time.</li>
    <li>The map was a bit unclear when it came to where the player was and where they could go. Multiple people got confused when using the map, as some rooms looked close together but actually you couldn't travel between them.</li>
</ul>

## Potential Improvements
<ul>
    <li>I could of added images to the game just to make it more pleasing and improve the feel of it. Maybe just a little pip boy character at the side if I wanted to go down the full fallout route.</li>
    <li>I would of changed some of my reading in from files as even though it was good it could of been optimised a lot more.</li>
    <li>I definately would improve my map so it blended in more with the background image and was more understandable.</li>
</ul>

## What I Learned
<ul>
    <li>I realised how much fun coding a text based adventure is even though it can be quite fidily. If you let your imagination do a lot of the work, with a text based adventure it is very easy to code what you want.</li>
    <li>It consolidated my understandting of pointers and how to use them as well</li>
    <li>It was also helpful in introducing me to a component based way of programming as I was constantly discussing with my lecturer how he would write it out. This ended up being very helpful and insightful on how someone with years of experience would do it.</li>
</ul>


[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/text%20based%20adventure%20dev%20diary/llp-dd-TBAG-5){: .btn}

[PROJECT](https://lbondi7.github.io/projects/LLP-TBAG/){: .btn}
