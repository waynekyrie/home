---
layout: post
title: "Basketball Retriever"
description: "A workout partner that helps the player to retrieve the basketball"
location: "Pittsburgh, PA"

---

This was the capstone project I did for [18500](https://courses.ece.cmu.edu/18500). The basic idea was to build a collaborative mobile robot that helps the basketball player during practice. When a player is practicing shooting, the ball would bounce to random places if missed the shot. It is sometimes frustrating and time-consuming to get the ball back. For professional players, they would usually have a partner/trainer to help get the ball and pass it back to the player. Another common solution is to place a huge net machine under the rim and collects the ball and launches back to the player. There are several disadvantages of this method. First, the machine is big so it is inconvenient to move from one gym to another. Second, it only aims in one direction, which means it could only pass the ball to one spot. If the player wants to practice shooting from another spot, the player should manually change the direction of the machine. Third, the net would force the player to change the shooting arc. Some player have lower shooting arc would be blocked by the net, so the usage of this kind of machine would also force them to change their shooting form, which is uneccessary. 

Therefore, in this project we intend to build a mobile robot that can retrieve the ball each time when it bounces away.

## Hardware Design
<img src="images/basketball/design.jpg" width="800">
The picture shows the design of the robot. It has a hollow body frame so it is able to keep the ball inside the frame. There is a gate at the front of the robot. Each time the robot has the control of the ball, it would lower the gate to secure the ball inside. The robot is front-wheel-drive, powered by two motors. The top of the robot has a board, where we could put all the sensors, processor on it.

## Software
<img src="images/basketball/Flow.png" width="800">
The system shows the software pipeline. Briefly, we used a Convolutional Neural Network to detect the basketball. We used the [Apriltag](https://april.eecs.umich.edu/software/apriltag) to represent the player. We used stereo vision to implement decision-making. The robot uses stereo vision to determine where the player is and when to offer the ball to the player. We also used PID motion control to smooth the robot motion.

## Video
<figure class="video_container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/n8TYA04VexE" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</figure>
This video shows a testing trial.

## Poster
This is our project poster for the capstone demo.
<object data="poster.pdf" type="application/pdf" width="700px" height="700px">
    <embed src="poster.pdf">
        <p>This browser does not support PDFs. Please download the PDF to view it: <a href="poster.pdf">Download PDF</a>.</p>
    </embed>
</object>

## Website
More details can be found on our [project website](http://course.ece.cmu.edu/~ece500/projects/s19-teamb6/?fbclid=IwAR1c3ziRjr1GjOS_lTIxvD0GUs8wR0JYVroZQG8C0PXkEcl1nTI8tKc-GOY).

## Credit
<img src="images/basketball/team.jpg" width="700">
Shout out to my teammates Alvin Shi (2nd right) and Roy Li (right)! And big thanks to [Prof. Tamal Mukherjee](https://www.ece.cmu.edu/directory/bios/mukherjee-tamal.html), who gave huge support to our work.
