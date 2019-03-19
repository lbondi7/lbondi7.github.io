---
layout: post
title:  "Mario Kart Dev Diary: Sound Manager"
date:   2019-03-19
author: Lewis Bond
categories: [Game Engine Programming Dev Diary, Mario Kart Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Sounds

For sounds I implemented a audio manager using the system locator class Matt implemented. The locator class allowed for anything within there to be called where ever it is needed so it made sence to put a getter to the Audio Manager in there instead of passing down through the scenes or instanciating it all over the place. This time the solution to an issue I had for saw when I took teh task of sounds had already been solved.

## Audio Manager

The Audio Manager has every sound in the game setup so whenever we need any sound it is just there in one location. For the time being it stores the sounds in different vectors. These are broken down by when the sound is used: menu sounds, game sounds, character sounds, misc sounds.
~~~
	std::vector<Sound*> m_menuSounds;
	std::vector<Sound*> m_gameSounds;
	std::vector<Sound*> m_characterSounds;
	std::vector<Sound*> m_miscSounds;
~~~
The constants header then stores multiple enums that allow the us to access the files we need. There is an enum for the catergory of sound eg. menu, game etc. There are then an enum for every catergory which stores an enum relating to the sound in the vector.
To play any sound for example the countdown, all we need to do now is just *Locator::getAudio()->Play(SOUND_TYPE::MISC, (int)SOUNDS_MISC::COUNTDOWN);*

</br>

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-6){: .btn}
