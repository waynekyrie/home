---
layout: post
title: "Adaptable Human Motion Prediction"
date:   2020-09-01
description: "Human Motion Prediction"
location: "Pittsburgh, PA"

---

## Overview
Human-robot collaboration enables more flexible production lines to address the contemporary needs. In such environment, human workers are required to collaborate with robots in a confined workspace. Since frequent physical interactions exist, it is essential to ensure the safety while maximizing efficiency. Human motion prediction is an important step to address the challenge. This project focuses on predicting human arm motion for assembly tasks.

----

## Problem
The problem focuses on human arm motion prediction, where the framework takes in the N-step historical arm trajectory and outputs the M-step future arm trajectory.
<img src="images/RNNIK_MKF/arm_model.jpg" width="800">


----

## Methodology
In general, human wrist moves with clear intentions while the elbow moves only to support the wrist motion. Thus, we address the problem using an RNN for wrist motion prediction and IK to extend the wrist motion to full-arm motion. A proposed Modified Kalman filter is used for online adaptation to adjust the model to the current human or task, since it is impossible to obtain motion data for all human workers and tasks in real application.
<img src="images/RNNIK_MKF/framework.png" width="800">

----

## Results
<img src="images/RNNIK_MKF/t1t1.JPG" width="800">
<img src="images/RNNIK_MKF/t1t2.JPG" width="800">
<img src="images/RNNIK_MKF/adaptation_error.JPG" width="800">
<img src="images/RNNIK_MKF/t1tt2.JPG" width="800">

----

## Credit
This project is advised by [Prof. Changliu Liu](https://www.ri.cmu.edu/ri-faculty/changliu-liu/). The project is in part supported by Ford.
