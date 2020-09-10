---
layout: post
title: "LEGO Line Following Robot"
description: "This is a course project for 16311-Intro to Robotics"
location: "Pittsburgh, PA"

---

## Overview
This was a course project for [16311](https://www.cs.cmu.edu/afs/cs.cmu.edu/academic/class/16311/www/s17/index.html). There were many projects throughout the semester, 
and each one lasted for around one week. The goal for this one was to build a robot that can follow the line track.

## Approach
The robot was built using lego pieces. It has a light sensor placed in front of the robot. The sensor measurement could distinguish the black line and the white background.
We used PID control to track the desired measurement value.

## Video
<figure class="video_container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/ZW3z8pkuRFY" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</figure>
This video shows our robot during the course demo. Our robot could achieve a smooth tracking during steady state, even though it vibrated at the beginning. 
The overshoot could be eliminated and achieve a quicker settling time by further tuning the parameters.

## Credit
The team includes [Henry Zhang](https://henryzh47.github.io/) and Xueting Li.
