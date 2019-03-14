---
layout: post
title:  "Mario Kart Dev Diary: More Cameras"
date:   2019-02-25
author: Lewis Bond
categories: [Developer Diary, Game Engine Programming Dev Diary, Mario Kart Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Camera 2.0

Carrying on with the cameras from last time, I am now trying to get it to display multiple cameras in order to get the split screen working. 

I figured out how to set the size of viewport and that the scissor rect is used to select what part of the viewport is rendered. 


<center>
	<figure class="half">
<a href="/assets/img/blog/GEP/MarioKart/veiwport1.png"><img src="/assets/img/blog/Uni/GEP/MarioKart/veiwport1.png" width = "300" height = "237"></a>

<a href="/assets/img/blog/GEP/MarioKart/viewport2.png"><img src="/assets/img/blog/Uni/GEP/MarioKart/viewport2.png" width = "300" height = "237"></a>
		<figcaption>The difference in the what is displayed when the scissor rect is changed.</figcaption>
	</figure>
</center>
<br/>

The first image shows the viewport normally and the second shows the viewport being 1.5x bigger than the window and and the rect being 1.1x bigger than the window.

These two variables, is what is needed to get the splitscreen working, but I havent quite figure out what needs to be done. Does there need to be multiple viewports to accommodate for multiple cameras or does using the scissor rect can one viewport being used with multiple scissors rects spliting up the screen.

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-1){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/developer%20diary/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-3){: .btn}
