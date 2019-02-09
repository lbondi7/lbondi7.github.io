---
layout: post
title:  "Ex-Machina Game Dev Diary: Level Builder Foundations"
date:   2019-02-09
author: Lewis Bond
categories: [Developer Diary, Low Level Programming Dev Diary, Ex-Machina Dev Diary]
img: /Uni/LLP/Ex-MachinaDevDiary/Ex-Machina.jpg
thumb: /Uni/LLP/Ex-Machina/Ex-Machina.png
published: true
---
<!--more-->

## Level Builder

I started on the level builder today. Its design is based of a mix of the level deisgner, mentioned in a previous dev diary, and the [particle editor](https://lbondi7.github.io/projects/GEA-Particle-System-Designer/){:target="blank" rel = "noopener"} I made for GEA. The foundations have started being implemented: clicking to spawn in the a new block, different blocks spawning in depending on which element in the menu was chosen, highlighting the selected block and draghging the block around the place.

<center>
	<figure>
	    <a href="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/LevelBuilderFoundations.gif"><img src="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/LevelBuilderFoundations.gif" height="400"></a>
	    <figcaption>The basics of the level builder.</figcaption>
	</figure>
</center>

### Problems

A problem that I encaounted when starting the level builder was to do with vectors. I used vectors for my user interface for the level designer but this time when I tried to implment my 2D vector I wanted it kept crashes due to missing sprite when clearing the temporary vector I used to push into the 2D vector. The code I used is shown below.

~~~
    for (int i = 0; i < 2; ++i)
    {
      ObjectVector temp_vector;
      for (int j = 0; j < 1; ++j)
      {
        temp_vector.push_back(GameObject());
      }
      objects_ui.push_back(temp_vector);
      temp_vector.clear();
    }
~~~

I couldn't figure out why there was a an problem with the sprite becuase the game objects in the vector weren't being given a sprite component at this point so it shouldn't be executing the code to delete the srpite of the game object. 

## Solution

I couldn't actually figure out what was this issue with the vector but in the end I used an array of game objects instead as I realised I didn't need a 2D vector as it would be wasting memory allocation. 

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-7){: .btn}
