---
layout: post
title:  "Mario Kart Dev Diary: BETA"
date:   2019-03-21
author: Lewis Bond
categories: [Game Engine Programming Dev Diary, Mario Kart Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## BETA

For the BETA we have a stripped back version of the mario kart. It had one track that was playable but had a lot of the functionality found in the original. There were a range of systems that we had implemented in the BETA to be able to produce a game similar to mario kart.

### Systems

- Toolkit
- Physics System
- Camera System
- Item System
- Sounds System
- UI System

#### Toolkit

The toolkit is used as the asset pipeline so it imports all our models, sprites, sounds or any data that we need the toolkit is also used to organise and change the json files that use to store all the data for the game.

#### Physics System

The physics showed how we got track collision working so it allowed th kart to be able to go around track such as Mario Kart Stadium fine as it used a ray cast to check if its near the track and then it would stick to it. 

#### Camera System

The camera system showed off the different cameras we had in the game such as a cinematic cam for the intros, a follow cam for each player and a orbit which span around the player once they had crossed the finish line.

#### Item System

The items work in the same way to the original mario kart in that a player would go through an item box to pick up an item and then be able to use that item when they pressed a certain button.

#### Sounds System

The sounds system is used to play certain sound effects or music at certain points in the game.

#### UI System

The system displayed all the information that a player needs to know such as their current lap, position and what item they have. This what specific to each player.


[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-8){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-10){: .btn}
