---
layout: post
title: "Real-Time Object Tracking"
description: "This was a project for 16720"
location: "Pittsburgh, PA"

---

## Overview
This was a course project for 16720: Computer Vision. The goal for this project was to build a pipeline that could robustly track a desired object. 

## Algorithm
The basic idea was simple. The pipeline uses a convolutional neural network to detect the object we want. However, it is inefficient to detect the object for each frame. 
Therefore, it combines the Lucas Kanade tracking algorithm with the CNN. Once the object is detected, the pipeline uses the tracking algorithm to track the object in scene. 
It is faster and more computationaly efficient in this way. When the object is lost or occluded by obstacles, the tracking would fail and the CNN is then used to re-detect the object.


## Video
<figure class="video_container">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/vTFdL37lyjo" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</figure>
This video shows the comparison of the project and pure tracking. The pipeline can achieve real-time performance and recover from object lost.

