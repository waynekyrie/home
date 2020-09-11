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
### Nichrome wire method
Thermal cameras capture the temperature features. Thus, we need to manually create such features. We use nickle-chromium heat resisting wire as thermal source and a 24x24 inch acrylic board as baseboard. Then hook it up with a 30V/5A power source. The wire will heat up under the current and become visible to the thermal camera.





## Report
<embed width="100%" height="500%" name="plugin" id="plugin" src="multiple-methods-geometric.pdf" type="application/pdf" internalinstanceid="3">
<object data="multiple-methods-geometric.pdf" type="application/pdf" width="700px" height="700px">
    <embed src="multiple-methods-geometric.pdf">
        <p>This browser does not support PDFs. Please download the PDF to view it: <a href="multiple-methods-geometric.pdf">Download PDF</a>.</p>
    </embed>
</object>
This is the research project report of the work we did. 

## Credit
This project was collaborated with [Henry Zhang](https://henryzh47.github.io/).
