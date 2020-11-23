---
layout: project
title:  "CPU Ray Tracer"
date:   2020-04-15 12:00:00
author: Lewis Bond
categories: 
- project
tagged: Ray Tracer, AT, UWEGames, C++, University
website: https://github.com/lbondi7
img: Uni/AT/title2.gif
carousel:
- Uni/AT/RayTracer.PNG
- Uni/AT/RayTracer2.PNG
abstract: A CPU ray tracer built using c++.
published: true
---

## CPU Ray Tracer C++

---

## Features

- Ray Tracer
- C++
- GPU programming
- Area Lighting
- BVH

<center>
<figure>
    <a href="/assets/img/project/Uni/AT/RayTracer3.PNG"><img src="/assets/img/project/Uni/AT/RayTracer3.PNG" width="448" height="252"></a>
    <figcaption>An area light being used to illuminate a dog.</figcaption>
</figure>
</center>

This project was to create a CPU ray tracer that uses a BVH to illuminate a scene with models. Materials were also implemented to make the surface more realistic. 

The rays were fired out from the camera origin through the image plane and returns all the hits on objects. When the ray hits an object it fires off multiple rays (shadow rays) in the direction of the light (only 1 if it is a point light) and returns the sum of these divided by the number of shadow rays. The pixel is then set to the colour that is returned.

A BVH (bounding volume hierarchy) is used in the to make it for efficient for collisions between the ray and objects. It generates bounding boxes around groups of triangles based of the cost of checking collisions (traversal cost). Then smaller bounding boxes are created around smaller groups of triangles within the larger groups. This continues until the traversal cost is lower than just looping through the triangle. The BVH is then traversed using nodes which connect to each other.

<center>
<figure>
    <a href="/assets/img/project/Uni/AT/bvh.png"><img src="/assets/img/project/Uni/AT/bvh.png" width="448" height="252"></a>
    <figcaption>(Source - NVidia): A BVH example thats shows the multiple levels of bounding boxes and nodes.</figcaption>
</figure>
</center>
---

## What I Learned

 - Consolidated my understanding of C++
 - Introduced me to Ray Tracing
 - Improved my understanding of 3D maths
 - Introduced me to spatial data structures
 
---
