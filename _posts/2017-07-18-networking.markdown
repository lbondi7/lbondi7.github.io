---
layout: post
title:  "Networking: A brief discussion and some thoughts"
date:   2017-07-18 16:54:46
author: James Huxtable
categories: 
- Blog
- Networking
- Development
- Crackers
img: post02.jpg
thumb: quake_thumb.jpg
published: true
---

<b>Networking</b> is quite rightly known for being one of the most difficult areas of gameplay to implement. In this post we'll look at some of the common techniques and technologies used to create multi-player experiences, both over WAN and LAN. <!--more-->

>The biggest difference is the addition of client side movement simulation.
>I am now allowing the client to guess at the results of the users movement 
until the authoritative response from the server comes through.  This is a 
biiiig architectural change.  The client now needs to know about solidity 
of objects, friction, gravity, etc.  I am sad to see the elegent 
client-as-terminal setup go away, but I am practical above idealistic.

[John Carmack][carmack] discussing the architectural changes to the networking model. It's clear that latency was a much bigger issue back then due to the proliferation of Dial-Up. Many of us now have broadband providing marked improvements in speed. 

[carmack]: http://fabiensanglard.net/quakeSource/johnc-log.aug.htm
