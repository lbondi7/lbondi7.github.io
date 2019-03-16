---
layout: post
title:  "Ex-Machina Game Dev Diary: Sound/Music"
date:   2019-02-19
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Ex-Machina Dev Diary]
img: /Uni/LLP/Ex-MachinaDevDiary/Ex-Machina.jpg
thumb: /Uni/LLP/Ex-Machina/Ex-Machina.png
published: true
---
<!--more-->

## Audio

For our game we wanted audio in order to enhance the experience. Audio in a game can be used to direct where a player is meant to go, signal that something has happened and you should be aware of it, adding more immersiveness to an enviroment and many more. This is why adding in the audio for our game was important. The links below hightlight the importance of having music and sound, in a game or a film, to improve the user's experience. 

[JAWS WITH AND WITH MUSIC](https://youtu.be/-fnq1s-babs){:target="blank" rel = "noopener"}{: .btn}
[THE SOUDN DESIGN OF HORIZON ZERO DAWN](https://youtu.be/SIAmi88akl0){:target="blank" rel = "noopener"}{: .btn}


## SoLoud

SoLoud was the engine that was used in the game. It was fairly simple to setup with just having to include a couple of lines in the cmake file in order to import the engine when the game builds. After that it is farily simple to get sound playing in the game. The files had to be included in the header file but then its was just initilising the component to play the sounds and loading the sounds in. 

~~~
## Header file syntax 

SoLoud::Soloud sound_player;
Soloud::Wav music;

## CPP file syntax

sound_player.init();
music.load();
sound_player.play(music);
~~~

Since our game had a retro synthwave theme we decided to go with the same kind of music, so we decided on songs M.O.O.N - Dust and Dynatron - Pulse Power. These two songs were the backing music to our game and gave that very distinct reto vibe we had for our game. The othe reason was that these songs both progressed to become grander and this helped for when playing the game as the player would be able to feel as they are proressing as well.

[Dust](https://www.youtube.com/watch?v=phL6fDiYNJk){:target="blank" rel = "noopener"}{: .btn}
[Pulse Power](https://www.youtube.com/watch?v=Ak1-qLbHHCM){:target="blank" rel = "noopener"}{: .btn}


## Issue

Once we implemented the music, the game soudned great and was working fine apart from one thing. It took forever to load up. This was down to the music and it was slowing the game down. It went from a couple of seconds to load up, to around 10-15 seconds. We knew it was the music but we thought instanciating multiple objects that have to load up and can access every sound possible might be slowing it down more. So we decided to pass the audio engine instead to each scene but that then interfered with the game scene. We didn't manage to get the issue sorted in the end but our lecturer pointed out that we hadn't compressed the audio and that's what was slowing down the load up, so next time we know to compress the audio.

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-9){: .btn}[EX-MACHINA GAME - POST MORTEM](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/post%20mortem/llp-dd-ExMachina-post_mortem){: .btn}
