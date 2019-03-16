---
layout: post
title:  "Ex-Machina Game Dev Diary: Size Boss"
date:   2019-01-14
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Ex-Machina Dev Diary]
img: /Uni/LLP/Ex-MachinaDevDiary/Ex-Machina.jpg
thumb: /Uni/LLP/Ex-Machina/Ex-Machina.png
published: true
---
<!--more-->

## Size Boss
In order for the level builder to be finished, I needed the player and enemies completed in the game. This was a big part of our game and so I coded the size changing enemy boss. 

The aim for this level is too have the player get over different obstacles whilst having the boss moving all over the screen and if it touches the player, they get reset back at the start of the level. The boss bounces all over the screen and when it gets to one point it change sizes to try and catch the player out and reset them.

### Code

The code below shwos the movement of the size changing boss. It gets executed if the the sprite's x or y position does not equal the target point it is trying to reach, it will lerp to the next point. The 'ai' is a component of the class, that helps with any movement that isn't the player. There is a float that gets increased which is then used a the time percentage of the loop.

~~~
  if (current_state == MOVING)
  {
    if (static_cast<int>(spriteComponent()->getSprite()->xPos()) !=
          static_cast<int>(ai->getNextValue(X)) &&
        static_cast<int>(spriteComponent()->getSprite()->yPos()) !=
          static_cast<int>(ai->getNextValue(Y)))
    {
      spriteComponent()->getSprite()->xPos(ai->lerp(X));
      spriteComponent()->getSprite()->yPos(ai->lerp(Y));
      ai->setCurrent_time(ai->getCurrent_time() + 1.0f * dt_sec);
    }
  }
~~~

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-3){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-5){: .btn}
