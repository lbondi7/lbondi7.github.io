---
layout: post
title:  "Ex-Machina Game Dev Diary: Dash Boss"
date:   2019-01-19
author: Lewis Bond
categories: [Developer Diary, Low Level Programming Dev Diary, Ex-Machina Dev Diary]
img: /Uni/LLP/Ex-MachinaDevDiary/Ex-Machina.jpg
thumb: /Uni/LLP/Ex-Machina/Ex-Machina.png
published: true
---
<!--more-->

## Dash Boss

Since the size changing bos was done (albeit temporarily done), the dash boss was next as we need to pick up the pace of the project. 

We had an idea about how the dash boss level would go. The player had to traverse different parts whilst teh dash would be randomly dashing to differnet parts of teh map and you had to avoid them. This is very similar to the size changing boss so it might be chagned to make it more unique and differnet to other bosses.

### Code

The code below shows a sample of the dash boss worked. A direction was randomly chosen and whichever one came the boss would dash in that direction. When a direction was chosen, if it was a north or south then the y position of the sprite would be updated and if it was east or west then the x position would be updated. In the code below the code below it shows y position = y postion - speed * dt, so the if y position was 50 and speed was 25 then it would y postion = 50 - 25 * dt. Dt is the time between frames, this is required so it will go at the same speed even if the frame rate changes. So the y psoition will be less then 50, which was it's previous position, so it will be higher up on the screen and be going north.

~~~
  case NORTH:
  {
    spriteComponent()->getSprite()->yPos(spriteComponent()->getSprite()->yPos()-speed*dt);
    break;
  }
~~~


### Randomiser

Since it randomised the direction, I had to include one of the libraries that did this, there is a small issue though with randomisation. The best way to is using the <random> library that uses random distribution to get a random number. Two numbers are passed in and these are the range that I want that to be in. This isn't working as the it only produces the lower value that is passed in. So the srand fucntion is being used temporarily, the issue with this is that it is less random, then the random distribution, and patterns can be seen if it used a lot so this really not what is wanted.

Once the number has been chosen it is then cast to a 'Direction', this is an enumeration which contains, NORTH, EAST, SOUTH and WEST.

~~~
      std::random_device rd;
//      std::uniform_int_distribution<int> dist(1, 4);
//      dir = static_cast<Direction>(dist(rd));
      srand(static_cast<unsigned int>(time(NULL)));
      dir = static_cast<Direction>((rand()%3)+1);
~~~


[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-4){: .btn} [NEXT BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-6){: .btn}
