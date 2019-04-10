---
layout: post
title:  "Network Game Dev Diary: Chatroom"
date:   2019-04-06
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Network Game Dev Diary]
img: /Uni/LLP/RainforestRampageDevDiary/RainforestRampageCover.png
thumb: Uni/LLP/RainforestRampage/RainforestRampageThumb.png
published: true
---
<!--more-->

## Chatroom

When connected to the server the players can send each other messages. This is done using the packet system mentioned in a previous post. Special streamming operaters had to be set up for sending strings across the network compared to other data like ints or chars. A string is a pointer to an array of chars if you tried to stream it in using the normal way of streamming thne it would give you memory location of the pointer and what would of been outputted was a load of nonsense that you couldn't understand or nothing at all.

~~~
// normal packet
    packet_data.insert(packet_data.end(), as_char, as_char + size);
    
// string packet
    packet_data.insert(packet_data.end(), string.data(), string.data() + string_length);
~~~

As you can see the string is passed in but we have to do string.data() in order to get the correct data. We can't do this in the normal packet as it uses a template class so it allows for anything and only the string is used that requires .data() after the variable has been passed in. Since we can't check what type of variable has been passed in with T, it is much esaier to have a separate functions for sending strings.

<center>
	<figure>
<a href="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/BasicChatroom.gif"><img src="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/BasicChatroom.gif" width = "600" height = "338"></a>
		<figcaption>The user talking to another player</figcaption>
	</figure>
</center>

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/network%20game%20dev%20diary/llp-dd-network-rr-8){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/network%20game%20dev%20diary/llp-dd-network-rr-10){: .btn}
