---
layout: post
title:  "Network Game Dev Diary: Player Input and Card Effects"
date:   2019-04-08
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Network Game Dev Diary]
img: /Uni/LLP/RainforestRampageDevDiary/RainforestRampageCover.png
thumb: Uni/LLP/RainforestRampage/RainforestRampageThumb.png
published: true
---
<!--more-->

## Setting Player Input

We needed to thet cards being draw form the deck by the player and then the effects of those cards being used when the player clicked on  the card. This needed to be for every player on their turn. AT first when player clicked on eth tile, their icon moved to hat tile and the <i>'current_player_turn'</i> would increment and that would get sent to the next player. If that value matched your client id then it would trigger a value to be true and the player could then move. This changed for the use of cards so I added in player input enum with 4 values. 
~~~
enum class PlayerInput : int
{
  NONE = 0, // not doing anything
  MOVE_TILE = 1, // move tiles
  USE_CARD = 2, // use a card
  TILE_SEL = 3, // select a tile
};
~~~
Instead of passing the curent player turn, a varaible of this enum was sent to the client id that matched the current player turn. When the user receives this data a simialr variable is sent from NONE to whatever is streammed out of the packet, The user can then perfrom certain actions depending on value the variable is set to.

## Card Effects

When the player input equals <i>'USE_CARD'</i> the player can click on the card drawn for the deck for it's effect to take place. If the card drawn is a deforestation, mass deforestation or recovery then it will allow the player to click the card, and then click on a tile to effect. If the drawn card is a poacher then it automatically does the effect of the card. If it is a deforest card then the tiles change from green to orange to show death and deforesation. The image below show the player clicking and the board changing depending on whta card it is.

<center>
	<figure>
<a href="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/CardsBeingUsed.gif"><img src="/assets/img/blog//Uni/LLP/RainforestRampageDevDiary/CardsBeingUsed.gif" width = "600" height = "338"></a>
		<figcaption>The card's effect when the player uses them.</figcaption>
	</figure>
</center>

<br/>

[PREVIOUS BLOG POST](https://lbondi7.github.io/low%20level%20programming%20dev%20diary/network%20game%20dev%20diary/llp-dd-network-rr-9){: .btn}
