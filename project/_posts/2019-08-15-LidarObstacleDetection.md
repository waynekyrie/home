---
layout: post
title: "Lidar Obstacle Detection"
description: "Lidar Obstacle Detection"
location: "Pittsburgh, PA"

---

## Overview
This was an intern project during my internship at Zenuity in the summer of 2019. We were trying to build a mobile robot that can manuever in the office automatically. There were many modules to implement, including path planning, motion control, safety, etc. I was working on the Lidar perception part. The goal was to use the Lidar to detect the obstacles and generate the free area that was traversable for the robot.

## Approach
The basic idea was to divide the world into a grid map. Then detect the obstacle for each grid. The traversability was obtained by searching for the connectivity starting from the robot current position.

## Video
This video shows the performance on the Kitti dataset.
<figure class="video_container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/gMa-xhgH_sM" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</figure>

This video shows the performance in the office.
<figure class="video_container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/GwfVTA1slqs" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</figure>

