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
We designed a state machine to control the workflow of the system pipeline. 
{% include image.html url="images/ARM/state_machine.jpg" caption="State Machine Transition Diagram" width="1000px" align="left" %}
