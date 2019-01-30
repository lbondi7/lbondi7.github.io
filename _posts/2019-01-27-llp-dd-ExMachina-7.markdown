---
layout: post
title:  "Ex-Machina Game Dev Diary: Dash Boss 2.0"
date:   2019-01-27
author: Lewis Bond
categories: [Developer Diary, Low Level Programming Dev Diary, Ex-Machina Dev Diary]
img: /Uni/LLP/Ex-MachinaDevDiary/Ex-Machina.jpg
thumb: /Uni/LLP/Ex-Machina/Ex-Machina.png
published: true
---
<!--more-->

# Dash Boss

As explained in a previous dev diary, teh code for the dash enemy was a temporary fix to test it out for the game. It didn't really work well and I discuessed with the team and we decided to change how the level would work. We changed to so the layput of the level would remain the same but teh way the boss worked would change. 

## Changes

Instead of dashing in random directions, it would target the player and then after a few seconds it would dash towards the player and if it collided with the player then they would be reset to the start of the level. They will dash for a few seconds and then it will restart at a random point and start targeting the player again. This is inspired by the Revek enemy from Hollow Knight. 

To see an example of the Revek follow the link below.

[HOLLOW KNIGHT EXAMPLE](https://youtu.be/dlFiPgPu2M8?t=124){target="blank" rel = "noopener"}{: .btn}

### Code

The code below shows a part of how the dash works. Whist the count is less then the timeout, it gets the difference between the player position and its position and works out the directional vector using the normalise function. It then multiplies that vector by 4000, this is the magitude of the vector. Once the count reaches the timeout, it resets the count, switches the state to DASH, using an else if statement, and then it updates the x and y position using the vector.

~~~
  if (timer->count < timer->timeout)
  {
    direction.setX(player_pos.x - (sprite.xPos()));
    direction.setY(player_pos.y - (sprite.yPos()));
    direction.normalise();
    direction = direction * 4000;
  }
  else
  {
    timer->count = 0;
    state = DASH;
  }
~~~

<center>
	<figure>
	    <a href="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/MenuScene.PNG"><img src="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/MenuScene.PNG" height="400"></a>
	    <figcaption>The menu is used to display the controls for the tool.</figcaption>
	</figure>
  </center>
  <br/>
  <center>
	<figure>
			    <a href="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/LevelBuilderScene.PNG"><img src="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/LevelBuilderScene.PNG" height="400"></a>
	    <figcaption>The level builder is used to help us with designing levels.</figcaption>
	</figure>
</center>

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-7){: .btn}
