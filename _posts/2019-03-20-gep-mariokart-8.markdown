---
layout: post
title:  "Mario Kart Dev Diary: Way-points"
date:   2019-03-20
author: Lewis Bond
categories: [Game Engine Programming Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Way-points

The way-points are used for multiple aspects of our game.

 - Player position/ranking
 - Increment player's lap
 - Reset the player
 - Some items (red shell/blue shell)

This utilities the positions imported from blender to place where the way-points are and then a oriented bounding box is placed at that point. This is used to increment the way-point integer on the player whenever they enter the way-point, and then that, a lap integer the player has and the position is used to calculate when they're current ranking in the race is. Once the player enters the last way-point then the lap integer increments.

## Issue

At the moment, there is a issue importing the position and rotation from blender as it uses a different orientation system so I am having trouble getting the rotation right. A temporary solution for the BETA tomorrow was to make the bounding boxes massive so they cover enough of the track but this will change for the gold release as we hope to have the rotation importer working by then so the bounding box will only need to be a certain size.

## More Uses

Toby and Evan are handling items but they are thinking of using the way-points as a way to make the red and blue shells go around the track until they reach the target player. That system might involve a clever hybrid of the way-points and the system they are using for the NPCs in the game.


[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-7){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-9){: .btn}
