---
layout: post
title:  "Network Game Dev Diary: Players"
date:   2019-03-18
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Network Game Dev Diary]
img: /Uni/LLP/RainforestRampageDevDiary/RainforestRampageCover.png
thumb: Uni/LLP/RainforestRampage/RainforestRampageThumb.png
published: true
---
<!--more-->

## Players

The players move about the board when the user clicks on a tile. There are turns in the game are determined by the server so for now the first player starts then it recieves that data and sends it out to all the other players as well as which players turn it is next. It just increments a value until it reaches the max players then resets it back to the first player. The data is sent via a packet. The packet contains the map and the player data which the server then updates it data and feeds it out to the other players.

## Images

<center>
	<figure>
<a href="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/PlayersTurn.gif"><img src="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/PlayersTurn.gif" width = "600" height = "338"></a>
		<figcaption>The map displaying on the client.</figcaption>
	</figure>
</center>

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/network%20game%20dev%20diary/llp-dd-network-rr-3){: .btn}
