---
Authors: Eric Rombokas,Nataliya Rokhmanova
DOI: https://doi.org/10.1109/ICORR.2019.8779518
Publication date: 07/29/2019
Literature Type: Paper
Relevant project(s): Dual Task
Objective of study: Assess a thigh mounted vibrotactile system to communicate foot placement
Summary: Vibrotactile feedback system proved effective in discriminating foot placement on stair edge
Materials: |-
  4 FSRs in insole, toe to heel
  Controls wore ski boot to eliminate plantar sensation 
  Thigh band: 7cm apart at 70Hz found to be ideal [31, 32], eccentric rotating mass motors
  Arduino Uno: I2C communication from FSRs to ERM motor; data collection via Robot Operating System serial
Methods: |-
  Discrimination of tactors: noise cancelling headphones 

  Simulated stair stepping: user indicates foot position on stair edge (not in view)
  Sliding hidden stair

  present possible positions to participant

  Accuracy calculated via actual tactor vibrations vs the intended placement of the sliding stair
Theory: |-
  Lack of proprioception leads to risks for amputees, particular difficulty with stair descent 
  Foot placement relative to stair edge important to decrease falls

  Prosthesis strategy: “roll” foot over edge to compensate for additional push off of prosthesis, need to visually confirm placement of foot

  Non-invasive feedback: alert if gait params are out of range, biofeedback, translate gate characteristic to artificial stimuli 

  Thigh chosen for surface area + proximity to amputation area
Outcome Measures: |-
  Accuracy of tactor identification
  Accuracy of foot placement identification 
Key Results: |-
  Vibration amplitude + spacing sufficient: supports anterior of thigh having higher specificity than posterior 

  Foot placement:
  All but two controls improved, vibration distracting, experience with ski boots
  Both amputee subjects improved (20 and 15%)
  - had lower baseline performance
  - most improvement in those with poor foot placement detection w/o feedback

  Did not appear to be difficulties with multiple tactor vibrations in T2

  Subjective Results: confirms suspected foot position, multiple tactors better than single
Conclusions: "Vibrotactile feedback promising "
Future work suggested: Is pressure feedback more effective (same modality)
Critiques: |-
  Interesting analogue experimental setup for able-bodied with ski boot, would need to screen controls better for familiarity with ski boots

  Simulate stairs in VR?
Citations: "4"
Core paper?: No
Journal: 2019 IEEE 16th International Conference on Rehabilitation Robotics
Key terms: haptics,lower-limb rehab,prosthesis,sensory feedback,stair descent
Name:
  - "[[Vibrotactile Feedback Improves Foot Placement Perception on Stairs for Lower-Limb Prosthesis Users]]"
Status: First Pass
---
