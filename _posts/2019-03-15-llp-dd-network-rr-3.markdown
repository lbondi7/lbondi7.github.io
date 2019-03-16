---
layout: post
title:  "Network Game Dev Diary: Board"
date:   2019-03-15
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Network Game Dev Diary]
img: /Uni/LLP/RainforestRampageDevDiary/RainforestRampageCover.png
thumb: Uni/LLP/RainforestRampage/RainforestRampageThumb.png
published: true
---
<!--more-->

## Board

The board will be genrated server side since the update and initilisation of the game is done there. Since the board is made up of hexagonal tiles, there were two ways of positioning the tiles. The first way was through pre-defined positions on the screen that the tiles will be set to, the second was via pseudo-random generation. This is where a tile would be placed randomly on the board, but would have to be connected to another tile for that position to be valid. This meant implementing an algorithm that calculated a position next to one of the tiles already on the board, with the correct orientation. As the tiles were hexagonal this made it way too complicated for the time that there was to make the game. So pre-defined positions were chosen.

## Pre-defined Positions

The positions are stored in a 2D array that has 59 elemenets and 2 elements for each one of them (temporary solutuion but these will be read in from file). These are to store the coordinates (x and y). When the server is initilised it calls a function that sets integer which then depening on that integer, loops through an array in a map struct (which holds the x pos and y pos for each tile) and sets the positions. 
~~~
  int map_num = 0;

  for (int i = 0; i < 36; ++i)
  {
    map.xpos[i] = tile_pos[map_num[map_num][i]][0];
    map.ypos[i] = tile_pos[map_num[map_num][i]][1];
  }
~~~

This data is then passed to each client, which holds a map class, in wich there is an array of tiles and this data is given to them to set their positions. Then the client renders them out.

## Images


~~~

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/network%20game%20dev%20diary/llp-dd-network-rr-2){: .btn}
