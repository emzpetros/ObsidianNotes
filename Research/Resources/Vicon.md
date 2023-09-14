  

# Toolbox

  

# Notes

RBak covered up

Reflection from phone and Daekyoo

# Data Processing

Reconstruct

A medial, B lateral for wrist

0.004s capture; 250 Hz; 250fps

Unlabeled: trajectories, components

Check for unlabled first

Rigid body + pattern matching best

  

## Visual 3D

[https://c-motion.com/v3dwiki/index.php/Tutorial:_Command_Pipeline](https://c-motion.com/v3dwiki/index.php/Tutorial:_Command_Pipeline)

Center of P, velocity

  

Be able to defend biomechanical analysis

Virtual Foot: covers ankle joint, can’t represent in 3 coords

Set up model with static

apply to dynamic

Virtual Foot for joint calculations?

Whole Body Angular momentum: foot + whole body interaction

- Can calculate via marker or force plate data

Join angle moment power

Power of body = hip + ankle + knee  
Step Length:

- Marker data heel to heel

Pipelines: SMT

Axis same as in Vicon may need to change based on walking direction

Reporting biomechanical data: start higher level, joint stuff later

- Start with gait speed, step length; COM; global to local

  

  

Marker Based Analysis:[https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2384115/](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2384115/)

  

![[PXL_20220716_194836687.jpg]]

# Marker Placement

[https://docs.vicon.com/display/Nexus213/Full+body+modeling+with+Plug-in+Gait](https://docs.vicon.com/display/Nexus213/Full+body+modeling+with+Plug-in+Gait)

[https://www.youtube.com/watch?v=fl7CWDmIaHw](https://www.youtube.com/watch?v=fl7CWDmIaHw)

- Vicon Training: left wrist A on thumb side
- Right arm: center markers proximal
- Left Arm: center markers distal

![[Untitled 607.png]]

  

![[Untitled 608.png]]

  

![[Untitled 609.png]]

  

Axes? for marker template (cmt) file in DFlow

![[Untitled 610.png]]

# Other

- [https://knowledge.motekmedical.com/wp-content/uploads/2019/05/D-Flow-Gait-tutorials-1-4.pdf](https://knowledge.motekmedical.com/wp-content/uploads/2019/05/D-Flow-Gait-tutorials-1-4.pdf)

  

  

## Open Sim

Marker Data as TRC

Motion / force data as .mot

Need marker set information as xml: [https://simtk.org/frs/?group_id=433](https://simtk.org/frs/?group_id=433)

  

Use [tool](https://simtk.org/frs/download_confirm.php/file/3060/Lee-Son%20Toolbox%201.5.1.exe?group_id=670) to convert (set -Y axis) csv to trc and .mot

  

Needed files

- TRC
- MOT
- Model osim
- Marker set xml
- IK tools xml

[https://simtk-confluence.stanford.edu:8443/display/OpenSim/Preparing+Marker+Coordinate+Data#PreparingMarkerCoordinateData-PreparingFileFormat](https://simtk-confluence.stanford.edu:8443/display/OpenSim/Preparing+Marker+Coordinate+Data#PreparingMarkerCoordinateData-PreparingFileFormat)

[https://simtk-confluence.stanford.edu:8443/display/OpenSim/Coordinate+Systems+in+OpenSim](https://simtk-confluence.stanford.edu:8443/display/OpenSim/Coordinate+Systems+in+OpenSim)

![[Untitled 611.png]]

From Vicon requires a 90 translation in Y