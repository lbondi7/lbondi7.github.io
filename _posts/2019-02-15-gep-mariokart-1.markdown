---
layout: post
title:  "Mario Kart Dev Diary: Cameras"
date:   2019-02-15
author: Lewis Bond
categories: [Game Engine Programming Dev Diary, Mario Kart Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Cameras

For the Mario kart game my first task is to understand how the cameras work in direct x. The way the cameras were set up was of a child class of game object, and then they have a child class of that called TPSCamera. This camera is used for third person and was set up by out lecturer for us. 

The difference between the two is that the first one, you pass in the camera's width, height, near view and far view and it would instanciate a camera and render whatever it saw from its position in the world. You could update the posistion and how far the camera rendered as well. 
With the TPSCamera, all the previous data was passed in when instanciating one, but also passed in a target and delta position. The target was what the camera to look at and the delta position was the position of the camera in relation to the target.

What I did to save on the number of classes is merge the TPSCamera class in to the camera class so now a camera can be both with having to use different class. In order to stop a camera being third person, a nullptr is passed in instead and it checks if the target pointer in the class is null and if it isn't then it locks onto the target else it goes back to being a normal camera.

~~~
m_cam1 = new Camera(static_cast<float>(1200), static_cast<float>(800), 1.0f, 1000.0f, nullptr, Vector3(0.0f, 3.0f, 10.0f));
~~~

[NEXT BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-2){: .btn}
