---
layout: post  
title:  "Monty Hall problem"
description: "It's easier to believe the solution by simulating it."
date:   2014-06-15 19:04:00
tags: [math, programming]
categories: math
math: false
comments: true
image:
    feature: star_trail_f.jpg
---

This is my first entry in this blog! It is rightful, as I decided to create this website after much thinking about the best way to share my Monty Hall simulation. But before showing you that, why do I need a Monty Hall simulator?

## The problem

Imagine you are a player in the famous game show <span style="font-style:italic">Let's make a deal</span>. You are faced with the difficult choice of picking a door out of three possibilities. I say it's difficult because behind one door is an awesome car and behind each of the other two doors is a goat. You correctly guessed that to win the car you must choose the right door, but there is something else I haven't told you: after you pick a door, Monty Hall, the show's host, choose one of the remaining doors having a goat behind it and open it, giving you the opportunity to stay with your previously choosen door or to switch to the remaining one. So here is the problem:

> Which choice maximizes your odds of winning?

The first time I heard the problem was in a probability class last month and I thought that I had 50% chance of winning either way. I was wrong. But I couldn't follow as the teacher gave a wordy argument explaning why the probability of winning is 66.6% if you switch doors. A week later I started to understand the answer, thanks to this video in Numberphile's channel:

<div class="aspect-ratio" align="center">
<iframe width="560" height="315"  src="//www.youtube.com/embed/4Lb-6rxZxx0" frameborder="0" allowfullscreen></iframe>
</div>

They give a good explanation in the video, but I found myself convinced only after I watched the extended version with more math. You don't have to watch the video or do any fancy math if you agree with the following reasoning, adapted from [vos Savant]:

1. Choose a door, let's say number one.
2. You have a 1/3 chance that the car is behind the door. In this case, if you switch you'll loose the car.
3. You have a 2/3 chance that a goat is behind the door. In this case, if you switch you win (as the other goat was revealed by the host). 
4. Conclusion: if you switch, you win 2/3 of times.

It's wonderful, isn't it?

## The simulation

I've also seen many people who don't believe the answer anyway (my parents for a start), so I decided to create a simulation of the problem. To be fair, even I, after seeing all those explanations, wanted to experiment with it and "confirm" the answer was indeed correct (what a shameful aspiring mathematician!). 

You can try it:
<a href="{{ site.url }}/monty-hall-simulation" target="_blank"><span style="margin-left:12px;" class="icon-html5"> Monty Hall Simulation</span></a>

[vos Savant]:http://marilynvossavant.com/game-show-problem/
