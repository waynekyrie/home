---
layout: post
title: "3D Reconstruction with Thermal Texture"
description: "3D Reconstruction with Thermal Texture"
location: "Pittsburgh, PA"

---

This was a research project that I did during the internship in the [AirLab](https://www.ri.cmu.edu/robotics-groups/air-lab/) led by [Prof. Sebastian Scherer](https://www.ri.cmu.edu/ri-faculty/sebastian-scherer/). The goal for this project was to enable inspection from 3D reconstruction. The conventional inpection process needs human workers to manually inspect the building structures. However, it is sometimes difficult or dangerous for humans to physically get close to the structure. Therefore, this project intended to develop a sensor pod that a robot, such as an unmanned aerial vehicle (UAV), could carry it to inspect the building structure. The inspection could be done by manually inspect the high accuracy 3D reconstruction from the measurement data. 

As the initial phase, instead of build directly on a drone, we built a handheld prototype that could be tested on ground. To achieve high-accuracy 3D reconstruction, the sensor pod has a pair of 4K XIMEA stereo cameras and a Velodyne Lidar. Since many inspections need thermal information, we also had a FLIR thermal camera onboard to provide thermal texture. The sensor pod had the Intel NUC as the core processor.<br />
<img src="images/reconstruction/front_description.jpg" width="900"><br />
<img src="images/reconstruction/hand_held.jpg" width="500">
<img src="images/reconstruction/tripod.jpeg" width="460"><br />
Henry with the hand-held sensor pod.


## Approach
The 3D reconstruction was accomplished by stereo vision. The Lidar measurement was used to filter out the noise in stereo mapping and improve the accuracy. The thermal texture was obtained by calibrating the thermal camera and visual camera. After having the transformation, we could project the thermal image onto the visual image and add an extra thermal channel for the RGB pixels.

## Results
We attached a paper box on a wall and reconstructed the surface while moving. The following images show the reconstruction of two consecutive shots. The reconstruction from the high-resolution visual camera and Lidar can give high-quality and detailed texture 3D reconstruction. <br />
<img src="images/reconstruction/result1.png" width="500">
<img src="images/reconstruction/result2.png" width="240"><br />
We put several ice cubes on the wall to test the thermal texture. <br />
<img src="images/reconstruction/result3.png" width="900">

## Credit
This project was collaborated with [Henry Zhang](https://henryzh47.github.io/) and [Yaoyu Hu](http://www.huyaoyu.com/).
