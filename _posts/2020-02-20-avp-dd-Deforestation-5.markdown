---
layout: post
title:  "Audio-Visual Production: Particle System Mesh Spawning Issues"
date:   2020-02-20
author: Lewis Bond
categories: [Audio-Visual Production Dev Diary]
img: /Uni/AVP/Deforestation.jpg
thumb: /Uni/AVP/Oculus.png
published: true
---
<!--more-->

## Mesh Spawning Issues: Fire Particle System

Today I tried to get the particle system spawning from the terrain meshes but this was trouble some. I wanted to get the big terrain mesh and its vertices so I could spawn the fire at the point where the player is looking. This was then changed when I realised that I could get the particles to only spawn in that area of the mesh. 

I then had the idea of breaking down the mesh into smaller ones but the where Unity handles mesh I found confusing and I could get a way to get the sub meshes from the one big mesh. Since this is the case I have figure I will break down the terrain in Blender and then import it a a group of smaller meshes. 

Hopefully this will produce the effect I want.

[PREVIOUS BLOG POST](https://lbondi7.github.io/audio-visual%20production%20dev%20diary/avp-dd-Deforestation-4){: .btn}
[NEXT BLOG POST](https://lbondi7.github.io/audio-visual%20production%20dev%20diary/avp-dd-Deforestation-6){: .btn}
