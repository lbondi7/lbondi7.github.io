---
layout: post
title:  "Mario Kart Dev Diary: Waypoints"
date:   2019-03-20
author: Lewis Bond
categories: [Game Engine Programming Dev Diary, Mario Kart Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Waypoints

The waypoints are used for multiple aspects of our game.

 - Player position/ranking
 - Incrementing player's lap
 - Reseting the player
 - Some items (red shell/blue shell)

This utilises the positions imported from blender to place where the waypoints are and then a oriented bounding box is placed at that point. This is used to increment the waypoint integer on the player whenever they enter the waypoint, and then that, a lap integer the player has and the posiiton is used to calulate when they're current ranking in the race is. Once the player enters the last waypoint then the lap integer increments.

## Issue

At the moment, there is a issue importing the position and rotation from blender as it uses a different orientation system so I am having trouble getting the rotation right. A temporary solution for the BETA tomorrow was to make the bounding boxes massive so they cover enough of the track but this will change for the gold release as we hoep to have the rotation importer working by then so the bounding box will only need to be a certain size.

## More Uses

Toby and evan are handling items but they are thinking of using the waypoints as a way to make the red and blue shells go around the track until they reach the target player. That system might involve a clever hybrid of the waypoints and the system they are using for the NPCs in the game.


[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-7){: .btn}
