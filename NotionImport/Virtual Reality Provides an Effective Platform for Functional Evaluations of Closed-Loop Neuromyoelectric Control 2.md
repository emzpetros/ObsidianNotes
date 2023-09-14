---
Authors: David M. Page,David T. Kluger,Douglas T. Hutchinson,Gregory A. Clark,Heather L. Benz,Jacob A. George,Janell S. Joyner,Suzanne M. Wendelken,Tyler S. Davis
pdf name: Virtual_Reality_Provides_an_Effective_Platform_for_Functional_Evaluations_of_Closed-Loop_Neuromyoelectric_Control
DOI: https://doi.org/10.1109/TNSRE.2019.2908817
Publication date: 04/02/2019
Literature Type: Paper
Relevant project(s): Ankle Sim,Crowdwalking
Objective of study: Assess VR closed loop performance translation to physical world
Summary: Closed-loop systems in VR are effective for obj identification.  Less effective for ADL tasks
Materials: |-
  Utah Slanted Electrode arrays, 100 electrodes median + ulnar nerves
  Intramuscular iEMG w/ 8 leads and 4 electrodees each 

  Multi-Joint dynamics with Contact VRE

  Simulations from XML scripts, real time I/O via MATLAB

  NON-IMMERSIVE, screen view 

  virtual Modular Prosthetic Limb, LUKE arm
Methods: |-
  Infrared camera tracked reflective markers
  Motive software translated movements from world to virtual

  Both freq + amp modulated to change intensity

  Jitter added to add realism + reduce habituation [5]

  Open Loop Task: identify stim at 3 intensities, 4 locations 

  Close Loop Task: identify above obj (none, small or large cylinder); identify large or small + soft/hard

  Task made harder w/ medium size + compliance

  Physical task: 2x2 identification

  Texture Identification

  Various ADL tasks from standards or custom
Theory: "90 s breaks to minimize sensory adaptation "
Outcome Measures: Confusion matrices for obj identification, P/F for ADL task within 60s; sensor output
Key Results: |-
  VREs suitable for identifying virtual obj properties - could be used just to indicate stim parameter effectivness
  Virtual PH can predict performance for obj id tasks, but if you can’t do it virtually doesn’t mean you can’t physically
  Virtual ADL did not improve w/ sensory feedback: task difficulty, tasks not relying on sensation, small # trials
  Virtual ADL tasks may be harder than physical 
  Qualitatively greater embodiment (strong reaction to feeling door)
Conclusions: |-
  Closed loop control of virtual PH w/ real time control / communication 
  Points to VRE acting as validation for closed-loop control methodds irl
  VR great for object id: repeatable, no secondary cues
  VR not predictive for ADL
Future work suggested: |-
  Higher sample size
  Better bug checking!: oscillating input corrected to 0 by physics engine led to no stim
  Worth trying AR for ADL
Critiques: What are typical ADL tasks for lower limb that could be done in VR?
Citations: "10"
Core paper?: No
Journal: IEEE Transactions on Neural Systems and Rehabilitation Engineering
Key terms: VR,myoelectric,sensory restoration,upper
Name:
  - "[[Virtual Reality Provides an Effective Platform for Functional Evaluations of Closed-Loop Neuromyoelectric Control]]"
Status: First Pass
---
### **Abstract**

  

### **Overview/key points**

Motivation

- Difficulties with physical limb: cost, fitting, maintenance
- Possible benefits: _lack_ of cues such as socket interactions + sounds
- Repeatability
- More detailed feedback + timing information

### **Methodology/Theory**

  

### **Materials/Fabrication Methods**

Immersion level not quantified

“motors could be moved in a “velocity” or “position” mode, and the mode of each DOF was independently toggled depending on the task. Velocity control is employed by conventional  
myoelectric prostheses; the joint angle of a given motor stays constant until a flex or extend signal is detected, at which time the motor moves. Position mode has a rest joint angle, and the DOF will return to this rest position when no intended movements are detected. The distance the joint moves from  
rest is correlated to the intensity of the decoded signal.”

### **Experimental Procedure**

  

### **Experimental Results and Discussion**

  

### **Outlook/Future Developments**

**Questions for critical engagement:**

- **What was the research question/problem?**

  

- **Is this title of possible value to my study?**

- **If so, why do I think so? (If not, stop at first pass)**

  

- **What is the author of this paper attempting to persuade me of, and am I persuaded?**

- **If not, why not?**

  

- **Which part of this paper is of most interest to me and why that part?**

  

- **Why have they chosen this approach or theoretical framework?**

- **Do I agree with the authors reasoning for this?**

  

- **What does the author think are the implications of their findings?**

- **Do I agree with the authors reasoning for this?**

  

- **What does this paper contribute to my own thoughts on my own research?**