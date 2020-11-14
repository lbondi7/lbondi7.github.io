---
layout: project
title:  "Vulkan Particle System"
date:   2020-05-01 12:00:00
author: Lewis Bond
categories: 
- project
tagged: Vulkan, CTP, UWEGames, C++, University
website: https://github.com/lbondi7
img: Uni/CTP/title.gif
carousel:
- Uni/CTP/flowfield.PNG
- Uni/CTP/dog.PNG
- Uni/CTP/heart.PNG
- Uni/CTP/flowfield3.PNG
abstract: A Particle System built in Vulkan that runs on the GPU. 
published: true
---

## Vulkan GPU Particle System C++

---

## Features

- Vulkan
- C++
- GPU programming
- Dynamic Lighting
- Different Models

<center>
<figure>
    <a href="/assets/img/project/Uni/CTP/bunny.gif"><img src="/assets/img/project/Uni/CTP/bunny.gif" width="448" height="252"></a>
    <figcaption>The particles swirling together and forming a bunny.</figcaption>
</figure>
</center>

This project was to get a particle system on the GPU using Vulkan with real time dynamic lighting. The particles move about and form different shapes using a signed distance function. This was used to get the closest triangle on the model and then barycentric coordinates were used to get a random point on the triangle. The particle system was passed as vertex inputs into the vertex shader but n used a storage buffer for the compute and fragment shader.

Dynamic lighting was implemented with the use of PBR. A roughness and metallic value was passed in and the colour value of the particles were used to illuminate the plane.  

---

## What I Learned

 - Consolidated my understanding of C++
 - Introduced me to Vulkan
 - I learned a lot about the different aspects of GPU programming 
 - Improved my understanding of 3D maths
 - Physically Based Rendering 
 - Forced me to learn about spatial data structures. 
 
---

## Gameplay

<iframe width="448" height="252" src="https://www.youtube.com/embed/ceDCeDINXao" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

---

#### Links



---

**This game was made for educational purposes, for me show my improvement as a games developer and so this was not made for any commercial purposes.** 
