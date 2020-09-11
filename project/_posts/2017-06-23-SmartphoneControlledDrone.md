---
layout: post
title: "Smartphone Controlled Drone"
description: "Smartphone controlled drone"
location: "Pittsburgh, PA"

---

This was a project that I did during the internship in the lab led by [Prof. Xiaorui Zhu](https://scholar.google.com/citations?user=S11Nv9EAAAAJ&hl=en).

## Overview
The goal for this project was to achieve stable UAV control based on smartphone motion sensing. Instead of using a specialized remote controller, the user can use a phone app to easily control the drone. To make the control method intuitive, we aim to use up/down buttons to control the altitude and the phone's attitude to directly control the drone's attitude.

## Functions
To achieve the goal, there were several things we implemented. First, the programmed app was able to capture the motion of the phone, which means we could know how much the phone was rotated or tilted. Second, the app was able to establish stable wireless connection between the drone and the phone. We used wireless hotspot to achieve that. Third, the app was able to transform the raw motion sensing data to reasonable motion command.  


## Video
<figure class="video_container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/5MQbwDau5tc" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</figure>
This video shows a test flight. Due to the light condition, the screen on the phone was unfortunately not visible. What happened in the video was that the drone was controlled by the RC initially. If the user want to gain control, an unlock button should be pressed on the phone. That was the reason why in the video the drone did not rotate for the first time. When the user wanted to increase/decrease altitude, the up/down button should be pressed followed by a confirm button. The other control commands in the RPY direction were done in simply changing the phone's RPY. 

## Credit
This project was collaborated with [Chris Yin](https://github.com/ChrisYin).
