---
layout: post
title:  "Ex-Machina Game Dev Diary: Reading and Writing from a File"
date:   2019-02-16
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Ex-Machina Dev Diary]
img: /Uni/LLP/Ex-MachinaDevDiary/Ex-Machina.jpg
thumb: /Uni/LLP/Ex-Machina/Ex-Machina.png
published: true
---
<!--more-->

## Writing to a file

Writing to file was done after the foundations for the level builder had been implemented. All the data from the objects, player and the settings for the level were put together into a buffer and then written to a .dat file. The player.dat file would look similar to what is shown below but would have the values there instead.

~~~
player texture,
player tag,
player x position,
player y position,
player width,
player height,
player jump,
player size change,
player dash,
player invert gravity;
~~~

## Read from file

Read from file proved a lot more difficult, the level designer wouldn't be able to load the levels no matter what I did. What I realised is that I was mounting the files wrong as the ASGE framework uses its own file input/output system. When I mount a folder it mounts all the sub folders as well. So before, when I attempted mounting, I was trying to mount a sub-folder when the root folder hadn't been mounted yet so it couldn't sccess the folder I wanted to mount.



<center>
	<figure>
	    <a href="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/loadLevel.gif"><img src="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/loadLevel.gif" height="400"></a>
	    <figcaption>Loading a level in the level builder.</figcaption>
	</figure>
</center>

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-8){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-10){: .btn}
