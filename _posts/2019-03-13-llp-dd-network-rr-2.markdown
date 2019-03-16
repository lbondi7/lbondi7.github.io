---
layout: post
title:  "Network Game Dev Diary: Sending Data"
date:   2019-03-13
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Network Game Dev Diary]
img: /Uni/LLP/RainforestRampageDevDiary/RainforestRampageCover.png
thumb: Uni/LLP/RainforestRampage/RainforestRampageThumb.png
published: true
---
<!--more-->

## Sending Data

Since our game has to support networking, it means that data must be send across different poeple on different computers. For this game, a server is used to store the data on shich is then sent all the clients which updates their game. This a safer method than peer to peer as it stops people changing the data that will be sent, so therefore cheating is reduced, as the server can check if the information sent is correct before sending it all to the other clients. 


## Packets

The data is sent using enet. I have implemented a packets class (recomended by my lecturer), to send data across so any type of data can be streammed into it, it gets sent across to the other players then, gets streammed out in the order it was streammed in. I advanced on this by adding in a packet id as an enum, which is sent along with the packet and when streammed out, it tells the client or server what kind of data this is.


## Data

Since the packets can contain any type of data, I decided to use structs, which contain the data which is needed to be sent. Each part of the game will have a differnt struct such as the player, map, cards, tiles, chat room etc. This allows for teh data to be sent but in an organised fashion and can easily be accessed once the client or server recieve it. 

~~~
struct PlayerData
{
  int lives = 0;
  int score = 0;
  int tile = 0;
};
~~~

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/network%20game%20dev%20diary/llp-dd-network-rr-1){: .btn}
