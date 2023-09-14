---
Authors: Fumihiko Nakamura,Kuniharu Sakurada,Maki Sugimoto,Masaaki Fukoka,Michiteru Kitazaki,Ryota Kondo
DOI: https://doi.org/10.1145/3519391.3522754
Publication date: 04/18/2022
Literature Type: Paper
Relevant project(s): Ankle Sim,Crowdwalking
Objective of study: How does the frame of reference affect embodiment and motor control?
Summary: |-
  Investigating how reference frame of robotic limb control affects embodiment 
  Virtual arms manipulated via trackers on feet by controlling the tip position (IK calculated)
  Torso vs head frame had lowest reaction time and straightness
  Torso vs space frame had highest body ownership 
Materials: |-
  Oculus Rift CV1, Touch Controllers 
  Unity3D
  Character Creator 3.0
  Final IK to calibrate between avatar and user : used to calculate rotation of spine bone
  HTC Vive trackers on shoes, 2x base stations
  Vibration motor triggered by Arduino Uno via serial communication 

  3D model of limb from designer: links scaled to be 1m

  Anchoring of Limbs: space = world coordinate, torso/head = child objs on bone of avatar

  Manipulation of virtual limbs: 3DoF
  Tracker position offset upwards and rotations translated from reference frame to world coordinate movement, movement continued until error between actual and target tip position of robotic limb was below a threshold 
  Rotation of wrist synced w/ rotation angle of tracker
Methods: |-
  Point to point task controlling robotic arm w/ legs in VR: hit targets that appear in random positions in an arc in front of the user, contact noted visually and with vibration IDEA replace with stim

  IDEA questionnaires on embodiment given in VR 
Theory: |-
  Reference frame for robotic limb can be relative to a fixed point, centered on torso, or centered on head
  Improved agency and body ownership of such limbs improve dexterity [16, 27, 29]
  Embodiment has been shown to happen with visually different libs

  Lower limbs used to control upper due to high “interactivity” - body remapping

  Space Frame: usable when robotic limb is not in same space as user

  Torso Frame: limbs attached to torso to help with balance

  Head Frame: used by people with motor disabilities, mostly done w/ VR with easy access to spatial head coordinates 

  Previous studies for hand: users choose motor control to minimize straightness + jerk of trajectory 
Outcome Measures: |-
  Jerk minimization of virtual limb + foot during reaction time

  Task performance: sum of reaction time and D = dif betwixt straight line distance start to end and actual path length
Key Results: |-
  Reaction time, movement straightness + priority sig high in torso
  Ref frame affected embodiment, motor control process, _ task performance 

  Reaction time decreased for each session + D (straightness) was less variable

  Embodiment occurred for all reference frames
Conclusions: |-
  Improved torso frame outcomes may be due to placement of virtual limbs as similar to human body
  Lesser head frame outcomes may be due to placement of limbs far from midline
Future work suggested: |-
  Examine other reference frames
  Results may change with differing DoF
Critiques: Virtual foot does not appear to move with real foot
Citations: "0"
Core paper?: No
Journal: Augmented Humans 2022
Key terms: VR,emodiment,motor control,reference frame,robotic limbs
Name:
  - "[[The Reference Frame of Robotic Limbs Contributes to the Sense of Embodiment and Motor Control Process]]"
Status: First Pass
---
