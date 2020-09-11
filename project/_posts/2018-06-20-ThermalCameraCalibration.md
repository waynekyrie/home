---
layout: post
title: "Thermal Camera Calibration"
description: "Thermal Camera Calibration"
location: "Pittsburgh, PA"

---

This was a research project that I did during the internship in the [AirLab](https://www.ri.cmu.edu/robotics-groups/air-lab/) led by [Prof. Sebastian Scherer](https://www.ri.cmu.edu/ri-faculty/sebastian-scherer/).

## Overview
Due to the manufacturing process, cameras are not made perfectly fitting the theoretical model. The mismatched model leads to deviation in the transformation map between 3D object points to 2D image points. It is required to correct this mismatched model in order to use the camera projection model. Therefore, geometric calibration is an important step that directly impacts the following algorithms. Calibrating a regular visual camera is a common task now and there exist many good tools to accomplish that. However, calibrating a thermal camera is much more difficult. Since the features are blurred on thermal images, existing methods of calibrating visual cameras can not be directly applied to thermal cameras. Therefore, we tried multiple methods to calibrate thermal cameras and compared the results. 

## Methods
Thermal cameras capture the temperature features. Thus, we need to manually create such features. Basically, we tried three methods in creating the calibration target board.
### Nichrome wire method
<img src="images/thermal_camera_calibration/hotwire_front.jpeg" width="500">
<img src="images/thermal_camera_calibration/hot_wire_view.jpg" width="500"><br />
We used nickle-chromium heat resisting wire as thermal source and a 24x24 inch acrylic board as the baseboard. We hook the wire to a 30V/5A power source. The current would heat up the wire and generate the desired heat pattern.

### Foam metal-plate method
<img src="images/thermal_camera_calibration/foam_setup.jpeg" width="500">
<img src="images/thermal_camera_calibration/foam_thermal.jpg" width="500"><br />
The basic idea was to insert metal plates into a foam board. We put the metal plates in a fridge to cool them. Since foam is adiobatic, the cold metal would have clear temperature pattern. 

Thanks to Joseph Bartels who designed the calibration board and Chuck Whittaker who fabricated the device.

### Sunlight heating checkerboard method
<img src="images/thermal_camera_calibration/direct_setup.jpeg" width="500">
<img src="images/thermal_camera_calibration/direct_thermal.jpeg" width="500"><br />
A regular checkerboard can generate good thermal patterns, since the black and white colors have different capability on absorbing heat from lighting. We tested using a heat lamp and sunlight to heat a checkerboard, and it turned out that sunlight was much better. In general, a even distribution of heat and stronger heat from light are preferred.

## Report
<object data="multiple-methods-geometric.pdf" type="application/pdf" width="700px" height="700px">
    <embed src="multiple-methods-geometric.pdf">
        <p>This browser does not support PDFs. Please download the PDF to view it: <a href="multiple-methods-geometric.pdf">Download PDF</a>.</p>
    </embed>
</object>
This is the research project report of the work we did. The details are explained in the report.

## Credit
This project was collaborated with [Henry Zhang](https://henryzh47.github.io/).
