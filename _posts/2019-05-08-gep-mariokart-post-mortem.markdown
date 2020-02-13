---
layout: post
title:  "Mario Kart Dev Diary: Post Mortem"
date:   2019-05-08
author: Lewis Bond
categories: [Game Engine Programming Dev Diary, Mario Kart Dev Diary, Post Mortem]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Post Mortem

### What Went Well
Overall he game and systems produced were extremely good with some being exceptional. All of them fitted in quite well with each other and worked together to produce a good quality game.

#### Toolkit

The toolkit that was produced is extremely useful in importing assets and aiding other systems. It is slightly confusing at first to find where everything is but after using it a few times it becomes very clear and is easy to use. The handling of model, images, sounds, text, cube-maps and fonts is very impressive and easy. With loading the model in the code being easy as well with the GameFilepaths class, which returned the file-path after giving it a string and what file is needed. It's extremely flexible and allows for anyone to come in and configure the game with ease. Not only dealing with asset importing but also adding configurations for grouping assets together. So, an image is grouped to a model and this allowed for easy coordination from choosing which character in the menu to loading the correct model in the game scene. This is just a very powerful and useful system.

#### Mesh Collision
The track collision is a strong system that works very well as all the cars collide and don’t fall through the mesh. It is a complex system but very well implemented. It is optimized so even when multiple karts are on the track it still works and there is no lag or delay. The way it was implemented allows the karts to go up the different surfaces and even upside down. The use of the multiple ray-casts to detect whether the player is on the track or into is great and was also used for the items. The system was exactly what was needed and works well with other systems, so it was good.  

#### AI
The AI that was implemented worked with every track that was used. Projection was used to path a track for the AI so that it would stay on the correct course. If its projection was hitting a surface that not part of the track then it would turn as best it could to avoid going that way. and Using the way-points to navigate around the track was very useful as the same system was implemented into the red shells. The AI not only were able to navigate around the tracks but also use items although this system wasn’t as complicated as moving around the track it still was impressive and added to the game none the less. 

#### Box Collision
The box collision that was implemented was very good and stopped players from clipping. The OBB collision detection allowed for accurate detection and response. The system didn’t affect the performance of the machine at all, so it was well optimized. When a player hit another, they collided off and went in opposite directions giving a nice fell to the game. This also worked well the AI system as it meant when an AI was hit, they would get knocked off and then must readjust giving them a more real feeling.

#### Items
The items system worked and added to the game. Since it is s bespoke system for Mario kart, it is very hard to make it a generic system that can be completely flexible. It was hard coded in some parts but again that was due to it being a very specific system found in Mario Kart, but other than that it was great. It worked well and had probability correct for each player depending on their position, all the items worked and acted the way that they should. The red shell at first had a serious impact on performance due to it loading in a new AI but in the end it worked fine and didn’t have a problem at all.

#### Cameras
The camera system worked well and allowed for different ways for the camera to behave such as a follow cam, cinematic cam, first person cam and more. It was nearly all data driven with some parts needing to be hard coded such as the orbit cam spinning around the player and the cinematic cam moving between different points in a vector. It worked well and captured the feel of Mario kart but also some extra finesse with the cinematic cameras and the orbit camera.

### What Could Be Improved
There are a few things that could be improved about. These are systems that are not bad by any means but could improved to a point where they are more useful.

#### Sound System
The sound system worked and worked well as it allowed for the any sound effect or music to be played at any point, so it made it flexible. It also read in all the sounds and data for the sounds from a file which was good. However, it used a string-based tag system which was a pain to call, as the person had to get the string correct otherwise it would fail. It also could have been improved by mapping the string to a sound so instead of looping through the vector of sound until the tags matched it just played the sound that mapped to string that was passed. 

#### Scene Manager
The scene manager ended up working and well. It allowed for multiple scenes to loaded and a loading screen and an attract state if the player is AFK. However, it is a bit messy and isn’t as structured as it should be this is because of Direct X not liking the deletion memory. The first iteration of the scene manager kept crashing when trying to delete memory, so the work around was to wait a period before deleting anything. In the end all the scenes are loaded at the beginning, but any tracks or models will be loaded as the scene transitions, in the expensive load and unload. In the end it wasn’t bad by any means but there are ways it could be improved. 


### What I Learned
I learned a lot about coding and how much I've improved over the last year especially the last couple of months.

#### Direct X
I learned about how to use Direct X and how it works. It was a hard task but in the end it was worth it be able to use a powerful piece of software. From 3D rendering of objects to back buffers and memory management by Direct X, I learned a lot from this.

#### Teamwork
I learned how vital it is working as a team especially on big projects like this as one person could not produce the project we have. Having a mixture of skills in the teams helps from people who are better at the maths, to people who are better with tools and making systems to help other people with their systems. This enables the group to work together and get on with the task. 


[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-13){: .btn}
