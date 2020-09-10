---
layout: post
title: "Line Following Tank"
description: "This was a project for the CMU Mobot 2018"
location: "Pittsburgh, PA"

---

This was a project for the [CMU Mobot competition](https://www.cs.cmu.edu/mobot/race.html) in 2018. This event is an annual competition held by the School of Computer Science. The goal is to build a mobile robot that follows a track in front of Wean Hall. There are small gates representing checkpoints placed along the track, and the robot is required to go through the gates. So the robot should strictly follow the line instead of go directly to the goal point. We got the third place in the end.

## Team
Same team as always!<br />
<img src="images/mobot/team.jpg" width="800"><br />
Alvin Shi (right), [Henry Zhang](https://henryzh47.github.io/) (left), and I and Baymax (middle).

## Robot
<img src="images/mobot/chassis.jpg" width="500"><br />
We purchased this tank chassis on Amazon. It looks cool, powerful, and stable. However, its performance was way worse than we expected. The chassis was too heavy for the motors that came in the package, causing the robot to perform randomly in real. By random, it means that given the same control parameters, it would occasionally work, but also would not work sometimes. Hence, it was extremely difficult to tune the control.

## Algorithm
We used monocular vision to track the line. A Raspberry Pi was used as the onboard processor and a Pi camera was placed in front of the robot. The vision algorithm was implemented using segamentation, where we extract the white line for each frame. The control part was implemented using PID. However, since the robot was too heavy, the robot's max speed was limited and it was very easy to understeer. Even though the vision worked stably, the robot could not ahieve a fast and responsive line following performance. The implementation can be found on our [GitHub Repo](https://github.com/alvinshi/Mobot_2018).

## Video
<figure class="video_container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/AZ35bDdGzBw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</figure>
Here is a short video for our testing. It was slow, but runs decently.

## Lesson Learned
Software/Hardware co-design is very important. Sometimes slightly improving the hardware quality could save enormous amount of time on tuning/improving the software. It is important to consider both hardware and software when doing a project that includes interactions with the real world. 
