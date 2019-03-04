---
layout: post
title:  "Mario Kart Dev Diary: Orbit Camera"
date:   2019-02-28
author: Lewis Bond
categories: [Developer Diary, Game Engine Programming Dev Diary, Mario Kart Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Orbit Camera

When a person finshes a race in mario kart it lerps round to be in front of the player. The link below shows the effect. I have been working on an orbit camera to do this effect.
[MARIO KART EFFECT](https://youtu.be/GHz6s5iVpYU?t=469){:target="blank" rel = "noopener"}{: .btn}

Since it need to circle around the player I knew I needed to use trigonometry. As [Maths Is Fun](https://www.mathsisfun.com/algebra/trigonometry.html) shows I need to use the opposite and the adjacent to get the hypotenuse. Once I had this it was easy. The center of the model was used as the pivot and the angle was changed to make it spin around the kart. M_dpos was a vector3 used to put the camera a set distance behind the car and to get the x of this vector was used as the opposite, the z was used to get the adjacent.

~~~
angle += amount;
sin(angle / radian) * vector3.x;
cos(angle / radian) * vector3.z;
~~~

The angle is increased by an amount every frame and the angle is then divided by a radian. The sin and cos of that result is then multiplied by the respective vector axis to get the position. Just by increasing the angle the position of the camera changes as shown in the image below. 

<center>
	<figure>
<a href="/assets/img/blog/Uni/GEP/MarioKart/SplitScreen.gif"><img src="/assets/img/blog/Uni/GEP/MarioKart/SplitScreen.gif" height = "50"></a>
		<figcaption>Splitscreen in direct x.</figcaption>
	</figure>
</center>

## Problem

This issues with this method is that it uses two dimensional ths but i need it to work in three dimensions so what way eh cart is facing it will orbit at the amount I want. For this i will have to incorperate the matrix and orientation of the car so it orbits around no matter how teh car is rotated.

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-3){: .btn}
