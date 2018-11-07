---
layout: post
title:  "PLAYGROUND PLATFORMER"
date:   2018-09-30
excerpt: "2D Endless Platformer made in Visual Studio."
tags: [Project, C++, Playground Platformer, ASGE, Visual Studio Project]
feature: /assets/img/Games/PlaygroundPlatformer/logo.png
project: true
published: true
---

**Playground Platformer** is a game I designed during summer 2018. It was made in visual studio using the ASGE framework I have been working with the previous year.

---

## Image Preview

{% capture images %}
    ../assets/img/Games/PlaygroundPlatformer/MainMenu.PNG
    ../assets/img/Games/PlaygroundPlatformer/EndScreenSingleplayer.PNG
    ../assets/img/Games/PlaygroundPlatformer/EndScreenMultiplayer.PNG
{% endcapture %} 
{% include gallery images=images caption="The images above show the menu screen and the end screens." cols=3 %}

{% capture images %}
    ../assets/img/Games/PlaygroundPlatformer/InGameMultiplayer.png
    ../assets/img/Games/PlaygroundPlatformer/InGameSingleplayer.png
{% endcapture %} 
{% include gallery images=images caption="The images above show the difference between singleplayer and multiplayer." cols=2 %}

---

## Features

It is a single and multiplayer game (local 2 player) where the aim is to get the highest score possible whilst without falling down. It is a endless platformer with a leaderboard so you can see where you have placed. This can be check via the main menu or right after the plaer loses as it displays the leaderboard with your position form the current attempt (if your score was high enough).

---

## Game Mechanics

Some of the game mechanics are the moving left, right and jumping but also include wall jumping, boosting and knock back.<br/><br/>
**Wall Jump** - The player can jump of either side of the game scene so if a platform is too far up to jump straight up there the player could use the wall to jump off and gain extra height.<br/><br/>
**Boost** - The boost is a horizontal boost left or right which enables the player to dash to platforms that they otherwise wouldn't be able to reach with a normal jump.<br/><br/>
**Knock Back** - This is only available in the multiplayer mode where the players can knock each other back with a by hitting them. If this happens the player that got hit will be forced backwards and slightly upwards potentially forcing them off the platform and into danger. Careful though both players both hit each at teh same time causing both players to be knocked back so if you want to go for a knock back you could potentially rick being hit back yourself.<br/><br/><br/>


**This game was made for educatonal purposes, for me show my improvement as a games developer and so this was not made for any commercial purposes.** 
