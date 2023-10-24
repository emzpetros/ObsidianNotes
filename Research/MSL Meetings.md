# Eric Heidorn

Trail-making test: random map of numbers / letters
- Connect 1-5 and then 1-A-2-B...
- Improvement potentially due to better oxygenation to brain after single legged cycling 
Cross education
- Performance improvement in one limb transferred to other limb 
	- Interlateral or bilateral transfer - skill transfer
	- Strength, skill changes 
- Mech?
	- No consistent muscle adaptations
	- Maybe spinal circuitry, not sure of specific paths
	- No change in H reflex 
	- H.Lim and S. Madhavan 2023: cortical interconnection, activation of ipsilateral descending pathway, facilitation of spinal circuits 
	- Could look at this in SCI and isolate CNS from peripheral mech




# 9/19/23
Gait Phase Detection during Post-Stroke Ambulation - Hailey

Stroke
- Ischemic or hemorrhagic 
- Also show downstream effect of stroke
- Walking impairments: fall risk, slower, less efficient
	- Lower toe clearance
- QoL: independence, community engagement, physical/mental health

Stroke Hybrid Exo
- Motor assistance + stimulation 
- Stim itself may not get strong enough contraction 
- Assistance throughout gait, have to detect gait phases

Control Schemes
- Threshold based: foot-floor contact, joint angle
- IMU based finite state machine even for foot contact
- Looking to transition between walking states i.e. standing, overground walking, stairs

Limitations: generalization + adaptability 
- step to step issues
- Apply ML to improve upon state machine control, work with varied speeds + steps
- Predicting future trajectories of system
	- Delay from stim onset to muscle contraction
![[Pasted image 20230919095558.png]]




# 8/22/23 summer students pt 2

Biodex and cart moved to the tissue health lab

New key needed and new scheduling

  

  

  

  

  

# 8/8/23 Summer Students

Connor Kacenjar

- Correlated metrics: stride length, time, speed
- Mostly stepped over

John

- Fall detection for exos

Mau

- Input impedance of sensors? mismatch would divide current
- Where is EPM noise coming from

# 7/25

Able bodied control comparison

Integrate DT into homegoing to assess possible plateau with integration of sensory feedback

Is LL02 prioritizing cognitive

David Cunningham: skin conductance under DT

  

Notes from Hamid

Justification that they were always presented with neutral, then CC and then IC? why not randomized

You may want to report accuracy in a table as well

SNP inactive and active: posthoc test should determine where it happens? It’s an overall effect?

Evidence on prioritizing cognitive task vs motor task for LL2 as opposed to LL1 and LL3?

Gait stability measures

Talk to David Cunningham (edited)

# 7/11/23

iNET

- Spark, seed, spread: depends on prototype stage
- Any VA employee
- Ex: gravity assist spark
    - E-bikes don’t account for gravity resistance
    - IP65 level, dynamic inclinometer + rasp pi control
- Ex: shower chairs, too big for some bathrooms
    
    - Adjustable flap, clamp
    - Adjustable legs to change height
    - Think about padding
    
    ![[Untitled 176.png]]
    

Mammography Chair spread

- User can’t sit when machine is flipped upside down
- Cutout in mammography chair for machine to slot into
- How many manufacturers? several but most machines are similar
    - Smaller than the model we have

vehiCLE Center Overview

- VA engineering health innovators: CLE
- Design + fabricate high-level functional prototypes
- Extrusion, molding, resin, FEM

![[Untitled 177.png]]

- Projects
    
    - Stimulatred exercise sleeve
    - Cord orga for hybrid exo project
    - Cont glucose monitor compression prevention
    
    ![[Untitled 178.png]]
    
- own funding
- Stephanie.Bailey3@va.gov

  

# 6/27/23

Marshaun Fitzpatrick: improving hemiparetic gait with hybrid exo

Stroke: blood vessel blocked or bursts

Hemiparetic gait

- Slow speed, asymmetry, reduced balance / stability
- Compensates with hip hike, circumduction, stiff-legs, less weight on affect side, toe first / flat foot at foot strike
- Kinematicly: swing - reduced hip, knee flexion; reduced knee extension + dorsiflexion
- stance - knee instability , reduced peak hip extn + plantarflexion of ankle

Treatments: brace, PT, FES, exo

Exo solution: stim + motors to help reduced strength, controller states helps with incorrect timing of muscle activity

- Fitment: thigh cuff, shank cuff, footplate
- Actuator: frameless brushless DC motor, continuous torque 17 Nm, peak 51 Nm; supports walking speed 1.6 m/s
- Sesnors: IMU, potentiometer, FSR for heel /toe contact
- Controller: finite state machine, transitions based on limb kinematics + foot contacts

![[Untitled 179.png]]

  

Slight delay from sim to response: earlier threshold, delay motors to match timing

  

Outcomes

- conditions: no assis, motor only, stim only, both
- Kinematics: ankle dorsiflexion during swing, knee extension at foot strike, knee flexion during swig, hip exensntion
- Speed, step length, gait symmetry
- Effect of combining / only one assist

  

Show context, baseline comparison: unimpaired leg

Could weight be causing oscillations

  

At comfortable walking speed: improved toe clearance, better loading response, increased ROM

Add more feedback control, less reliance on hand tuning, more general framework

  

What are you focused on?

- Matching kinematics of normal gait, some kind of nominal comparison for gait

# 5/30/23

Eric Heidorn - Blood Flow Regulation during Orthostasis in Individuals w/ Paralysis: Ventilatory Training Intervention

Pulmonary Fxn post SCI

- Reduced volumes, less muscle strength, more dead space
- BP regulation: baroreceptors stretch = increase BP : loss of this sympathetic innervation in SCI ( No parasymp)
- BP adapts to higher values ex exercise or hyper tension
- SCI: sympathetic thoraic / / lumbar area, high level energies lose sympathetic heart control, can’t increase as easily - comes from periphery not direct innervation
- quick response , 2 heartbeats
- Sit up test: supine to seated, quick adjustment + increase in able bodied, drop in SCI

![[Untitled 180.png]]

Ventilatory muscle training: mitigate decreased pulmonary fxn

- may indirectly affect cardiovascular, increase sensitivity of baroreceptors

Orthostatic tolerance test: supine for 10, upright for 10 minutes

- Constant BP measurement
- NIRs device: blood in + out, measure scattering at various wavelengths, O and deO Hg
- 40 mm apart, 2 cm down into brain

Results

- No sig change over 8 wks
- Somewhere in breath we don’t use full muscle use
- LOTs of variability : maybe group by injury type, look at subj by subj
- Need a large interthoracic pressure to sensitive the baroreceptors

Cerebral Regulation of BF

- 60 to 160 tightly controlled
- Higher than range, more effects, stresses arteries
- Cog fxn before + after
- Would want to keep blood flow to brain - better cog fxn

Orthostatic tolerance + CBR w/ SCI

- drop in arterial pressure, HR tries to increase, not successful, lower Cardiac output: symptoms of light headedness
- SCI has low but not always displaying symptoms: some kind of mech

![[Untitled 181.png]]

Tests may be too late in the day, more issue in the morning anecdotally

One indv has trunk stim system, muscle activity may improve BP

What factor would you adjust? they are interrelated, higher cardiac output - wouldn’t need to maintain high HR to keep that up vf

# 5/2/2023

Site visit July 13

Suzhou Li - Electrically Elicited Sensations to Reduce the Risk of Falls for Individuals with Lower Limb Loss

  

Background: 1 million w/ limb loss, fall risk, important part

- Plantar sensation: smooth + stable gait, body position during falling
- Plantar sensation can affect many aspects of needs for lower limb devices
    - propriocepton: know where the prosthetic foot is in space, related to loading only (not foot just up in space)
- SNP: feels as tho it comes from missing foot
    - Previous work, postural stability, navigation of challenging terrians, energy expenditure

Characterize modulation of spinal reflex pathways

- H-reflex: sensory motor control, sensation to modulate motor output
- Peripheral nerve 1a fiber synapses on motor neuron + feeds back to same muscle
- Mechanoreceptors modulate H-reflex via pre + post synaptic inhibition
- Plantar cutaneous: indirect control, contributing to how much proprioceptive fibers contribute to the H reflex arc
- Exp: postures to mimic phases of walking
- Data: PCA, measure H + M wave peak to peak, normalize by baseline EMG ebfore
- Results
    - Linear regression model: M-wave, posture, EES → H-reflex amplitude
    - EES no effect on amplitude in early + midstance postures: doesn’t interfere
- Muscle configuration after amputation unknown: same pulling as with intact limb may not occur
- What does EES not interfereing with spinal pathways mean functionally
    - Will not overexcite reflexes leading to jittering walking: won’t trigger flexion reflex when foot is on ground
    - Don’t need a new stimulation scheme

Evaluate sensation on stumble recovery strats

- Recovering from trips: reduce forward rotation with foot/ankle and hip
- Appropriate foot placement to redirect GRF + stop forward fall
- Peak trunk flexion angle velocity
    - peak ankle decreases in LL1 participant
    - LL2 did not see same decrease, they’re very good at recovering
- Stride length or perturbed leg
    - Intact perturb doesn’t change
    - LL1 and 2 take shorter step, LL3 takes longer
- Peak GRF magnitude on recovery stride
    - Perturbed on prosthetic stride, GRF on same limb
    - Maybe better control of when they fall, use less force
- Changes for prosthetic side perturb
    - Consider trip on intact limb: prosthetic limb becomes stance limb, no control of ankle joint

  

Q&A

- Functional significance
- With and without data: show trend lines
- Could not figure out why H reflex didn’t occur sometimes
- Do they all receive same perturbation: yes, should maybe adjust on body weight
    - At maximum of acceleration
    - Could maybe modulate with stride length
- Should collect able bodied data
- Feeling safer is important too: ask immediately after each one

# 4/4/2023

Updates

- New Bertec MSL treadmill

  

Gabrielle Labrozzi “Gait Control after a Spinal Cord Injury”

  

Background

- Compromised musculoskeletal control, much reduced quality of life
- Walking restoration is a top priority
    - Transportation, decreases medical expenditure, chronic disease risk, improves join flexibility + muscle strength
- Functional Neuromuscular Stim: surface stim and/or implant
- Feedforward control: initiate steps via trigger
- Need to quantify gait
    - Gait variability : gait variabiltiy index, gait deviation index, mean + sd

![[Untitled 182.png]]

  

![[Untitled 183.png]]

Baseline Analysis

- Metrics need quantifying for SCI
- 5 walking trials

![[Untitled 184.png]]

Symmetry index: Robinson et al 1987

- General high variation

  

Gait deviation index

- 18 variable 9 perside, PCA to reduce dimensionality , GDI score
- suggestion of a significant decrease able to SCI, similar ranges found for other pathologies
- Lots of upper extremity effort

  

Add feedback control, using CoM!

CoM estimation

- Zero moment point as control parameter: global param with well defined patterns, computable from CoM, associated with stability
- Can’t be measured directly, estimated

Feedback control direction

![[Untitled 185.png]]

  

Exp design: 12 IMUs

- Markers = gold standard, origin point moves to support foot
- Rotation matrix
    - Individuals don’t walk in a straight line, rotation from previous foot to current foot, translate to body CoM vs global

![[Untitled 186.png]]

- IMUs transferred to segment

  

Results

- Group 1: able bodied 1-4, Group 2: AB 5
- Choose one with low error but also takes into account asymmetry for SCI patients
- Looking toward real time validation study

  

Fowrard Direction

- Discontinuous walking pattern
- COM acceleration: areas of toe off and heel strike in AB
- Replicating SCI gait: pattern lost

  

# 3/21/23

Updates

- Post doc interview next week

  

Sandra Hnat - SCI Hybrid Project Update + Future Plans

- Currently need funding
- Background: powered exos
    - Pelvic band, electric motors, ankle orthosis
    - Reduction in pain, spasisticy, better bowel fxn, muslce tone
    - Control: electric motors take over during different part of gait cycle
        - Controller for each join to follow velocity + angle, spring + damper model
    - Too slow for community use , need crutches / walker (upper extremity effort), muscles don’t contribute to movement
- Overview MAHNP
    - Hybrid: stim + exoskeletal movements : muscles first
    - Biologically inspired controller : burst activity of muscles , don’t care how we get to target
    - Biologically Insipiried Iterative Learning Controller: adapt exo to each pilot
        - Still doing muscles first, modulates muscle burst
- Ankle perturbation
    - Some powered exos have balance control
    - Using zero moment point: biped is stable if contact force is oppoite of inertia and gravity
        
        ![[Untitled 187.png]]
        
    - Sum of total moments = 0, project point on ground
    - ZMP approximation with COM: IMU sesnors
    - Ankle perturb
        - Calc COM with XYZ marker positions for gold standard, calc with IMUs
    - Can MAHNP design assist with maintaining upright balance
        - Standing perturb with and without Partial differnential controller
    - Exps: volitional (move jar), unexpected, hands free
        - Magnitude found by increasing based on participant comfort
    - prelim
        - Usability rating: not huge differences
        - Ankle : target ankle varies per person, visually seems to be closer to target angle with controller
- Corset fitment
    - Aligning joint centers of rotation
    - Rotation at knee, upper turns inward, lower turns outward
    - Corset solutions
        - Custom corset (expensive), reuse same one (not flexible enough) off shelf TLSO (motors move too much)
        - ReWalk pelvic band for now
        - long term - adjustable corset
- Future Plans
    - Improve BIOTILC: stance controller, feedback control, bilateral
    - Fall mitigation: lock joints to slow fall
        - Crash test exo to measure forces
    - Supplement commercial exo with fes
- Garverick Project: ES attachement for commerical exos

  

IMUs to speedgoat interfacing

- skh63@case.edu
- Wired , serial communication?
- 9-axis might not use all of them , may just use orientation
    
    ![[Untitled 188.png]]
    

  

# 3/7 2023

John McDaniel

Practical approaches of PULSE racing in training their athlete for the cybatholon global edition FES bike race: a case report

- Rotating team of undergrads
- Borrowed from traditional exercsie
    - Vs pyramid, mostly low, then mid, 5% high
    - Low and high suspected use was just weighted extension

![[Untitled 189.png]]

- Plan: macro, meso, micro (8 months, 6 wks, 4 wks)
    
    ![[Untitled 190.png]]
    
    - Base, specific, tapering
    - 3 week cycles: recovery intermediate, high intensity
- 1500 meter trials across 7 mon
    - Some drop in time but also high variation

![[Untitled 191.png]]

- Kept to longer sessions bc of setup time
- Trying to maintain baseline level of activation throughout day with multiple sessions per day

  

Active lifestyle: ACSM 30 min, 5 days

- Active couch potato issue
- Maybe improve mitochondrial function before focused muscle function / performance
- Lit points to mitochondria affecting muscle performance a lot
- disuse leads to less mitochondria + dysfunction then muscle atrophy
    
    - Protein synthesis interrupted
    - recovery is slower in SCI
    
    ![[Untitled 192.png]]
    

![[Untitled 193.png]]

- Prime muscle throughout the day, low stim to improve mitochondiral fxn
- Study with low level stim

# 2/21 Kevin Foglyano

Updates

- New crash test dummy available

  

Adapted Exercise

- Lower limb paralysis have a hard time getting enough exercise
- Biking system: stimulator + crank angle sensor, can be done outside

Spread beyond VA

- Surface stim taken to three different hospitals
- VA Teams: translational education + mentoring program, move toward commercializaiton
- ExerSTIM: supplemental gear to adjust commercially available exercise equipment
    - 8 channel surface stim, sensor, app, safety
        
        ![[Untitled 194.png]]
        
        ![[Untitled 195.png]]
        
    - User interviews:
        
        ![[Untitled 196.png]]
        
    - Really want higher heart rate, reduce set up / tear down time

Rowing, VR, Virtual cycling academy, long distance riding

- VR Cycling Academy
    
    ![[Untitled 197.png]]
    
    - Peleton type environment
    - **Would the Virtual Cycling Academy have a solo setting**
    - Focus on accessibility
        
        ![[Untitled 198.png]]
        
- Avatar stops and starts with person: needed to add multiplier to effectively start again

  

VR! can a VR environment trick the body to a better physiological response (HR, fatigue, muscle oxygenation

- Get them more engaged, compensate for lack of body response since muscles are triggered via stim only
- Cycling: tied to cadence sensor
    - Grab collectables, turn with head
- **Phone VR?**
- **Third person view?**

  

Long distance: advanced controllers

- Match cadence only
- Still using 360 plot, whole muscle groups on or off regardless of cadence

Other ideas

- Tandom bike
- hand crank for front wheels
- Big hill: small motor to assist

  

Questions

- Other populations for biking? stroke?
    - Stroke + MS, Mineapolis team looking at rowing + stroke
- Rachel Mann: ASCU with implant recipients

  

# 2/17 Nathan Makowski

Research Update

Background

- Improving mobility + independence after stroke

  

COSMIIC SWARM: NNP open source, new modules

- Coms, power out, sampling, leakage current limitations, configurable pin mapping, IMU, ADC and filtering
- Smaller IMU sensor
- Reuse remote module packaging
- Evaluate DC leakage on existing connector interface : test imp betwixt cable and module body
- Detect current leakage failures, not determining what problem is

R01

- Implant IRS/IST systems + develop controllers
- Perturbation study: acceleration during walking, increases or decreases mag depending on fall or not, find magnitude of perturbation that would not lead to fall

Stroke hybrid: non surgery candidates, surface stim + exo skeleton knee

- thigh + shank orientation, no measure of hip flexion

  

# 1/24 Aidan Friederich

Expanding Seated Posture for Individuals with Trunk Paralysis through Feedback Control of Peripheral Nerve Stimulation

  

Spinal Cord Injury: c

- Communication from CNS to periphery interrupted
- Depends on level + severity
- Large effect on QoL: improve it by increasing indep

FNS: implanted stimulator, IM electrodes

Seated stability

- Justifcation: need stability for reaching
- Improves posture, reaching distance
- Improvements: resist perturbations, hold different postures

Aim 1: enable upright + leaning postures

- Previous upright controller: accelerometer for trunk tilt
- Apply perturbations (forward push), test controller to resist this
- Updated to resist in multiple directions, two PID controllers, new task to move weighted jar to places on table
- Results
    - Pitch + roll angles, area of movement ellipse : reduce area in 2 subjects
    - Time to reach max + min angles of pitch: 4 saw reduced time to return to upright - less time in unstable configuration
- Leaning postures- balance muscles

Aim1.2 id trunk + hip muscle contractile properties

- find muscle recruitment curves: not linear
- Hypoth: model by sigmoid recruitment curve
- Tested over 4 subjs, 44 muscles; model was good fit
- Co-activation of muscle groups: co activate groups → force and moment vectors add linearly
    - Two back muscle, one on each side → extension only with lateral forces cancelling, ideally
- 24 co activations, separate + together sim
- Plotting N of co acti vs mag / direction of force → linear
- Characterize subject moments of leaning positions + moment production from FNS at postures
- Conclusion: could model nonlinearities via system identification

1.3 static controller

- lots of muscles, calc many times / second: use muscle synergies (groups of muscles together?)
    
    ![[Untitled 199.png]]
    

![[Untitled 200.png]]

- results: increasing forward reaching distances
- moderately stable to very stable during reaches
- Resistanct to ext perturb up to 90
- Synergy based feedback can allow for static forward leaning postures, can obstain with reduced resistance to perturbations

  

In the home?

- Networked neuroprosthesis: implanted accelerometer
- Placement is surgeon dependent

  

Aim 2: create reliable + accurate measure of trunk posture from a group of sensors with unknown orientations

- combine everything
    
    ![[Untitled 201.png]]
    
- Rotate with rotation matrix to align sensors
    
    ![[Untitled 202.png]]
    
- Convert to pitch and roll angles
- Sensor fusion with weighted average or townsend algo
- Experiment: 6 accelerometers
- Optimization to rotate + convert to pitch and roll

  

Additional work: trajectory tracking, nonlinear; translation to home - ADL tasks, NNP, take home study

  

Feedback

- ID major scientific goal, show how you test hypothesis not just list aims
- Define drastically with numbers
- Synergies? underlying philosophy / motivation behind this
    - Nervous system control of multiple muscles
    - Architecture for simplifying system
- Question, exerpimental method , results
    - Not chronology
- Need to show neural and muscle anatomy

  

# 1/10/23

Elizabeth Hardin: Walking When Challenged

- Parkinsons, stroke

Background

- Walking is complex: feet back and forth, sensory, left + right motor + left / right field vision

  

Parkinson’s Project: what triggers freezing of gait + how DBS can help

- Initially looking for a biomarker for earlier diagnosis
- Different doorways for people to walk through, changed to a hospital hallway + modulate optic flow
    
    ![[Untitled 203.png]]
    
- 10 PwPD bilaterall subthalamic DBS and 8 age matched control
- 10 and 5x optic flow, randomized, 2-3 minutes at each condition
    
    ![[Untitled 204.png]]
    
    - First one should be right step length
- See instantaneous walking speed drop + then catch up phase with overshoot + plateau
    - Hip markers + malioli (feet)
- Split by leg
    
    - Controls have narrow variability in metrics
    
    ![[Untitled 205.png]]
    
    - Spread for DBS off
- Optic flow changes
    - Foot height decreased DBS off, length + duration increased
        - Did not change between optic flow velocity
        - Some left and right disparities
    - Either no differences in flow or compensation was too fast
- DBS effects
    - 5/10: foot height increased, 8/10 length increased, 8/10 duration increased
- Symmetry: Disparities between right and left sides
    - Controls: close to 1, perfectly symmetric
    - DBS on and off similar asymmetric results
    - Skewness in phase: high variability between patients
    - Width ratio, close to 1 is similar values
- Conclusions: little effect of optic flow on kinematics
    - Could be useful for system reweighting when 2 systems conflict, maybe a visual dipendence
    - PwPD may depend on internal visual mechs not proprioceptive / vestibular
    - Participants may look at floor not at optic flow
    - Maybe length + height may be controlled by different neural correlates than the ones controlling time matrix (left + right coordination + step phase, no changes)
    - DBS stim patterns: larger volumes of activated tissue —> larger effects
        
        ![[Untitled 206.png]]
        
        - Dr. Aasef Shaikh
- Limitations: only 10, difficult to walk without holding on to treadmill, need to analyze arm swing data, fatigue possible did not measure , done at end of medication dose cycle ; not directly comparable to overground but need to start here
- Future: subthalamic DBS, look at vestibular system + heading perception, suspected it will correlate with veering, find sim strat to modulate deficiets
- Q&A
    - No one froze during exp, were changes in input severe enough to trigger effect
    - Use AR to change what people see, confusing inputs , things on wall in addition : objects of multiple sizes
        - Give participants glasses to focus on screen, could it work with an oclulus to prevent looking at feet
        - Changes in adaptation to optic flow with DBS? quicker, delayed?
            - Hone in on transition, slope of the line changes
    - Effect of treadmill on feedback to system: depends on treadmill power
        - Can’t control it, hoping it’s the same effect on all participants
        - May be something to look at it : look at unpowered treadmill

  

Stroke: novel motor training task with transcutaneous current stim

- Background
    - Sides: reduced motor abilities in opposite side, extra activity bleeding over from one side
    - Non invasive stim: better than sham in TUG timed up and go
    - gait training with tDCS led to increased excitability
    - Non looked at simultaneous stim + novel motor task
- Exp:
    
    ![[Untitled 207.png]]
    
    - Blind to who gets actual stim
    - Obstacles to step over: 34 along path, vary thickness + height
- Results: increase in gait speed, Fugl Meyer gains stayed 3-week post, TUG going down vs baseline , FGA increasing
    
    ![[Untitled 208.png]]
    
- Looking to test efficacy of intervention

Activities of Daily Living Data: one above knee prosthesis, mostly able bodied

Muscle Vibration Study:

  

# 12/20

Hamid Charkhkar: Neural Interface Tech to Restore Sensry + Motor Fxns in Individuals with Lower Limb Loss

Implant surgeries

  

Here is how you can access the files from my anatomy talk back in May:  
On R drive, go to :  
Triolo_lab\database\lab_meeting_presentations  
If you have access to ReLLiNC platforms, you can get the files from the following directories too:  
R Drive: 01.Study Folder\Triolo 1583890 Rellinc\Posters_and_presentations\MSL presentations  
VA Teams: under Rellinc Teams: General\presentations\MSL presentations  
Case Teams: Presentations-publications\presentations\MSL presentations

  

Our approach is better!Weir, Richard F.; Troyk, Phil R.; DeMichele, Glen A.; Kerns, Douglas A.; Schorsch, Jack F.; Maas, Huub (January 2009). "Implantable Myoelectric Sensors (IMESs) for Intramuscular Electromyogram Recording". IEEE Transactions on Bio-Medical Engineering. 56 (1): 159–171. doi:10.1109/TBME.2008.2005942. ISSN 0018-9294. PMC 3157946. PMID 19224729.

  

  

Establishing neural connection

- Cuff + intramuscular electrodes (sensing EMG)

  

Transfemoral Amputation

- microprocessor controlled knee: built in sensors to modulate mech resistance during phases of gait, no additional power (powered pros.)
- Note socket areas that are tight
- Surgical planning
    - Limited by anatomy + surgery tool sizes
    - Lead length
    - Locate nerve

Implanted components

- C-FINE
    - Built in anode strip for return ground: confine electrode flow to C-FINEs, reduce stim artifact + don’t need ground patch
    - Width x depth
        
        ![[Untitled 209.png]]
        
    - In-line connector
- Tetra IntraMuscular Electrodes
    - barbed tip for deployment + anchoring
    - Bipolar electrodes
        
        ![[Untitled 210.png]]
        
- One incision for TIMs, one for connector
- Percutaneous Leads:
    
    ![[Untitled 211.png]]
    
    - 2/ Cfine, 1 / TIM
    - twisted pairs, double helix
    - Skin grows in and locks in

  

Lead routing

![[Untitled 212.png]]

- Redundancy
- Unique ability to record distal to amputation

  

Surgery

- Identify sciatic nerve
    - Silicon shell to size C-FINE
    - Install + rotate to get better coverage
    - Leads tunnel to anterior incision, keep slack for leads on electrode side for mech. stability
    - 2 vs 1: selectivity? better to have one denser cuff?
        - 2 cuffs to maximize chance for plantar sensation
        - Is 1 insufficient? no, need backups
        - Even a higher density cuff only hits surface fascicles
        - Some overlap in percepts but still some unique
- TIM
    - Apply currents to look for twitches
    - Motor point vs muscle belly: confirm if we are in muscle
    - Slide peelable sheath to marked point
    - Load electrode into lead carrier (hollow cylinder)
    - Crack sheath + remove it
- In-line connectors
    - Push + twist silicone boot into inline connector
    - Dry connector + insert into perc receptacle
    - Tighten set screw + tie sutures
    - Route leads out one at a time
- Total time: routing, connectors, + closing takes a lot of time

X-rays

- Cuffs: orientation still same, enough slack

  

Q&A

- Why perc leads vs fully implanted?
    - Large number of contacts, implantable systems can’t accommodate all the channels
- Include outcome slides as well
- Yield on TIMs?
    - Need to interface with muscles more proximal
    - LE02 below knee are doing very well, hamstrings not responding, unsure why

# 12-13

Musa Audu: Two productivity aids for writing scientific manuscripts

EndNote: reference citations

- Separate EndNote software from Utech, but needs to be on Case Wifi (license)
- References in ribbon → smalll arrow, footnotes and endnotes buttons
    - End of document, can choose number format (1,2 vs i, ii)
- Commands:
    
    ![[Untitled 213.png]]
    
    ![[Untitled 214.png]]
    
- Change from 1,2,3,4,5 to 1-5: unlike refs from numbers
- Control shift s: change from superscript to [1] for ex
    - select endnote ref, format, and adjust font settings
- Developer → Record macro

  

MathType: Equation editing

- Not same as embedded equation Editor
- Add on menu

  

Latex note: open source but command-line based + hard to understand

  

# 11-15

John Schnellenberger: New Modules, New Wearable Surface Stimulator Capabilities, and an Initial Contact Detect Algorithm

  

New circuit board

- Added impedance measurement circuitry
    - Prevent burns from increasing charge density
    - Needs firmware and code to fully take advantage of it
- Ordered 50, 15 assembled, all need to be tested
- Modifications also being made to 0erc boards?
- Sensor serial interface board:
    - Nathan + Sandra’s projects
    - Natha: IMU data , speedgoat
    - Sandra: board in ASCU, process low level IMU data to send to controller + modulate stim , optional tablet application
    - Speedgoat, ASCU, bluetooth, buzzer, 4 pushbutton switches
    - IMU: adafruit \#4754 IMU boards ($25), multiple communication methods - we’ll use UART
        - Wired vs wireless: getting wireless data in real time to speedgoat is difficult, uses proprietary software, good for acquisition but not use in real time
        - Large amount of data coming in
- EMG processing
    - Contracted out
    - Interfaces with UECU, ASCU, or a prosthesis

Wearable Surface Stimulator Capabilities

- Allows 900 MHz wireless sensors or Bluetooth LE boards to connect
- Code in C
    
    - Can’t use Arduino environment ASCU or UECU
    
    ![[Untitled 215.png]]
    
- Finer current resolution : interesting for sensory applications
- speced to 250 but actually made to be 1000 us
- Develop UECU perc board based on WSS features?
    - Possible yes, could be a higher level programming language
- Analog or digital inputs for triggering? Probably not analog, maybe digital
    - Goal was to be small enough for a pocket
- Possible benefits to different stim pulses + double or variable freq trains instead of constant
- Motivation for dev? not knowing which pulse shape to use

Initial contact detect algo

![[Untitled 216.png]]

![[Untitled 217.png]]

- Sagittal plane angle crosses threshold then when it crosses zero
- A little early detection
- 99/100 IC events detected, works at lower + mid shank
- Only tested in able bodied thus far

![[Untitled 218.png]]

  

  
Rachel Mann: Updates to Tablet Applications and New Pulse Ramping ASCU Capabilities

- Triking / Rowing App
    
    ![[Untitled 219.png]]
    
    - Stim start up on ASCU green button press
    - Last used stim setting used by ASCU on startup: home use
    - Sync command: pulses start to drift over time, two boards used for output
        - Now timing can be maintained and separated
    - Battery hysteresis: battery drops during stim can trigger warnings
        - Keeps warnings constant, even after battery rises again post stim
    - Version Bluetooth crash, stop cycling if encoder link is lost, filing system compatible with s3 and A7 tablets
- Rowing App
    
    ![[Untitled 220.png]]
    
    - Use stim to find phase transitions : find thresholds with own muscles instead of being placed by clinician
    - Can use baseline trunk stim for stability
- Profiler App
    - Determine + save stim parameters
    - ![[Untitled 221.png]]
        
- Pulse Ramping + Freq Mod w/ ASCU
- Useful Skills
    
    ![[Untitled 222.png]]
    
- Suggestions
    - Participant ID instead of name
    - Default is non cuff: allowing higher current level
    - Can do real time adjustments via smaller button increments, slider available when stim is off

# 11-1

Holly Warner: Simulating Functional Neuromuscular Stimulation-Driven Gait with OpenSim Moco

  

Background

- Spinal cord effects vary by level of injury + complete vs incomplete + motor vs sensory
- Studies of rehab priorities - walking typically high
- FNS: walker / crutches for stability
- Want to develop close loop control to improve stability (reduce upper extremity effort)

OpenSim

- Simulate full gait cycle with assistive device under min. effort criteria for baseline stim pattern
- Use to create feedback controller
- Hill muscles models 46, 7 Hunt-Crossley contact elements / foot, torque actuator at shoulder + elbow (under voluntary control, don’t sim muscle)
- Assisstive device: reserve actuators or walker model of a structure w/ contacts
    - Moving toward better walker model

Control

- Optimal control: best control pattern given a set of requirements
    - Least fuel, time, smoothest path
    - Practical limitations: max speed
- Ex car
    - Hold one value then jump to another : max acceleration then at half time max deacceleration
        
        ![[Untitled 223.png]]
        
- Musculoskeletal
    - 46 muscles, 8 arm joint actuators, 5 reserve actuators → 150 states for joints + muscles + constraints
    - Need numerical optimization
        - Single shooting: start with control, try + evaluate + adjust
        - Direct Collocation: break trajectory into segments, ensure segments correct + slope is consistent with physics
            - No waiting on simulation of physics
- Application
    - Constrained by injectable energy to muscles + minimize upper extremity effort + match AB
    - Match contact elements on foot with GRF
        
        ![[Untitled 224.png]]
        
- Early results: wobbly + stiff legged but it walks
    - Reserve Actuators: largest 72N, 12% body weight (15% is consistent with standing)
- Group muscles to match stim channels + reduce usage of some muscles

![[Untitled 225.png]]

# 10-18

Speaker: Mike Miller

Presentation title: From manufacture and sterilization to reporting and surgery with lower extremity implantable devices: what do you need to know and what do I need to improve?

  

Motivation

- Underlies all subjects + data despite not being at forefront
- Improvement: standard methods, access, communication

  

Background + Context

- Motor on left 8 contacts; right 16 contact amputee (lower one has ground in cuff)
    
    ![[Untitled 226.png]]
    
- Recording: 2 places to record + two pins (y split)
    
    - TIM: 4 IM recording to 8 pin connector
    
    ![[Untitled 227.png]]
    
- All still implanted
    
    - Pin connected via conducting spring to another pin
    - Can cap it off: connector sleeve w/ filled silicon rubber to seal it off
    - Boot covers exposed metal
    
    ![[Untitled 228.png]]
    
- Implanted stimulators: 8 channel can record too
    
    ![[Untitled 229.png]]
    

  

Documentation:

- Technical drawing
- Finance: quote, order
- Verification: what we want + what we’re planning to make
- Shipment: certification of source materials, details of manufacture process
- Inspection: check packaging, integrity seals, sanity check of physical measurements
- Device tracking binder physically + placement in digital files: summary files
    
    - Database for each folder contents, inspection logs
    - **Checklist of steps**
    
    ![[Untitled 230.png]]
    
    - Investigational Device Logs: type, model, SN, manufacturer

  

Sterilization

- Packing list: specific device instructions
- Record of exposure profile, lethality of gas
- Devices air out to get rid of gas that seeped in
- Verify all devices are back : 3M stripe shows gas exposure
- Add date to investigational device logs

  

Consumption

![[Untitled 231.png]]

  

  

Q&A:

- Does steralization expire?
    - Up to us
    - CFINE: After a test FDA approved for 5 years
    - Event based expiration for everything before: sterile until wet or damaged
- Document on product rework?
    - Corrective process mech in place for APT + RDM has one also
- Part number: 90% of the time something we’ve come up with
    - List of part number to devices? Inside Aquisition folder → drawings

  

# 10-4

Speaker: Eric Heidorn

Presentation title: An Update on Blood Flow Restriction Exercise in those with Incomplete Spinal Cord Injuries and Ventilatory Training in those with Paralysis

  

![[Untitled 232.png]]

  

![[Untitled 233.png]]

- Measure occlusion of limb

  

BFR Exercise Study

- Baseline:
    - Blood draw for safety (clotting), looking for vascular growth + inflammation markers

![[Untitled 234.png]]

  

Preliminary Data

- Increases in torque at slower speed (60, 120 deg / s)
    - One subject had greater torque without extension
- No statistically significant differences for knee flexion torque
- Fatigue: 5-10 mins, relative change dropped more
    - Torque after exercise remains higher than without BFR training
- Questions
    - Measure of how well blood flow is constricted?
        - Doper ultrasound
        - Complete occlusion of arteries not needed, also blocking venous backflow
    - Muscles being blocked involved in extension? gluts + hamstrings, less effect on flexion
        - Gravitational pull of flexion, don’t have to actively pull down
            - Could they lie down and perform knee flexion / extension? : instrumentation should allow it
            - Or estimate weight of limb + known angle, calculate gravities contribution
    - Anectdotedly: walking + daily life became a bit easier, putting pants on
    - Do they use a walking device to walk? Could measure upper extremity exertion as well
    - Could group results by injury severity
        - Could initially do required stim + didn’t
    - Force generation: using peak as the comparison point, only one time point
        - Is it happening at the same point in the range of motion?
        - Area under curve? Energy over entire motion
- Still working on variation + muscle size data from CT scans

  

Pulmonary Fxn Training

- Higher level of injury associated with issues: problems coughing, exhale
    - muscles lower involved
- Measurements: total lung capacity, fxnal, tidal volume (Rest breathing)
- Train muscle to deduce decrements

![[Untitled 235.png]]

Orthostatic Hypotension: BP drop going upright

- Reduced pressure differences
    
    ![[Untitled 236.png]]
    

Cerebral Tissue Oxygenation

- Maintain BF to brain
- Transcutaneous stim → constriction of arteries → improved venous return → better BF to brain

  

Ventilatory Training: tap into muscle pump, increase barorecepeter sensitivity

- Weight training for the lungs: increased resistance or reduced diameter
    
    - Can it improve cerebral tissue oxygenation, can it improve cycling
    
    ![[Untitled 237.png]]
    
- intervention at home
    
    - 4 week follow up for long term effects: how often do you need to do exercises
    
    ![[Untitled 238.png]]
    
- Results
    - Improvements in maximum expired pressure: any improvement at such low levels is beneficial
    - Max voluntary ventilation improved
    - forced vital capacity (expire max vol from max inspiration): small increases
    - Q: what’s normal? how much change would you generally expect
- Results: more leveling out
    
    ![[Untitled 239.png]]
    

  

  

# 9-20

Presenter: Hannah Morgan

Presentation title: Restoring Sensation and Improving Tissue Health in Diabetic Amputees

  

Background: leading cause of amputations + it’s increasing

- Diabetic Peripheral Neuropathy: **have pathway diagram fade in so there’s less crowding**
- Build up of sorbitol, osmotic stress, NADH depleted = oxidative stress
    
    ![[Untitled 240.png]]
    
- Many effects: foot ulceration → amputation / reamputation
- Sensory neuropathy:
    
    ![[Untitled 241.png]]
    
    - Protective sensation: detect potentially damaging stimulus - ulcers
- Autonomic:
    
    ![[Untitled 242.png]]
    
    - Poor circulation: flow skipping capillary, reduced sympathetic tone (vasoconstriciton)
    - Heating tissue = vasodilation: reduced in diabetes
- Physiological issues not lifestyle factor
    
    - Reamputation: ulcer formation, higher amputation
    
    ![[Untitled 243.png]]
    
    ![[Untitled 244.png]]
    

  

  

Peripheral Nerve Stim: plantar sensation in our lab

- May improve tissue health: better perfusion, less inflammation

  

Aims

- Determine effect of PNS on perfusion + temp
    - Hypoth: stim will ^ perfusion + temp
        - general metrics, predictor of wound healing
- Char. elicited sensations in DPN
- quantify effects of SNG on balance, gait stability, symmetry

  

Thermographic Imaging

- 15 min baseline, stim for 10, 15 mins post
- Visual markers on limb
- Results
    - Trace of each time point, averaged over time - similar trends among points
    - Upward trend during PNS, but very small
- Comments: variability betwixt trials, days, individuals
    - Small temp changes, may not be significant
    - Noise in control

  

Improving methodology

- Following peripheral blood vessels, follows autonomic nervous system
    
    - Regions, heating is not uniform
    - Developing algo for edge detection along regions
    
    ![[Untitled 245.png]]
    
- Laser doppler fluximettry: 1mm depth, microvasculature
    - Measures speed = [] of RBC, correlated with blood flow
    - Dependent on probe placement: can’t compare betwixt subjects
    - Processing: char. freq peaks, energy content
        
        ![[Untitled 246.png]]
        
    - Verifying approach with test signal of known freq to find time average + get area under curve of each freq → energy contributions
        
        ![[Untitled 247.png]]
        

  

Experimental condition for ^

- Axon reflex: heat skin → vasodilation: reflex reduced or absent in DPN
- Mediated by autonomic nerv. system → FR2 band
- Protocol: warm contralateral leg to 45C for 29 mins
- Able bodied pilot: promising
    
    ![[Untitled 248.png]]
    

  

  

![[Untitled 249.png]]

- Will move to the mobility side of things eventually

  

Q&A:

- Detrended by avg value: take average at each time point + subtract from each trace, then avg again
    - Ensemble average
    - Take one trace + detrend so it’s centered at zero?
- Filtering? didn’t know what to filter by
- Initial decrease in 1st 15 mins? consistent across trials despite long acclimation time
    - Room is cold , would have to record for a while to see a point where it stops
    - Looking for relative temperature change
- Adaptation to PNS?
    - short period of stim
- Axon reflex: **hone in more on the absence of reflex vs presence**
    - PNS should trigger the reflex as would be in able bodied
- Response to a “thermal” challenge
    - Hoping to see restoration of autonomic reflexes
- Where in the flow do you expect to see improvement
    - Currently thinking it’s just transient when stimulating, may have a long term effect
    - Pointing to changes in sensation over time, may be some nerve plasticity
- Balance + walking ability
- Ways to measure inflammation??
- Metrics for chronic use of SNP? Maybe post doc, how SNP affects daily activity such as step counts (mobility)
    - Could be a therapuetic effect from increased activity
    - Apply stim pattern even while seated, fool body into thinking limb is there + provide resources to it
- Pulsing stim?
    - Could activate motor nerves to cause contraction + improve blood flow
    - Need to look into modulating params more
    - We know loading pattern of foot: record FSRs + “play back” stim pattern
- Careful of using just peripheral nerve stim: just moving the limb will cause effects but that’s been done

# 9-6

Speaker: Nathan Makowski

Presentation title: COSMIIC HORNET - SWARM Plans (acronyms to be defined during presentation)

Cleveland Open-Source Modular Implant Innovators Community plans for the Sensor Withdrawn from A Remote Module

![[Untitled 250.png]]

- IRS8 in the 90s
- IST16: could be 16 sim, 12 stim or 2 EMG recording sig, 10 stim
- Networked Neural Prosthesis: no external pieces, distributed modular architecture

![[Untitled 251.png]]

- IM: barbed tip to hook into it, stimulate metal part
- Spiral: wraps around nerve
- C-FINE: nerve reshaping, more contacts

Paralysis: hand function, trunk support, standing, stepping

![[Untitled 252.png]]

- NNP: not specific to just spinal cord stim
- Any version of closed loop control: modular + scalable multipurpose
- SWARM: DC powered sensors

![[Untitled 253.png]]

- Each remote module has 4 network connectors for branching

  

Creating new things is difficult!

![[Untitled 254.png]]

- Q&A: surgical expertise?
    - Will be relevant, may need in person training
- Want it to be used beyond current movement apps: autonomic control, surgery methods will change

![[Untitled 255.png]]

- HIVE: Gbur working on DBS
- Powered sensor support lead: people can develop new sensors w/o remaking the communication / power part
- External Gear: ew powering mech, recharging coil, support ext accelerometer sensors
- High Frec Block: prevent AP from traveling down nerve

![[Untitled 256.png]]

- Vagus nerve stim - various regulation, walk after stroke, hand system

![[Untitled 257.png]]

- Flexible circuit connections that can fold
- Can retool w/o distributed architecture, get down to minimum hardware

![[Untitled 258.png]]

- Support variety of DC power sensors
- Previously all electronics are all inside module
- Remote placed sensors: i.e. IMUs or other could be placed where a module can’t go

![[Untitled 259.png]]

- Host module with all of the nuts and bolts: supplies power + coms to sensor
    - Coms to network, microcontroller for filtering
    - Pin mapping for various protocols
    - Current monitoring
    - Power converting from AC to DC at var voltage
- Unique to SWARM: pin mapping, failure detection; microcontroller connections, var voltage
    
      
    

![[Untitled 260.png]]

  

![[Untitled 261.png]]

Develop time

Determine sensor specs from our groups + beyond

![[Untitled 262.png]]

Current Leakage:

![[Untitled 263.png]]

  

Pin Mapping: digital programmable option (risk of failure), hardware, physical PCB connections (set at production)

  

Packaging: Titanium + silicone, epoxy? other

Connections: fixed cable (reduce failure, limits length)

  

![[Untitled 264.png]]

Q&A

- Encapsulation procedures? Smth like FSR can’t be put in a metal box , hopefully there is a solution
- Where does FDA approval begin?
    - Benchtop testing results will be available, share guidelines leading toward FDA
    - Here are pieces for your own work, own IDEs not open source
- What quality system to track everything
    - Have same approach across teams
- Open source, what if other Case people want to use the stuff? Is there a fee?
    - May be Synapse for manufacturing
    - Still figuring out these questions
    - Goal: make their own or buy from manufacturer
    - Stuff is not free, access to knowledge free
- Figure out what’s realistic, can’t support everything
- Upgrade or replacement for NNP?
    - Plugs in
    - Figuring out how to make it backwards compatible
    - Electrodes + connectors would be the same
- reconfigurable hardware? may be useful for benchtop, once it’s in a person the sensor configuration is mostly fixed
    - Mostly microcontrollers + supported electronics currently in modules

  

# 8-23 Sydney, Isabella, Harshita, Anish

## Sydney

Exoskeletons: current ones lack ability to recognize and react to falls

- Need data on force and acceleration of falls

Create a exo for fall tests

![[Untitled 265.png]]

Design: orthotic joints, lockable angles

- Machined and assembled parts, reduced weights as needed

5 fall scenarios : forwards, back, left, right, forward with CCW twist

Results

- Knee and backpack weight off
- Straight fall had higher acceleration than twist

Next steps: new knee joints, covers, rework hip attachment; more testing

Q&A

- how much does testing replicate humans falling? For now looking at does the device survive a fall, needs to mimic actual movement eventually; most work will be in simulation (trip + slips via treadmill belt); exo do cause unnatural fall pattern (locking joints)

  

## Predicting Stair Ascet with a Gait-Assist Neuroprosthesis

Stroke target: hemiparesis (weak muscles on one side)

Gait-assist device: surface stim + exo knee, sensors to assist with transitions

![[Untitled 266.png]]

![[Untitled 267.png]]

- Expand to stair states

Able bodied tests to get data on walking + stair walking patterns

Offline Algorithms

- Show IMU axes for whole gait cycle
- Look for thresholds when ascending stairs: gyro Z < -20, acc x < -100

![[Untitled 268.png]]

Fully planted feet = quiet stance

![[Untitled 269.png]]

- Very quick detection!

![[Untitled 270.png]]

Q&A

- IMUs x3: thigh, shank, unaffected leg: for this one just using unaffected leg
- Just finding first step onto step? What about continued climb?
- Step over step pattern (Able bodied) or bringing trailing limb to the same step? later, one leg detection
- Ultimate goal for generalized algo vs threshold for each person: did look at slope trends as well

  

## Harshita: Predicting Joint Angles from IMU Sensor Data

SCI, develop walking controller: predict angles using IMUs, use for outside lab setting

Knee, hip abduction, hip flexion

Only using acceleration in neural net

![[Untitled 271.png]]

Gold standard from Vicon markers

- Sync data 60 Hz vicon, 50 Hz IMU

![[Untitled 272.png]]

- Large errors with feed forward
- Switch to long short memory network: cyclic nature of joint angles

Optimizing network for data

- Modulating number of neurons + epoch?

Applying network to test data

- Optimizing again
- Could be overfitting: too specific to the training data, not flexible to new data

Added other joint angles + optimized for # of neurons

Q&A:

- How big of a data set needed for LSTM memory network? 80 seconds of walking or so
    - Could errors be reduced with a large data set?
    - What is the input? All IMU data? Using all of the IMU acc data
- Delay to output?
- Knee seems to track better: consider scaling data since knee and hip angles are different in magnitudes

  

## Anish: Summer Experience at ReLLiNC Lab

![[Untitled 273.png]]

Vicon: missing markers + trajectory gaps

- Clavicle, anterior pelvic markers (hand in front)

![[Untitled 274.png]]

IMU or FSR: FSRs easier to work with, looking for toe off and initial contact

![[Untitled 275.png]]

- IMU uses resultant vector

![[Untitled 276.png]]

  

Q&A:

- Only 6 used in algo, lower back not used
- Full IMU sensors

  

# 7-9-2022 Madi, James, Anna

## User Centric Design for Novel Prosthetics: Madi Person

Little research done on user feedback and perspective on surgery

Most work is on upper

![[Untitled 277.png]]

- Would want improvements to durability, comfort, functionality

![[Untitled 278.png]]

- Slider type questions

![[Untitled 279.png]]

  

Demographics

- Background, time and cause of amputation, prosthesis type and changes wanted (found myoelectric was more likely to want to undergo surgery), challenges and concerns

Sensory Feedback

- Explain what it is
- Surgery risks

User interface

- Demonstrate how it works
- Assess usability

Qualtrics: industry standard

### Smart Liner

Existing liners aren’t designed for diabetic amputees

![[Untitled 280.png]]

Q&A:

- Does initial placement of slider bar bias the answer?
    - Something to think about
    - Set it to neutral initially
- Do you get how long people spend on each question?
    - Not sure, but would be useful
- Use combination of negative and positive answer questions
- Feelings on user feedback
    - Valuable from a stats perspective to understand survey design
    - Interesting background factors that impact prosthesis use
- Smart liner?

  

## James

### Open Source Bionic Leg

### Wearable Energy Expenditure System

![[Untitled 281.png]]

Develop energy monitor usable outside lab to assess effect of SNP on energy expenditure for homegoing

Q&A

- Frequency of data collection? Storage available on RPi? Could preprogram Sd cards so participants coudl switch them out
- IMU? Adafruit LSM9BS1
- Algorithm that gets “metabolic” measures? Weights determined from separate paper
- Implementation challenges with having all these extra sensors and wires? Move to wireless IMUs
- HR? That alone has delays in responding to actual work done, lower limb kinematics alone seem more accurate

  

## Anna: Transcutaneous Spinal Cord Stim and Amputee Stair Ambulation

![[Untitled 282.png]]

- Alternating activity from a reflex

Benefits:

- SCI population
- Increase motor activity, reduce spasticity, reduce pain
- Optimizing for these benefits: gaps between bone
- Usually multidisciplinary approach with drugs (increase excitability), rehab, peripherial stim too, exo

Falls on stairs can be especially dangerous

- SNP has been shown to affect gait and reduce stair errors

![[Untitled 283.png]]

  

Q&A

- Foot orientation outcome measure? Traveling in a straight line forward, how much foot deviates from that forward direction
    - What about natural deviations in foot direction

## 7-12-2022 Lisa Lombardo MPT: SCI 101

![[Untitled 284.png]]

- Facts and figures site good for stats
- Most due to car accidents, secondly falls

![[Untitled 285.png]]

- Most left with some deficit

What happens to the body?

- Really on arms for mobility

Anatomy

![[Untitled 286.png]]

- Neck to lower backand on down
- Spinal cord: sends messages from brain and back
    - Voluntary and involuntary movement, sensation, autonomic nervous system

![[Untitled 287.png]]

- Higher SCI = more lost / altered movement sensation
- Cervical: tetraplegia, thoracic or lower may only paralyze legs + lower trunk: paraplegia

![[Untitled 288.png]]

![[Untitled 289.png]]

- Anatomy can help understand what participants present with

![[Untitled 290.png]]

![[Untitled 291.png]]

- Upper: descending track hurt
    - Still has spinal reflexes below site
    - Spasms, Babinski response (reflex), relative preservation of muscle bulk — still responds to stim
- Lower: “damaging a peripheral nerve”
    - Decreased muscle tone, muscle atrophy, weakness or paralysis, absent or reduced reflexes

![[Untitled 292.png]]

- Middle: could walk perhaps but bad upper extremity control

  

Diagnosis

- American Spinal Injury Association: standard system to classify SCI, predict level of function
- AIS: ASIA impairment scale, most caudal level (lowest) with normal function sensory + motor
    - Understand what the scores mean is most important
- Sensory: touch + pin prick while supine, compare with check feel
    - Found for left and right, touch + pinprick

![[Untitled 293.png]]

- 1 could be less or more sensation
- Motor: key muscle groups
    
    ![[Untitled 294.png]]
    

![[Untitled 295.png]]

![[Untitled 296.png]]

- also S4-5 anal assessment for both sensation and motor

![[Untitled 297.png]]

- Correction: NO = B, YES = C or D

![[Untitled 298.png]]

- A = nothing at all below injury
- B = sensory incomplete (no motor)
- C = motor incomplete
    - Movement but not super strong

![[Untitled 299.png]]

![[Untitled 300.png]]

- D: fairly good strength below injury

![[Untitled 301.png]]

Spasticity: exaggeration of normal reflexes

- Lack of inhibitory signals
- Good or bad: can trigger purposefully for movement or support
- If change from normal see a doc!!
- Treatment: stretch, heat or ice, therapy, stim, medications
    - May exhaust muscles but also improving muscle strength..

Circulatory

- BP low or irregular, faster or slower HB, larger vessels, blood return to heart is worse
- Swelling, edema, blood clots (abnormal swelling), fainting (low BP sitting up), impaired temp control
- Treatment: compression, sitting tolerance, tilt table, medications to affect BP / HR

Cardiovascular

- Vagus nerve intact - cranial nerve
- Sympathetic innervation of heart from T1-T5: T6 injury and above can affect autonomic system, normal parasympathetic and heighted or reduced sympathetic
- Lower exercise capacity: loss of exercise pressor reflex, llower HR, BP
- Possible complications
    - Orthostatic hypotension: decreased BP
        - Signs/symptoms: pale, blank stare, dizzy, foggy feeling
        - Treatment: abdominal binder, wraps, supine to sitting slowly

Autonomic Nervous System

- Controls functions of organs + glands automatically all the time
- Sympathetic: energy for sudden results (fight, flight, fear); increase BP, HR, pupil size
- Para: slows body
- SCI prevents regulation of ANS: lower parasympathetic, some part of sympathetic (entire system in tetraplegic)
- Autonomic Dysrefexia
    
    - noxious stim below injury level: may not feel it but response occurs
    - Pain = flight or fight, tempered by parasympathetic response but that only reaches areas above injury
    - Increase BP, decrease HR
    
    ![[Untitled 302.png]]
    

![[Untitled 303.png]]

- Symptoms: redness, headache, chills, tired, blurred vision
- Treatment (Sit up + seek cause): sit up , find cause, call 222 med team, educate patient
    - unresolved 15-20 mins go to ER

Breathing

- Diaphragm, chest muscles
- Can lead to pneumonia

Skin

![[Untitled 304.png]]

- Can’t sweat below level of injury
- Pressure sores: can be worse below
- Shearing
- Allow subjects to weight shift and relieve pressure

Bowel Function

- Regular schedule to keep

Lower bone density

- Carefully moving, prevent fractures
- Heterotropic ossification: bone growth in abnormal areas
    - Decreased range of motion

Research Considerations

![[Untitled 305.png]]

- Experimental set-up: just testing vs collecting data to be reported
- Make sure to get demographics! **calibration into for vicon**

![[Untitled 306.png]]

- What you’re collecting and WHY: developing a controller, what it’s contributing to

  

Q&A:

- New brace setup: try for 15 mins + do a skin check
    - Don’t put more padding lol

  

## 6-28-2022 Daekyoo Kim: Restored plantar sensations in individuals with lower-limb loss improves gait symmetry and motor adaptation

August 17th Musculoskeletal Research Symposium

Challenges of Lower Limb Loss

- Balance deficits + abnormal gait
- Prosthetic limb: less push off, longer stance time, shorter step length, asymmetric step pattern
- Reliance on intact limb, less confidence, more energy to walk, increased fall risk, less mobility

Sensory Neuroprosthesis: restored plantar sensation

Hypotheses

- Increased gait symmetry + stability

Methods

- 4 amputees, 6 able bodied
- Location mapping
- Vgait: force instrumented split belt
    - Wore own shoes, googles to avoid looking down, white noise in headphones
- E1: walk 0.5m/s for 2 mins
    - Gait symmetry: step lengths of both legs
        
        - Normalized by COM and stride length
        - COP marker for step length: 100% = symmetrical, > 100 prosthetic is longer
            - Clinical, functional relevance? Overusing hip and knee, bone issues, fall related injuries, osteoarthritis
            - At what point do these effects happen?
        - Statistically significant changes, clincically? not sure
        
        ![[Untitled 307.png]]
        
        ![[Untitled 308.png]]
        
    - Ground reaction forces
        
        ![[Untitled 309.png]]
        
        - Tend to load vertically without SNP, now pushing from side to side like able bodied
        - How will foot design need to change? will need to change
        - Force impulse = area under curve
    - Whole Body angular momentum
        
        - Sagittal plane: rotating backward and forward movement
        
        ![[Untitled 310.png]]
        
        ![[Untitled 311.png]]
        
        - Can be calculated from markers or GRF
        - _suggests improvement in gait stability_
- E2: speed matching (10 mins), split belt walking (10), speed match (10)
    
    - Hypth: Perception of prosthetic limb will be retained
    - can it be retained?
        
        ![[Untitled 312.png]]
        
    - updating movement in our internal model
    - Amputees have mismatch betwixt perceived and actual speed
    
    ![[Untitled 313.png]]
    
    - Experiment setup
        
        - 13 different speeds randomized: judge speed relative speed of each leg to the other
        - Is the speed the same or different
        
        ![[Untitled 314.png]]
        
        - Adaptation: intact leg belt 0.5, prosthetic limb 1 m/s
    - Outcome measures:
    
    ![[Untitled 315.png]]
    
- Results of E2
    
    - Sig effect of SNP
    - SNP off: push off from treadmill belt was less
    
    ![[Untitled 316.png]]
    
    - W/o SNP for same belt speed, said speeds were not the same - altered perception of prosthetic limb
    
    ![[Untitled 317.png]]
    
    - Adaptation
        - During initial adaptation, no effect of SNP
        - Subjs w/ SNP adapted to split belt perturbation at similar rate to controls
    
    ![[Untitled 318.png]]
    
    - After split belt walking
        - All subjs show one leg perceived as faster, evidence of learning
        - Originally symmetry returns
    
    ![[Untitled 319.png]]
    
    ![[Untitled 320.png]]
    
    - Perceived symmetry response: show adaptation to split belt perturbation
        - Initially they get it wrong, think everything is the same even though it is not
        - Perceive the difference correct after adaptation
        - COP results alone doesn’t reveal anything perception of leg

  

  

Reduced perception difference betwixt legs

Adapted to split belt walking w/ use of SNP

With gait training may not be able to change stepping pattern, but can change timing of symmetry

COP velocity can tell about balance and show things not shown in COP alone

![[Untitled 321.png]]

  

RT: keep scales of y-axis more consistent

- Compelling novel results
- Tie it back to clinical implications when presenting
- Error bars on plots are good
- **Need to indicate statistical differences and then clinically**

Stephanie: explain what people expect to see

- Mini conclusions along the way

  

Q&A

- Would results be worse for subjs with worse overground walking performance
- Dr. Hardin: tuning prosthetic foot to get same results theoretically
    - If three subjs with limb loss have 3 different feet: may need to explain that factor

## 6-14-2022 Current trends in robotic Assistive wheeled mobility

Intro

- Power wheel chairs provide mobility, comfort, indep BUT challenges of steering, outdoor use, barriers
- Uneven surfaces, curbs
- Smart wheelchairs: smart obstacle recognition + navigation: large potential benefit but little transfer from research to market
    - Ultrasound sensors used not great for outdoors, cost
    - Wheelchair limitations: flat enviornments

Goals

- Trends in RW, standardize reqs, propose evaluation tools to compare effectiveness

![[Untitled 322.png]]

Taxonomy

![[Untitled 323.png]]

- Standard on top
- User-RW: computer interface of it

![[Untitled 324.png]]

Lit Review

- 111 adapted from normal, 21 novel PW

![[Untitled 325.png]]

- 1-2: basic user testing in lab

![[Untitled 326.png]]

- Most in basic science stage: feedback from wheelchair users

  

![[Untitled 327.png]]

- Most tested in indoor environments, some outdoor simulated
- Shared control of user + robotic device

![[Untitled 328.png]]

Example: MEBot

- User need: create prototype, focus group to see if device meets needs
- Continue testing + prototyping, iteration

![[Untitled 329.png]]

Translate taxonomy factors to user needs:

- maneuverability —> wheelchair dimensions

MEBot: 6 independent wheels

![[Untitled 330.png]]

Focus on self-leveling feature

- Survey: what features would you used? most said self-leveling, curb climbing, traction control
- Formed initial list w/ help of wheelchair users in research team

Evaluation

- Engineering: lab testing for safety + ISO standards, 113kg dummy or single user
    - Static + dynamic stability: tipping point and stability while driving/braking
    - Dimensions
- Usability: experienced users, satisfaction, comfort, ease of use
    - Effectiveness: measure completed tasks
    - Efficiency: self-leveling time, seat angle deviation
    - Satisfaction: QUEST, System usability scale

![[Untitled 331.png]]

![[Untitled 332.png]]

- MEBot 2.0: all completed

Results

- Generally lower angles (pitch and roll) and less variation
- Faster reaction time
- No sig dif but that means MEBot is as good as their current PW

![[Untitled 333.png]]

![[Untitled 334.png]]

  

Limitations

- Haven’t tested outdoors TRL-5
- Not really a gold standard, just comparing to normal PW not commercial ones that can handle more difficult terrain
- Small sample size: may be impossible to find sig
- Qualitative vs Quantitative: feedback from users vs statistical sig

  

![[Untitled 335.png]]

  

Q&A:

- usable by those with impaired fine motor control
    - Are there levels of automation
- At MVP stage not commercial product but any idea how cost compares
- Slow reaction time? software or mech
    - Hydraulic is a bit faster
    - Some limitations on torques on actuators
    - User: driving too fast
- What makes it robotic? automation level
    - Anything from self-driving car sphere
    - Committee on self driving cars
- Technology Readiness Levels?
    - NASA TRLs
- What would it take for MEBot to be picked up by a large manufacturer
    

## 5-31-2022 Suzhou Li Does electrically elicited sensation modulate spinal circuitry?

Intro

- 50% of lower limb amputees fall, reduction ADL
- plantar sensation contributes to H-reflex

H-Reflex

- Sensory fibers to central, out to motor fibers to muscle
- Latency from stim to muscle 30-40ms
- M-wave: direct stim of muscle 2-10ms

EMG waveform

![[Untitled 336.png]]

  

Modulation of H-wave

- pre synaptic: sensory fibers gate inputs into reflex
- post synaptic: changes excitability of motor fibers

Cutaneous Afferent Effect

- Second pulse lowers amplitude of H-wave
- cutaneous stim modulates reciprocal inhibition ^

![[Untitled 337.png]]

- Increase interval between green and blue
- Functional effect?

  

![[Untitled 338.png]]

- Foot sole stimulation modulated H-reflex

  

Sensory Neuroprosthesis: high density nerve cuffs, electrical stim, modulate intensity + location

- How is this stim integrated within CNS + sensorimotor control

![[Untitled 339.png]]

  

Experiment Design

![[Untitled 340.png]]

![[Untitled 341.png]]

- Posture changes sensory fibers, may also direct effect on CNS
- Visual feedback on loading as % of body weight

H-wave

Principal Component analysis + clustering

- normalized on trial by trial basis
- Just trying to separate H-wave by morphology not amplitude
- finds dimension in data that accounts for most variability: what separates it most
- PCA: rotate a cube, angle where data lines up = dimension

Results: fixed stim and range of stim levels

- FS: reduciton in occurance of H wave with SNP
- Range of stim: reduced with 30% but not 70%
- **Modulation depends on loading of prosthetic limb:** other modulation inputs
    - significance?
    - Same pattern present in able bodied lit? effect occurs on H reflex amp
    - indicative that the CNS is listening to the SNP: stim being processed + integrated with other sensory inputs
    - Whether that reflex is beneficial or detrimental
    - Between 30 and 70?? Need to look into it

How is H reflex amplitude affected by plantar sensation

- M wave amp different betwixt loading %
- historically a measure of stim strength: how many fibers recruited
- H-wave: one session had sig SNP dif in 30, the other 80
    - T test
- Over range of stim levels: no sig dif bewixt max M waves of loading + EPS conditions
- Same for H-wave
- But do H and M wave maxes occur at the same place relative to each other

Conclusion

- No sig effect of elec elicited plantar sens on H-reflex amp
- But it does modulate occurrence of H wave
- Effect depends on sensory input from residual and intact limb

![[Untitled 342.png]]

Questions

- subject posture effect on H-wave? has an effect, trying to mimic gait stages to potentially extrapolate to functional applications in walking reflexes
- Loading: includes sensation from joints, knees, visual
- loading AND posture as variables technically: may not be worth instrumented all these factors
    - Ideally isolate just loading but that’s not practical
    - loading is the biggest difference

Conclusion:

- What does it mean
- functional implications? just electrically interesting
- add interpretation: what’s the story, plantar sensation being integrated into CNS
- _**Here’s what the data says, interpret what it means**_
- Other relevant groupings in PCA?
    - There were other groupings but had very different amplitudes
    - Concluding that the subset was not coming from same reflex pathway as the primary cluster

## 5-3-22 Aarika Sheehan lower extremity anatomy

I have uploaded the video recording + slides from Aarika's presentation today. For those of you who have missed it, it was a condensed and very informative lecture on lower limb anatomy. Here is how you can access the files:

On R drive, go to :

Triolo_lab\database\lab_meeting_presentations

If you have access to ReLLiNC platforms, you can get the files from the following directories too:

R Drive: 01.Study Folder\Triolo 1583890 Rellinc\Posters_and_presentations\MSL presentations

VA Teams: under Rellinc Teams: General\presentations\MSL presentations

Case Teams: Presentations-publications\presentations\MSL presentations

  

Muscle lengths affect strength + range of motion

Hamstring muscles

![[Untitled 343.png]]

- hip extension
- Majority innervated by tibia portion of sciatic
- biceps femoris - fibula portion
- Muscle characteristics for EMG
- BF, ST, SM (most medial, on inside)
    - ST and SM insert on medial part of tibia

![[Untitled 344.png]]

  

  

adduction: move toward midline of body - medial compartment

![[Untitled 345.png]]

[](https://www.notion.soundefined)

OE - originates near OF

obturator nerve passes through here

![[Untitled 346.png]]

Adductor muscles originate in same areas

AM:

- AD: rotate hip out
- H: rotate hip in
- Stablization for balance or ambulation

![[Untitled 347.png]]

Gracilis - weakest

![[Untitled 348.png]]

Femoral nerve

Sartorius

![[Untitled 349.png]]

- Crosses hip + knee joint

  

![[Untitled 350.png]]

psoas minor: 60% have them

Tightness in muscles in this region can affect all the way down the leg

Illiacus: femoral nerve

![[Untitled 351.png]]

One spans two joints: RF, affects hip + knee

VI: under RF

![[Untitled 352.png]]

Hip flexors tend to get weaker as you get older

- Watch torso as you sit and raise leg: lean back so gravity will help
- Have to direct to use the muscles you’re targeting

  

![[Untitled 353.png]]

Femoral: anterior compartment,, front of thigh

Obturator: medial compartment, adductors

Sciatic (back of leg): hamstrings

  

  

![[Untitled 354.png]]

Four compartments instead of three in thigh

Bones to know attachment points

![[Untitled 355.png]]

Tibia: 90% of weight bearing

![[Untitled 356.png]]

Dorsiflexion: foot up

Damage to this nerve: foot drop, trouble clearing foot when walking

Hallucis: people can trip on their toes if this is messed up

![[Untitled 357.png]]

Ankle dorsiflexion + inversion (ankle out to the side)

  

  

  

![[Untitled 358.png]]

G: lateral and medial head

  

![[Untitled 359.png]]

Toe off during gait cycle

![[Untitled 360.png]]

P: internally rotates knee joint to lock it

  

![[Untitled 361.png]]

![[Untitled 362.png]]

![[Untitled 363.png]]

Surface stimulation

- use specific movements to target muscles

Recording electrodes: minimize cross talk from other muscles

  

### 3-8-2022 Sandra Hnat “Suggestions for Writing User Friendly Code”

Why

- Help with debugging
- Saves time in long run
- Good team member, they don’t have to rewrite code
- Someone asks about something you did months ago
- Pick up on project
- Contribute to science w/ open source!

Anti-motivations

- Deadlines, might not be fun
- Not a priority, project started exploratory

Goals when writing new code

- Give it someone else w/ minimal to no explanation
- Ideally one button push from raw data to results
- If possible, translate to a generic tool to be reusable

Start with an outline:

- Define ultimate goal: final results (ex tune a fancy controller to track knee angle)
    - Set up things to be as lazy as possible, helps if you need to collect more data
- Intermediary steps: pipeline, modular way
- **Never modify raw data:** determine reasonable starting point, makes results reproducible

![[Untitled 364.png]]

![[Untitled 365.png]]

Multiple subjects? Batch post-process in for loop and save as new file if post-proc takes a while

Example: estimate COM w/ accelerometers

![[Untitled 366.png]]

Organize File Folders + File Naming Convention

- Separate raw + processed + subjects (think about for loop processing, dates may not work)

![[Untitled 367.png]]

![[Untitled 368.png]]

![[Untitled 369.png]]

ReadMe

- Overview of project
- List of dependencies (toolboxes, versions)
- filenames + descriptions
- instructions for pipeline
- experimental protocol
- Could make a data read me too

![[Untitled 370.png]]

![[Untitled 371.png]]

Documenting with Code

- Top of each script / function: purpose, inputs/outputs

![[Untitled 372.png]]

- Break code into sections

Clear Variable Names lol

avoid hardcoding numbers n equation

Avoid copy pasting code!!!!!

- Do subplots in a or loop!

Git Repos?

Update status to command window

Come up with test data

- Use limited or fake data set with known outcome
- Include in public code
- Ex standing knee angle, one cycle

Write error flags for others!

![[Untitled 373.png]]

Repos

- Track changes, fosters collab, forces documentation, reproducibility + transparency
- Don’t back up data!

  

[[Screenshot (Nov 15, 2022 09-11-24)]]