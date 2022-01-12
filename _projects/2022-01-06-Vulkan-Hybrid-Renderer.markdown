---
layout: project
title:  "Hybrid Soft Shadow Renderer"
date:   2022-01-06 12:00:00
author: Lewis Bond
categories: 
- project
tagged: Vulkan, Dissertation, UWEGames, C++, University
website: https://github.com/lbondi7
img: Uni/CTD/TreeCompareDebug2.png
carousel:
- Uni/CTD/DragonCompare.png
- Uni/CTD/DragonRRQSSTitle.png
- Uni/CTD/DragonRRQSSDebugTitle.png
- Uni/CTD/TreeRRQSSCulling.png
abstract: A Hybrid Soft Shadow Renderer that uses Shadow Mapping and Ray Tracing 
published: true
---

## Hybrid Soft Shadow Renderer using Shadow Mapping and Ray Tracing 

---

## Features

- Vulkan
- C++
- GPU programming
- Shadow Mapping
- Ray Tracing
- Ray Query
- Adpative Performance

<center>
<figure>
    <a href="\assets\img\project\Uni\CTD\DragonCompareTitle.png"><img src="\assets\img\project\Uni\CTD\DragonCompareTitle.png" width="448" height="252"></a>
    <figcaption>Comparion showing the the final result and the debug view of where areas are being ray traced.</figcaption>
</figure>
</center>

This project implemented a new algorithm for soft shadow rendering using shadow mapping and ray tracing. The RRQSS (Raster Ray Query Soft Shadow) algorithm estimates areas of shadow using PCSS (Percentage-Closer Soft Shadows), then utilises Vulkan Ray Query to ray trace these areas to obtain higher detailed shadows. The number of rays traced also depends on the shadow value, with fewer rays traced in the umbra than the penumbra.

---

## What I Learned

 - Shadow Maps
 - GPU Ray Tracing
 - Adaptive Performance based on frame rate
 
---

**This game was made for educational purposes, for me show my improvement as a games developer and so this was not made for any commercial purposes.** 
