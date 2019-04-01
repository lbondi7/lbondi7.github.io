---
layout: post
title:  "Network Game Dev Diary: States"
date:   2019-04-01
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Network Game Dev Diary]
img: /Uni/LLP/RainforestRampageDevDiary/RainforestRampageCover.png
thumb: Uni/LLP/RainforestRampage/RainforestRampageThumb.png
published: true
---
<!--more-->

## States

The GameCore (server side) and the GameScene (client side) cpps were getting too big and unreadable. To sort this I changed the switch case I had with teh states in different classes all inheriting from an abstract state class (similarly to my scenes). Teh code in teh switch case was moved and it cleaned up the cpp. Now to update the game the code is ..

~~~
  state[static_cast<int>(current_state)]->update();
~~~

## Issue

A problem occured when I needed to send packets back to the client. I had fucntions that did this is in the game core called <i>sendMap()</i>, <i>sendPlayers()</i>, etc. But with the code now in different classes I couldnt call these fucntion as they were in the game core and I needed access to them in each state. This would of meant duplicating the code and having the same fucntion for each class. The code was put in a namespace called Packet Compiler and whenever I want to send a packet to a client I call this one of these fucntions from the namespace and it sends the data to the clients.

~~~
    PacketCompiler::sendPlayerTurn(server, *current_player_turn);
~~~

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/network%20game%20dev%20diary/llp-dd-network-rr-6){: .btn}
