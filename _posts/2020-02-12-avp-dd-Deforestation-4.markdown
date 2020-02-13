---
layout: post
title:  "Audio-Visual Production: Testing the Particle System"
date:   2020-02-12
author: Lewis Bond
categories: [Audio-Visual Production Dev Diary]
img: /Uni/AVP/Deforestation.jpg
thumb: /Uni/AVP/Oculus.png
published: true
---
<!--more-->

## Fire Particle System

Today was all about testing the fire particle system we have implemented. I was seeing what would look best for it when changing different parameters such as the size of the emitter (are where the particles are generated), the size of the particles overtime (whether that changing or remaining constant) and more.

<center>
	<figure>
		<a href="/assets/img/blog/Uni/AVP/smallFire.jpg"><img src="/assets/img/blog/Uni/AVP/smallFire.jpg" height="200px"></a>
	    <figcaption>This image shows the fire particle system that is being used without any modifications.</figcaption>
	</figure>
</center>
<br/>

After changing some parameters to see how the particle system looked, the emitter was then changed to be the mesh of objects that are designed to catch fire such as the land and the trees. This worked well and so can be used for when implementing a more dynamic fire system.

<center>
	<figure class = "half">
		<a href="/assets/img/blog/Uni/AVP/treeFire.jpg"><img src="/assets/img/blog/Uni/AVP/treeFire.jpg" height="50px"></a><a href="/assets/img/blog/Uni/AVP/terrainFire.jpg"><img src="/assets/img/blog/Uni/AVP/terrainFire.jpg" height="50px"></a>
	    <figcaption>These images show the fire particles being instantiated using the mesh of the tree (left) and the terrain (right).</figcaption>
	</figure>
</center>
<br/>

Next is actually implementing the fire system. It is going to be started from when the user looks at one place for long enough then the fire will eventually start. Then, the fire starts spreading and any tree, bush or land it interacts with will be set alight. There will have to be restrictions though as it might be beyond the Oculus to simulate all these particle systems. To counter this, maybe only the trees/vegetation will be set on fire.

[PREVIOUS BLOG POST](https://lbondi7.github.io/audio-visual%20production%20dev%20diary/avp-dd-Deforestation-3){: .btn}
[NEXT BLOG POST](https://lbondi7.github.io/audio-visual%20production%20dev%20diary/avp-dd-Deforestation-5){: .btn}
