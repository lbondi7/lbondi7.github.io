---
layout: post
title:  "Mario Kart Dev Diary: Camera Class Clean Up"
date:   2019-03-28
author: Lewis Bond
categories: [Game Engine Programming Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Clean Up

The cameras were getting too hard coded and fixed so clean up on the cameras was important. 

### Previous Version

Previous the cameras had all be handled in a switch case. So it was massive and it handled every single type of camera. What I found was that it was too big and there were too many types. Such as a follow camera which looked at the player from a set distance away and a lerp version of the same type so instead of snapping to its position it lerped to it instead. This was implemented for multiple types of cameras and with each one having its own case in the switch it made the code bulky.

### Udpated Version

The code has been  updated so that now any code that is relevant to all the different cameras it executed first at the top and then any code that is specific to any is executed in the switch case. This reduced the code down a lot as well as removing necessary camera types. Any camera that had a lerp and a non lerp version was changed to all cameras moving using a lerp. This allowed for smoother transitions, and if the user wanted a camera to snap to a position then they could just set the lerp amount to one and it would update instantly as that value represents the lifetime percentage of the lerp. If that value is always 1 then it will be at the end of the lerp.



[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-9){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-11){: .btn}
