---
layout: post
title:  "Mario Kart Dev Diary: Sprites"
date:   2019-03-14
author: Lewis Bond
categories: [Game Engine Programming Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Sprites

Getting multiple sprites rendering on the screen for each player was my target today. I was over thinking all the time as with direct x it renders sprites using a batch, so it has a batch of sprites which is sent to the renderer to be rendered. Since I had done the splitscreen by having multiple viewports and cameras which render all the obejcts separately. I applied this logic to the sprites thinking I needed multiple batches to render the sprites on different viewports, so I implemented this and realized that if each player has its own sprite batch, then every sprite for every player will get added to each batch. So every player will render every sprite. Also the renderer would receive multiple batches so it would be horribly inefficient.  

## Solution

A simple solution was realized, as all that was needed was one batch with each sprite being made into an array. The viewport the sprite batch uses being separate from the viewports for rendering the 3D models and positioning each sprite in the array over the viewport correlating with the number in the sprite array and viewport array.

~~~
		test[i] = new ImageGO2D(_RD, "twist");
		test[i]->SetScale(0.25f*Vector2::One);
		test[i]->SetPos(Vector2(_WD->m_viewport[i].TopLeftX, _WD->m_viewport[i].TopLeftY));
		m_2DObjects.push_back(test[i]);
~~~

## Image

<center>
	<figure>
<a href="/assets/img/blog/Uni/GEP/MarioKart/Sprites.png"><img src="/assets/img/blog/Uni/GEP/MarioKart/Sprites.png" width = "600" height = "338"></a>
		<figcaption>Sprites rendering to different screens.</figcaption>
	</figure>
</center>

[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-5){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-7){: .btn}
