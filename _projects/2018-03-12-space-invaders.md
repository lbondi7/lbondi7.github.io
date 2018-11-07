---
layout: post
title:  "SPACE INVADERS"
date:   2018-03-12
excerpt: "Space Invaders"
project: true
tag:
- Project
- C++
- Space Invaders
- ASGE
- ESD
- Visual Studio Project
- Year 1 Coursework
published: true
---
**Space Invaders** is a game I designed whilst in my first year at U.W.E. It was coded using c++ and in the ASGE. It plays very similar to the original, except with a different graphical layout and some modifications.<br/>

<a href="/assets/img/Games/SpaceInvaders/Space_Invaders_Home.jpg"><img src="/assets/img/Games/SpaceInvaders/Space_Invaders_Home.jpg"></a>

The image above shows the menu screen and the one below shows gameplay.<br/>

<a href="/assets/img/Games/SpaceInvaders/Space_Invaders_In_Game.jpg"><img src="/assets/img/Games/SpaceInvaders/Space_Invaders_In_Game.jpg"></a>

#### How to move the player.
```C++
	if (move_left)
	{
		player_ship_sprite->xPos(player_ship_sprite->xPos() - player_ship.getSpeed()* player_ship.getX() * dt_sec);
	}
	if (move_right)
	{
		player_ship_sprite->xPos(player_ship_sprite->xPos() + player_ship.getSpeed()* player_ship.getX() * dt_sec);
	}
```

#### How to move the aliens.
~~~ C++
		alien_ships_sprite->xPos(alien_ships_sprite->xPos() + alien_ships[i].getSpeed() * alien_ships[i].getX() * dt_sec);
		if (alien_ships[i].isVisible())
		{
			if (!alien_ships->spriteComponent()->getBoundingBox().isBetween(alien_ships_sprite->xPos() + alien_ships_sprite->width(), 0, game_width) ||
				!alien_ships->spriteComponent()->getBoundingBox().isBetween(alien_ships_sprite->xPos(), 0, game_width))
			{
				inverseVectors();
			}
		}
~~~

#### Initialise the player.
~~~ C++
	if (!player_ship.addSpriteComponent(renderer.get(), "Resources\\Textures\\spaceshooter\\PNG\\playerShip1_blue.png"))
	{
		return false;
	}
	player_ship_sprite = player_ship.spriteComponent()->getSprite();
	player_ship_sprite->width(80);
	player_ship_sprite->height(60);
	player_ship_sprite->xPos((game_width / 2) - 40);
	player_ship_sprite->yPos(game_height * 0.9);
	player_ship.setSpeed(300);
	player_ship.setX(1);
~~~
<br/>
<br/>
<br/>
**This game was made for educatonal purposes, for me show my improvement as a games developer and so this was not made for any commercial purposes.** 
