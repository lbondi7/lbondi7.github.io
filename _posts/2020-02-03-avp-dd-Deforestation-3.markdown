---
layout: post
title:  "Audio-Visual Production: Burning the Trees"
date:   2020-02-03
author: Lewis Bond
categories: [Audio-Visual Production Dev Diary]
img: /Uni/AVP/Deforestation.jpg
thumb: /Uni/AVP/Oculus.png
published: true
---
<!--more-->

## Withering Trees

Today the burning effect on the trees was implemented. In the scene when the fire will touch the trees they will slowly start turning black and shrinking slightly. The leaves on the trees will rapidly shrink and will fade out eventually the signify they have all been burned away.

A timer will be triggered whenever a particle from the fire will hit a trunk or the leaves as each have a mesh collider. This timer will start counting down till it reaches 0 and in that time the burning effect will occur.

<center>
	<figure>
	    <a href="/assets/img/blog/Uni/AVP/witherTree.gif"><img src="/assets/img/blog/Uni/AVP/witherTree.gif" height="300px"></a>
	    <figcaption>The gif shows how the trees will look when burning gradually and withering away.</figcaption>
	</figure>
</center>
<br/>
I had an issue with the model as when shrinking the leaves, since it is a child of the trunk and its pivot point was not located on the end of the branch, originally when the tree shrank, the leaves would get left behind. They would end up floating in the air whilst the tree was shrinking, so I had to go into blender to change the pivot points.

[PREVIOUS BLOG POST](https://lbondi7.github.io/audio-visual%20production%20dev%20diary/avp-dd-Deforestation-2){: .btn}
[NEXT BLOG POST](https://lbondi7.github.io/audio-visual%20production%20dev%20diary/avp-dd-Deforestation-4){: .btn}
