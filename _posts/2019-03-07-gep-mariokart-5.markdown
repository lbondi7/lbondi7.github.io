---
layout: post
title:  "Mario Kart Dev Diary: Camera System"
date:   2019-03-07
author: Lewis Bond
categories: [Game Engine Programming Dev Diary, Mario Kart Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Camera System

The way the cameras were setup before was with the TPSCamera class inheriting from the Camera class but now I have done away with that and based the camera class upon the way the unity camera works. The unity camera can act as any type of camera the user wants as the [video](https://youtu.be/xvyrzwwU1DE){:target="blank" rel = "noopener"} shows.

The camera system I have implemented now allows the camera to up to 8 types of camera, including a fist person camera, a lerping follow camera, a cinematic camera or a camera that can fly around (although this is only used for debugging and checking the map works). All of these behaviours are stored in the camera class atm but if it gets too long I will make it a component based system with each part in a different class (for readability/organisational purposes).

~~~
	enum class BEHAVIOUR : int
	{
		BEHIND = 0,
		FRONT = 1,
		LERP = 2,
		FIRST = 3,
		INDEPENDENT_FIXED = 4,
		INDEPENDENT_LERP = 5,
		ORBIT = 6,
		CINEMATIC = 7,
		DEBUG_CAM = 8,
	};
~~~

## Orbit Camera Problem

I fixed the issue with the orbit camera, I was calculating the range of the orbit using the delta pos (the distance from the camera to the kart) added onto the kart's psotion instead of just delta pos. This is why the orbit stretched and changed because the karts position was changing.  

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-4){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/developer%20diary/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-6){: .btn}
