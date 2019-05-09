---
layout: post
title:  "Mario Kart Dev Diary: Blender Camera Positioning"
date:   2019-05-06
author: Lewis Bond
categories: [Game Engine Programming Dev Diary, Mario Kart Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Cinematic Cameras

At first the cinematic cameras were hard coded. This was for the BETA to show off that we had cinematic cameras but it was specifically designed for Mario Kart Stadium and thats it. 

This was changed when the blender plugin was complete. It allowed for the user to position two cameras in blender and a look at point, save those values, read them in to Direct X and get the cinematic camera to follow those positons. The gif below shows the blender tool in action. The user clicks to create the cameras and the look at position and the camera always point to where the look at position is. This allows the easier visualisation of how the cinematic will look.

<center>
	<figure>
<a href="/assets/img/blog/Uni/GEP/MarioKart/BlenderPlugin.gif"><img src="/assets/img/blog/Uni/GEP/MarioKart/BlenderPlugin.gif" width = "600" height = "338"></a>
	</figure>
</center>


This was done by storing a vector of Vector3 and when reading in the data from a json file. The cinematic camera loops through until it is finished. This allowed the user to customise cinematic camera intros for any track they imported or created, allowing for any amount of cinematic cameras. The gif below shows the cinematic cameras that were set up using the blender plugin for Mute City.

<center>
	<figure>
<a href="/assets/img/blog/Uni/GEP/MarioKart/MuteCityCine.gif"><img src="/assets/img/blog/Uni/GEP/MarioKart/MuteCityCine.gif" width = "600" height = "338"></a>
	</figure>
</center>

[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-12){: .btn} [POST MORTEM](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/post%20mortem/gep-mariokart-post-mortem){: .btn}
