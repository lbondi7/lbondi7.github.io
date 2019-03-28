---
layout: post
title:  "Network Game Dev Diary: Reconnecting"
date:   2019-03-28
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Network Game Dev Diary]
img: /Uni/LLP/RainforestRampageDevDiary/RainforestRampageCover.png
thumb: Uni/LLP/RainforestRampage/RainforestRampageThumb.png
published: true
---
<!--more-->

## Reconnecting

For the game, one of the requirements is to allow a player to disconnect and reconnect. For this, I used a bool on the server that gets set to true when a player disconnects. This triggers the game core state to go to the disconnection state and sends a similar state to all the players. In this state not data is sent or receive by either the server or the players until the disconnected player rejoins or is timed out. When the payer first connects to the server, it collects their ip address and stores it so when they try and reconnect it checks the stored ip address against the reconnecting client. If they match then it allows them to join in the game again. If the player doesn't reconnect in time then it sets a bool on the player to false and all other players ignore them when udating.

## Images

<center>
	<figure>
<a href="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/PlayersTurn.gif"><img src="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/PlayersTurn.gif" width = "600" height = "338"></a>
		<figcaption>The map displaying on the client.</figcaption>
	</figure>
</center>

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/network%20game%20dev%20diary/llp-dd-network-rr-5){: .btn}
