---
layout: post
title:  "Ex-Machina Game Dev Diary: Tools"
date:   2018-12-20
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Ex-Machina Dev Diary]
img: /Uni/LLP/Ex-MachinaDevDiary/Ex-Machina.jpg
thumb: /Uni/LLP/Ex-Machina/Ex-Machina.png
published: true
---
<!--more-->

## Level Designer

Since the game included a level I made a tried making a level builder to test it out as that is my main contribution to the project. A tool was made to help with the design of the levels so we can just drag and drop some objects and save us drawing out each level of our game. This allowed for me to test out a basic level builder as well. The tool was built using ASGE and free assets from kenny. 

[Kenny Assets](https://www.kenney.nl/assets){: .btn}

### The Tool (Images)

<center>
	<figure>
	    <a href="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/MenuScene.PNG"><img src="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/MenuScene.PNG" height="400"></a>
	    <figcaption>The menu is used to display the controls for the tool.</figcaption>
	</figure>
  </center>
  <br/>
  <center>
	<figure>
	<a href="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/LevelBuilderScene.PNG"><img src="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/LevelBuilderScene.PNG" height="400"></a>
	    <figcaption>The level builder is used to help us with designing levels.</figcaption>
	</figure>
</center>


A user can just drag and drop items in the scene using the list of objects on the left. When the user clicks it spawns in the object. The user can then drag it around by clicking and holding and then dragging. The user can also change the size of the object by clicking adn holding the small sqaure at the bottom right corner of the object. the user cna also change the psosition of all the objects clicking and ragging the background and changes the world offset. It uses a snap to function that can also be changed so user can make it snap to from 16 to 128.


[PREVIOUS BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-2){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-4){: .btn}
