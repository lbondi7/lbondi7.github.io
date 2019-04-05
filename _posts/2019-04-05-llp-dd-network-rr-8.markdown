---
layout: post
title:  "Network Game Dev Diary: Input IP Address"
date:   2019-04-05
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Network Game Dev Diary]
img: /Uni/LLP/RainforestRampageDevDiary/RainforestRampageCover.png
thumb: Uni/LLP/RainforestRampage/RainforestRampageThumb.png
published: true
---
<!--more-->

## IP Address

When connecting to the server, each clients needs the ip address of the server in order to connect to it. As default it uses localhost which gets the ip of the local server, this is an issue when trying to connect to a server on a different computer. In order to accomplish this in the menu when the player presses enter they go to a page where they have to input their username and the ip address of the server they want to connect to. I use the service locator which stores teh username and ip adress and when they press enter the service locator is called and the ip address is given to client to connect to that server.

<center>
	<figure>
<a href="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/InputIP.gif"><img src="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/InputIP.gif" width = "600" height = "338"></a>
		<figcaption>The user inputting the IP address.</figcaption>
	</figure>
</center>

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/network%20game%20dev%20diary/llp-dd-network-rr-7){: .btn}
