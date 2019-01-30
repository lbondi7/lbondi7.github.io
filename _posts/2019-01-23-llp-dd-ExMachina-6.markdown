---
layout: post
title:  "Ex-Machina Game Dev Diary: Size Boss 2.0"
date:   2019-01-23
author: Lewis Bond
categories: [Developer Diary, Low Level Programming Dev Diary, Ex-Machina Dev Diary]
img: /Uni/LLP/Ex-MachinaDevDiary/Ex-Machina.jpg
thumb: /Uni/LLP/Ex-Machina/Ex-Machina.png
published: true
---
<!--more-->

# Ex-Machina

The size boss had been done before but it wasn't very good good in terms of optimisation and readability so I cleaned it up and changed a lot of it.  

### Code

The previous code can be seen in a previous blog post but it showed a sample of the code which had a really unreadable if statement that waasn't necessary at all. Since it moves by a lerp a timer can just be used to as a checker for when to update its x and y position. Once the timer reaches the timeout value then it changes the state from MOVING to SIZE so then the size uses the lerp as well. The timer is also then reset back to 0 so it can start counting up again. Checking if the sprite hasn't reached it's destination isn't necessary anymore, because when the timer reaches the timeout function then the sprite will be at or very close to the intended desination due to the lerp. 

~~~
  if (current_state == MOVING)
  {
    if (timer->count < timer->timeout)
    {
      sprite.xPos(timer->lerp(last_point.x, next_point.x, percentage));
      sprite.yPos(timer->lerp(last_point.y, next_point.y, percentage));
    }
    else
    {
    // rest of the code
    }
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

[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-5){: .btn}
