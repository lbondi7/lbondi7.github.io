---
layout: post
title:  "Mario Kart Dev Diary: Splitscreen!"
date:   2019-02-28
author: Lewis Bond
categories: [Game Engine Programming Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Splitscreen

Splitscreen is working!
Since the splitscreen need to accommodate for multiple cameras, multiple viewports were required. I figured out how to set the size of viewport and that the scissor rect is used to select what part of the viewport is rendered. Having multiple viewports is the method I used for rendering multiple cameras. Our lecture set up a pointer to a camera in the render data which is sent to render function as a batch to be drawn. The scissor rect is used to change the size of how much is rendered. The scissor rect has to be changed based on the size of the window but not the viewport.

<center>
	<figure>
<a href="/assets/img/blog/Uni/GEP/MarioKart/Splitscreen.png"><img src="/assets/img/blog/Uni/GEP/MarioKart/Splitscreen.png" width = "500" height = "284"></a>
		<figcaption>Splitscreen in Direct X</figcaption>
	</figure>
</center>
<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-2){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-4){: .btn}
