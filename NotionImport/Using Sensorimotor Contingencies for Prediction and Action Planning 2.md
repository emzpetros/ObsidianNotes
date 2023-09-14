---
Authors: Alexander Maye,Andreas K. Engel
pdf name: Maye-Engel2019_Chapter_UsingSensorimotorContingencies
DOI: https://link.springer.com/chapter/10.1007/978-3-642-33093-3_11
Publication date: 01/12/2022
Literature Type: Book Chapter
Relevant project(s): Ankle Sim
Objective of study: |-
  Show model for prediction + evaluation of future sensorimotor events

  ”generate predictions about sensorimotor events from known SMCs”
Materials: |-
  Robotino: omnidirectional wheels, webcam, collision sensor, 9 distance sensors
  Accelerometer added

  Motor control: ramp up and down in speed vs instant

  Environment: one wall detectable by bumper sensor, other by current usage
  - needs to learn effects of actions using bumper + current sensor data

  Additional dynamic barriers 

  Value system: minimize bumps, current, acceleration spikes
Methods: |
  Action-observation pairs linked in tree
  New pairs update previous nodes so a history can be traced + length = level of tree

  Compute probability of the next action-obs pair based on history: each node is a probability distribution

  Prediction by looking at child of current node path OR “imagine” drop older action-obs pairs until sequence match is found
  - search for longest match, more information utilized

  Action Selection
  Combine values from each action in sequence to find seq w/ best value
  Average context size: avg math length, more info considered
  - lower value = less reliable prediction ?
  Values of action-obs pairs
  Weighting so action pairs w/ more frequent sensory features are worth more
  - Lower value = more likely alternative action is done
Theory: |-
  SMCT Sensorimotor contingency theory: “law-like relations” betwixt actions + resulting changes in sensory signals —> base for sensory experience + awareness
  - doesn’t rely on internal model

  Computational model: SMC as probability dist over pairs of actions + related changes in sensory signals based on database of actions + observations

  Link SMCs
  - Previous SMC seq = “remembering”
  - SMCs can be arranged in new sequences 

  Propose a method for evaluating plans that considers state value but also frequency of state, likelihood of it happening, prediction reliabiltiy
Outcome Measures: |-
  Path lengths, observed movement
  Acceleration, current of motor, collision rate, turning probability (straightness of movement)
Key Results: |-
  With learning robot had smooth transitions and minimized current consumption, accel peaks, + bumper triggers

  Unexpected changes
  - Struggled with front obstacle, initially had learned not to associated bumper data with a forward obstacle
  - exploration needed, no previous seqs
Conclusions: |-
  Collision avoidance without distance or camera sensors
  Switches to exploration in a dynamic environment 

  How does this hold up in more complex environment?
  - theorizes that complete exploration of tree not needed + that actual experienced seq is small relative to all possibilities 
Future work suggested: Real-world testing
Citations: "8"
Core paper?: No
Journal: From Animals to Animats
Key terms: Markov model,action planning,robotic limbs,sensory-motor contingencies
Name:
  - "[[Using Sensorimotor Contingencies for Prediction and Action Planning]]"
Status: First Pass
---
