---
layout: post
title:  "Ex-Machina Game Dev Diary: Post Mortem"
date:   2019-02-23
author: Lewis Bond
categories: [Low Level Programming Dev Diary, Ex-Machina Dev Diary, Post Mortem]
img: /Uni/LLP/Ex-MachinaDevDiary/Ex-Machina.jpg
thumb: /Uni/LLP/Ex-Machina/Ex-Machina.png
published: true
---

<!--more-->
# Deity: Become One

<center>
<figure>
    <a href="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/DeityBO.gif"><img src="/assets/img/blog/Uni/LLP/Ex-MachinaDevDiary/DeityBO.gif"></a>
    <figcaption>This just shows a snippet of the game.</figcaption>
</figure>
</center>

## Pros
<ul>
    <li>Refactoring the code down so it made it easier to understand and read, when someone else was looking at it.</li>
    <li>Reading/writing to dat files worked well when loading and saving the levels. It was broken down into 4 parts. One dat file stored the data on the boss, another the obejcts such as blocks and lesser enemies, another the player data and teh last one stored the settings for the levels.</li>
    <li>The mixture of inheritence and composition based progarmming also worked well with our lecturer commenting that we had done a "superb job".</li>
    <li>The astectics were also very good as it gave our game a very unique style and people could instantly recognise our game.</li>
</ul>

## Cons
<ul>
    <li>The level builder wasn't as good as it could of been code wise and also when using it.</li>
    <li>The code for the level builder was a bit messy and could of been cleared up if I had made a button or an UI class to help with all the button presses and unique code.</li>
    <li>The design was a bit confusing so as some people were saying they didn't know what to press once tehy had made their level and that they didnt seen the side bar as it was hidden away too much.</li>
    <li>The story was also a bit lacking and there was no real motivation to play in terms of character that the user could relate to or become interested in.</li>
</ul>

## Potential Improvements
<ul>
    <li>Make the enemy designs more unique so they are clearer and easier to distinguish.</li>
    <li>Added in a  real story to make the user want to play the game more.</li>
    <li>Compress the audio so it doesn't take ages to load up rigth at the start.</li>
</ul>

## What I Learned
<ul>
    <li>I learned about component based programming and how useful it is. The fact that you can just attach a component to an object and say, ok now behave like this and then attach another one and the object can act entirely different.</li>
    <li>It taught me component based programming, as well as consolidating my understanding of how classes and objects should interact in a game.</li>
    <li>Also I learned how important constant communication in a group project is, as sometimes we didn't and then we would end up working on the same thing and end up clashing.</li>
</ul>


[PREVIOUS BLOG POST](https://lbondi7.github.io/developer%20diary/low%20level%20programming%20dev%20diary/ex-machina%20dev%20diary/llp-dd-ExMachina-10){: .btn}

[PROJECT](https://lbondi7.github.io/projects/LLP-ex-machina/){: .btn}
