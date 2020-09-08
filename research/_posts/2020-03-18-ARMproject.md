---
layout: post
title: "Automatic Onsite Polishing"
date:   2020-03-18
description: "ARM project"
location: "Mill 19, Pittsburgh, PA"

---
# Overview
In manufacturing, many large workpieces are made by welding subcomponents together. It is required to remove the weld bead remained on the surface in order to deploy the workpiece in real applications. Conventionally, the weld beads are removed manually by human workers. However, the work is time-consuming, expensive, and more importantly, dangerous for human workers. For instance, a metal tube is manufactured by welding the upper half and the bottom half. The weld bead would remain both inside and outside the tube surface. It is relatively easy for a human to polish the bead on outter surface, but it is extremely difficult and dangerous for a human to polish inside the tube. Therefore, this project provides a robotic solution to the polishing task.

# Hardware Setup
The problem that this project intends to solve is polishing the weld bead inside a workpiece. We have the metal workpiece placed in front of our robot using a positioner. We designed a fixture for the robot to hold the polishing tool. The fixture allows the robot to reach into the workpiece and polish the weld bead inside. A depth camera is placed next to the setup to visually locate the setup.

{% include image.html url="images/ARM/environment_setup_caption.jpg" caption="Hardware Setup" width="1000px" align="left" %}

# System Pipeline
We designed a state machine to control the workflow of the system pipeline. The pipeline includes six major states to complete the polishing task. The state machine controls the transition from states to states.<br />
The first state for the pipeline is Visual Alignment. The system uses the depth camera to estimate the transformation between the robot and the workpiece.<br />
After the transformation is determined, the system enters the Measurement Planning state. The motion planner plans a reference trajectory for the robot to use the laser scanner to measure the inner weld bead. <br />
After the trajectory is obtained, the next state entered is Surface Measurement. The controller controls the robot to reach into the tube and precisely measure the weld bead. The weld bead is extracted from the scanned pointcloud. The laser measurement is also used to refine the estimated transformation measured by Visual Alignment. <br />
With the measured weld bead, the motion planner plans a polishing trajectory in the Polishing Decision state. <br />
In the Polishing state, the controller controls the robot to safely performs the polishing. <br />
At last, the robot remeasures the inner surface to evaluate the polishing quality. <br />

{% include image.html url="images/ARM/state_machine.jpg" caption="State Machine Transition Diagram" width="800px" align="left" %}
