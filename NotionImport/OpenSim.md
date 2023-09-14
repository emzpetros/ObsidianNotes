[https://simtk.org/projects/real_time](https://simtk.org/projects/real_time)

[https://www.mdpi.com/1424-8220/21/5/1804/htm](https://www.mdpi.com/1424-8220/21/5/1804/htm)

  

https://github.com/mitkof6/OpenSim_API_tutorial

  

They implemented an OpenSim backend to do real time kinematics calculations (from Vicon marker data or IMU) and then visualized the model outputs in Unity!  They were able to build an entire application on top of it all in Unity which of course could then be exported to any platform

The source code doesn't include the Unity build unfortunately but at least an integration is possible

There's a lot in the paper regarding the accuracy of the modeling approach (filtering, optimizations etc) I would need more time to understand.  But as far as implementing biomechanically accurate movement in Unity in the future, this seems like an ideal approach that can utilize something like OpenSim that's already a widely accepted tool

### Documentation

User API: [https://opensim-org.github.io/opensim-moco-site/docs/1.0.0/html_user/index.html](https://opensim-org.github.io/opensim-moco-site/docs/1.0.0/html_user/index.html)

OpenSim Download page: [https://simtk.org/projects/opensim/](https://simtk.org/projects/opensim/)

  

## Another Real Time System

Paper: [https://ieeexplore.ieee.org/document/9512410/algorithms#algorithms](https://ieeexplore.ieee.org/document/9512410/algorithms#algorithms)

Real time tutorial: [https://simtk-confluence.stanford.edu:8443/display/OpenSim/Wearable+and+Real-time+Kinematics+Estimates+with+OpenSense](https://simtk-confluence.stanford.edu:8443/display/OpenSim/Wearable+and+Real-time+Kinematics+Estimates+with+OpenSense)

  

# OpenSim File

IMU data comes in as table of XYZ for each frame and sensor

![[Untitled 640.png]]