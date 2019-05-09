---
layout: post
title:  "Mario Kart Dev Diary: Data Driven"
date:   2019-04-24
author: Lewis Bond
categories: [Game Engine Programming Dev Diary, Mario Kart Dev Diary]
img: /Uni/GEP/MarioKart/mariokart.png
thumb: /Uni/GEP/MarioKart/marioKart.png
published: true
---
<!--more-->

## Data Driven
The cameras were too hard coded before, as all the variables were set in the camera header and were magic numbers. This had to be changed in order the cameras to be more usable. The data that was shared ebtween all the cameras were taken out of the camera class and stored in a json file. This enabled the user to change the configurations in the json without having to go into the code base.It was helped with Matt's tool which had a nice GUI, in which teh user could adjust values without having to see the json file (example shown below). 

~~~
  "FOLLOW": {
    "fov": 60,
    "rotation_lerp": 0.1,
    "position_lerp": 0.50,
    "look_at_position": [ 0.0, 0.0, 1.0 ],
    "target_position": [ 0.0, 0.0, 0.0 ],
    "camera_offset": [ 0.0, 2.0, 5.0 ],
    "look_at_offset": [ 0.0, 2.0, 0.0 ]
  },
~~~

Any data that shared across multiple camera instances such as how fast teh orbit cam span or what psoitions the cinematic camera went to were put into the CameraData struct. This was called by the service locator and it stored all the data shared across multiple cameras. This meant now, every instantiation of camera didn't hold a vector of its possible cinematic positions which never changed so multiple vectors were created unnecessarily.


[PREVIOUS BLOG POST](https://lbondi7.github.io/game%20engine%20programming%20dev%20diary/mario%20kart%20dev%20diary/gep-mariokart-10){: .btn}
