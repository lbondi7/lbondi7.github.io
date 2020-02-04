---
layout: post
title:  "Audio-Visual Production"
date:   2020-01-31
author: Lewis Bond
categories: [Audio-Visual Production Dev Diary]
img: /Uni/AVP/Deforestation.jpg
thumb: /Uni/AVP/Oculus.png
published: true
---
<!--more-->

## Camera Movement

This week I implemented camera movement to enable us to test the project without having to Oculus setup yet. This enables us to look around as it follows the mouse's movement, as the gif below shows. A ray cast has also been setup that fires from the camera's position and in the direction the camera is facing. This ray cast will be used to produce a fire particle system, which when it interacts with the environment (trees and bushes) it will burn. That will be the next task me.

<center>
	<figure>
	    <a href="/assets/img/blog/Uni/AVP/cameraMovement.gif"><img src="/assets/img/blog/Uni/AVP/cameraMovement.gif" height="300px"></a>
	    <figcaption>The gif show the camera movement with is following the mouse.</figcaption>
	</figure>
</center>
<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/audio-visual%20production%20dev%20diary/avp-dd-Deforestation-1){: .btn}
[NEXT BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/AVP-dd-ExMachina-3){: .btn}
