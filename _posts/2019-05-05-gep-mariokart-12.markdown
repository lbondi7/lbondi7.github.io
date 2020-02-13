---
layout: post
title:  "Mario Kart Dev Diary: Sounds by Tag"
date:   2019-05-05
author: Lewis Bond
categories: [Game Engine Programming Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Sounds

The sounds were called by sending two enums. The first was tell the user what sound type it is and the second was to tell which sound needed to be played. The sounds were stored in different vectors depending and type of sound it was. There was a vector a game sounds, a vector for menu sounds etc. So the first enum decided which vector it was going to get and the second enum decide which element in the vector was being called. This system worked but relied on the vector storing the correct sounds and the sound that part of the vector matching the enum.

### Tag Based

This was changed to a tag based system where each sound now had a tag and the user would call the play function and give it tag. Instead of there being multiple vectors, there was one that stored all the sounds. The audio manager would then loop through the vector of sounds it stored until the string matched the tag of a sound in the vector. This method was much better as it meant it didn't rely on the enum matching the correct element in the vector. However it does mean the user has to get the tag absolutely correct in order for the sound otherwise it will do nothing, also the fact it loops through the vector. If this was a large game with  massive amount of sounds then it would definitely be inefficient but for the amount of sounds in the game it is fine.

[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-11){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/gep-mariokart-13){: .btn}
