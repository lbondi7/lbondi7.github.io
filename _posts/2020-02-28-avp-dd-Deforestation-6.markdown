---
layout: post
title:  "Audio-Visual Production: Burning Trees"
date:   2020-02-27
author: Lewis Bond
categories: [Audio-Visual Production Dev Diary]
img: /Uni/AVP/Deforestation.jpg
thumb: /Uni/AVP/Oculus.png
published: true
---
<!--more-->

## Burning Trees

I managed to implement the complete system for burning the trees completely with the withering, the particle system and the leaves being destroyed completely.

<center>
	<figure>
		<a href="/assets/img/blog/Uni/AVP/treeBurningEffect.gif"><img src="/assets/img/blog/Uni/AVP/treeBurningEffect.gif" height="300px"></a>
	    <figcaption>This gif shows the wither effect and the tree burning working together.</figcaption>
	</figure>
</center>
<br/>

This will need to be improved as it will probably tank the Oculus Quest with their being so many particle systems. Maybe extending the fire manager is required in order to achieve an effect, without destroying the frame rate.

Implementing the fire burning the terrain mesh is next, the idea with that is to split the mesh up into smaller meshes. With this the user will look at each section and only that section will burn.

[PREVIOUS BLOG POST](https://lbondi7.github.io/audio-visual%20production%20dev%20diary/avp-dd-Deforestation-5){: .btn}
[NEXT BLOG POST](https://lbondi7.github.io/audio-visual%20production%20dev%20diary/avp-dd-Deforestation-7){: .btn}
