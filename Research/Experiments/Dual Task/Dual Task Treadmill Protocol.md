# Purpose

To investigate the effect of the SNP on the cognitive load required during gait.

The dual task paradigm centers on the concept that gait involves high level cognition, specifically executive function and attention. With limited resources, a person concurrently executing a motor and cognitive task may demonstrate a measurable performance degradation in one or both tasks. This methodology has been applied to study neurological diseases in Alzheimer’s and Parkinson’s populations. With lower-limb amputees, qualitative reports indicate they devote more focus to walking suggesting a higher cognitive load. A handful of studies have investigated amputee populations and found significant gait changes during dual tasking compared to able-bodied participants. We will assess dual task performance in lower-limb amputees with and without elicited plantar sensation to investigate how restored sensation may affect the cognitive load during walking. Our pilot study will consist of self-paced treadmill walking and a two cognitive Stroop tests (visual and auditory)

# Materials

VGait system

Vicon motion capture: configuration CamsDigitalFPs (verity DFLOW config has direct FP data input)

# Methods

## Outcome Measures

Visual Stroop: number of correct responses in 30 seconds

Auditory Stroop: number of correct responses in 30 seconds

Gait Parameters: velocity + spatial/temporal metrics

- Gait velocity
- Stride length / width
- Cadence
- Symmetry:
    - Step length
    - Stance time
    - Single and double limb support time
- COM angular velocity ?
- Joint kinematics: knee and hip angles
- Work done from COM

## Tasks

During all tasks the visual field will show an endless road scene that moves at the participants current speed. For both stroop tests the participant will be instructed to “Answer as quickly and as accurately as possible”

### Visual Stroop (VStroop)

VStroop consists of displaying words of colors with congruent or incongruent font colors.

Participants are tasked with identifying the font color of the words.

![[Diagram.drawio.svg]]

### Auditory Stroop (AStroop)

AStroop consists of recordings of the words “high” and “low” delivered in congruent or incongruent pitches.

Participants are tasked with identifying the pitch of the words.

### Self-paced Treadmill Walking

The subject will walk using a self paced treadmill for 30 seconds. During this time the screen area where the stroop tests would be administered will display a cross in the center of the screen as a focus point.

![[Untitled 605.png]]

![[Untitled 606.png]]

## Experimental Setup

![[Diagram.drawio 1.svg]]

The dual task experiment will be conducted in blocks of trials where SNP is _ON_ or _OFF_ for the entire experiment session. All the blocks with the same SNP condition will be performed together to allow time for the subjects to adapt to and utilize the resulting sensory feedback in the SNP _ON_ condition.

Within each SNP trial block there are 20 trials. First, VStroop and AStroop will be assessed while the subject is standing. The next 18 trials consist of the following three conditions: walking, walking while performing VStroop, and walking while performing AStroop. Each condition will be assessed six times per block and presented in random order. After these trials, there is a break before the start of the next trial block.

  

  

### Experiment Details

[[Experiment Checklists]]

1. Setup
    1. Marker placement: plug-in-gait full body model (minus arms), 27 markers
    2. **Subject measurements:** height, knee/ankle widths, weight (can calculate from force data) [mm and kg]
    3. **Take static trial**
2. Introduce Treadmill Walking: introduce control of the self-paced treadmill, walk as normal
    1. Vicon self-paced via 4 pelvis markers
    2. Determine a subjects preferred walking speed by performing the following 3x
        1. Increase the treadmill speed from 0 till the subject is comfortable
        2. Decrease the treadmill speed from maximum till the subject is comfortable
    3. Bring the treadmill up to the subject’s preferred speed and then activate the self paced mode
3. **Walk for 5 minutes of baseline w/ Vicon + DFlow recording: self paced and fixed**
4. Introduce cognitive tasks
    1. Explain and calibrate VStroop task
        1. Determine interstimulus duration by running through trials (10-15 seconds each) with stimulus at the following intervals (seconds)
            - 1 s interval —> 30 stim
            - 1.5 —> 20 stim
            - 2 —> 15 stim
        2. Increment and decrement in interval to arrive at a condition that is challenging for the subject without being impossible
        3. For the actual trials utilize a slightly shorter interval: i.e. subject preferred interval is 1.2, perform experiment with 1 or 1.1
5. **Perform standing and VStroop single task: 30 seconds**
6. **Perform SNP trial blocks for ON or OFF condition: record video of trial blocks**
    1. Goal is not a perfect score
    
    3. ~~Single Task Cognitive trials: no Vicon data needed~~
        1. ~~Standing and VStroop~~
        2. ~~Standing and AStroop~~
    4. ~~Single Task Motor and Dual Task trials: randomized~~
        1. ~~Walking x10~~
        2. ~~Walking and VStroop x10~~
        3. ~~Walking and AStroop x6~~
7. Break

# Data Processing

Vicon: Plug-in-gait full body in Visual3D

Dflow: R Studio

# Data Analysis

Compare performance between

- Single tasks and DT Without SNP
- Single tasks and DT With SNP
- DT Without SNP and DT With SNP

  

Significant reduction in performance ST vs DT Without SNP indicating cognitive-motor interference

Significant improvement in performance from DT Without to DT With SNP indicating SNP reduces cognitive load of gait

May find no significant difference between SNP conditions

- No interference OR cognitive or motor task may not be complex enough

May find no significant difference between ST and DT conditions

- Cognitive or motor task may not be complex enough to cause interference