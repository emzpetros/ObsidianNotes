  

  

  

# 8/30/23

MS, AS, JJ taking over Alexandra’s duties

Students will start taking minutes again in rotation to communicate with clinical team

- Esp as we do scheduling with the subjects ourselves

Scheduling

- LE01 maybe 11th
- LE02: Tuesday Hannah, Eileen, Mau or John (finish before 2:30), 5th
    - Develop a plan
- LE04: MS will up on Sept dates, stair data, Hannah, Mau, Eileen (?)
    - May not see him for a couple months after Oct
- LE06: 13th? ask about dark room

Stairs: heel markers may be blocked by treadmill rails, bad cameras, spotters

Restarting journal club Suzhou : at least once a month

Can practice presentations at ReLLiNC meeting: students let Hamid know

Update to jewelry box

- maybe use extreme sizes for demo
- Upper may need subj without connector between C-FINE and perc to reduce bulk over joint crossing

  

  

# 8/17/23

  

General

- LE07 surgery pushed back to ??
- Dod updates for Dakota : high levels, design/collect, reason, outcomes
- Website!!

John S: knows about UECU block compatibility

- 164 on cart

LE04 - Monday

- Wed: Suzhou, Eileen, maybe Lindsey
- Thursday: Hannah, maybe Aarika, SVV

LE02 28th

- Hannah, stairs, SVV?

Maybe LE06 wed 23?

LE01: 29th or 31st, Hannah + SVV

# 8/3/23

BC talk on Monday

- No exp with LE01

Website content : [https://docs.google.com/document/d/1tlIg9SQl8B3KKIpvIr6mX0EILpo71gkBAYnFpNVvLqo/edit](https://docs.google.com/document/d/1tlIg9SQl8B3KKIpvIr6mX0EILpo71gkBAYnFpNVvLqo/edit)

  

September RESTORE update, august for transfemoral update

- Blurbs soon

  

LE06 Wed: lindsey, me SVV, Aarika stairs

# 7/20/23

General

- DoD reports coming due soon: high level + understandable, sig, why + where we’re going
- Cleveland NeuroDesign Neurotech Entrepreneurs Workshop in September: STEM + disability outreach
- Intern poster session next Fri

Multimedia

- Website: maybe Trainee videos
- PwrPt templates

Scheduling

- Bree coming Mon Aug 7th

  

# 7/6/23

Updates

- Draft of the chronic stability paper
- Setting up a meeting with Daekyoo
- Added another metric to analysis
- VR equipment came in!

  

General

- Spend anytime, July 15
- Close lab door

  

APT Site Visit 7/13 1-3pm

- Clean Monday morning
- LE06 APL, LE03 ReLLiNC, MSL already has SCI or another subj
- 1:30 for 15 mins
- Hannah LE02, Suzhou LE02 tradmill perturb ( done by 12-1230), JW, L
- LE06 start with Aarika (2 hrs, best case 1.25-1.5), LH, Eileen afternoon, maybe Suzhou

  

Open Source Leg

- U of Michigan: Elliot Rouse?
- Open source, powered prosthetic : common hardware for comparison
- 30 +- plantar and dorsioflexion

  

Hardware

- Knee + ankle are identical
- Challenges: misisng fasteners, newer device, belt tensioning hardware - pulley adjusts tension based on subj weight + needed torque (speciality hardware needed), tolerance issues from anodization
- Configs: RL, LF; knee vs ankle only

![[Untitled 445.png]]

- T-motor AK80 actuators: IMUs, motor + electrical encoder, temp sensor, Plan GUI

![[Untitled 446.png]]

![[Untitled 447.png]]

Control Systems

- 5 Hz high level algo control for next step, 200 Hz impedance control - regulate energy in or out, > 1000 Hz position signal and bandwidth test
- Low level: regulate feedback loops
    - Step + bandwidth response tests to see how well t tracks target metrics
- mid-level: how should device respond in an activity, walking or standing
    - Impedance control: virtual spring / damper / equilibrium position
- high-level: headless rasp pi, predictive algo to switch state

  

GTech used it for adaptive walking speed: ML indp of user to predict walking speed for gait recognition

RR Posh Finite-State Imp + Direct myoelectirc control

- Autonomous + user input control : surface EMG
- “volatile” terminology : maybe from user isn’t best definition, even IMUs technically read input from user’s muscles + nerves

  

Would like to move beyond simple thresholds

Not keen on environmental classification of direct walking to stairs: you stop first, why detect change in state while walking if you’re going to stop first

- Could have direct user control of state change

Combining direct + finite states

Modulating sensitivity + control parameters of commerical devices that are out there: tune gains using EMG data

  

Can you add an external sensor to the control, maybe targeting mid level control instead of another finite state

  

Assumption that finite state machine is perfect, emg would tweak the params ; may not to rely all on FSM of IMUs

- We can instrument EMGs not related to joint control as well: hip on either side can be informative

# 6/22/23

Subjects

- LE02: 7/22
- LE07: surgery after 7/18

Treadmill training 6/28 noon

July 13th APT visit

take off batteries

Book PCs on calendar

  

Cable with 8 channel connector for canon connector or surface EMG

  

IRB: close on able bodied

  

Scheduling:

  

# 6/8/23

Updates

- Qual passed, Hannah T32 Neural Engineering, new lab members (Mau - EMG module, Anish - Open Source leg, Jessica - regulatory)
- Purchases: Safe gait, speckle imaging, Delsys, Vive, moticon sensors, electrodes
- UECU / ASCU:
    - 151 tentatively fixed
    - 3rd one in the works, Will have 3 w/ 2 perc board each
    - New EMG board in ASCU housing
- Bertec treadmill 27th June

  

Subjects

- LE01: week of 19?
- LE02 17th: Suzhou, me, John
- Le06: next wed, visitors at VA (1 hr)
- LE07:

  

Work on papers

# 5/24

Updates

- OPTech Conf: ECT prosthesis - passive pros. with active components when needed, hybrid type
- Elliot Roahse? Open source leg
- Two summer interns: Mao (EMG board) + Anish (open source leg)
- Jessica Jervela: regulatory expert starts June
- Meetings moved to Thursday 1
- Purchasing: 29k to spend
    - No treadmill for now :(
- Minnesota events next year
- Dirty linen bin in lab now to use

  

Subjs

- LE01 - cyst in residual
- LE02: June 17

  

Genium

- Outputs data to perc board giving stim values, need to verify output values are appropriate

  

Really need to do data analysis!!

# 5/4 NER Recap

Posters

- Injectable Wireless Neuromuscular Microstimulators: A. Ivorra, Barcelona Spain (UPF group)
    - 2 A stim!
- Open Source Leg
- Sensory feedback after SCI: rats, augmentation to help with motor response
    - Ahensei , Texas A&M

  

People

- Daniel Ferris, Nicol Stafford: open source leg
- Mohsen Rakhshan: memory task, with auditory words + remember if current word matches N word before
    - Look for publication
- Warren’s Lab: Eric Musselman, Daniel Marshall
    - Open source toolkit for PN
    - Princess Tara - technician for toolkit
- Eugen Romulus Lontis: EEG, Denmark
    - For future could be useful to look at papers
    - Spinal cord stim for pain + phantom pain with EEG
- Luke Osborn:

  

Me

- Celia Fernandez Brillet: vestibular DT, saw in crease in dual task speed
- Prof Thomas Stieglitz: uneven terrain, delayed vision input for amputees + dual task
- Possible DT Ideas
    
    - Audio task: functional relevance of tracking voices + picking out background noise
    - Uneven terrain: someone at SFN did it , manually put block on
        - Treadmill version of gravel walking
        - Some kind of EEG collection method to reduce noise from walking
    
    ![[Untitled 448.png]]
    
    - Stim drop out

  

Split belt loocomotor adaptation , EEG

- Neurological adaptation happens slower than behavioral

  

Look at

- [https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0278646](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0278646)
- [https://faculty.eng.ufl.edu/human-neuromechanics-laboratory/people/](https://faculty.eng.ufl.edu/human-neuromechanics-laboratory/people/)
- [https://scholar.google.com/citations?view_op=view_citation&hl=en&user=zjJ4V0UAAAAJ&sortby=pubdate&citation_for_view=zjJ4V0UAAAAJ:F9fV5C73w3QC](https://scholar.google.com/citations?view_op=view_citation&hl=en&user=zjJ4V0UAAAAJ&sortby=pubdate&citation_for_view=zjJ4V0UAAAAJ:F9fV5C73w3QC)

# 4/12

NER

- Flights + all should be covered
- Maybe check in with sedona about workshops
- Bree Christie will be there!

LE02: Hannah (1.5), Lindsey , try and do CWM first then perturb, John

LE04: lindsey, Hannah, me

LE01 back 25th: next couple days, Hannah + john

Special Funding Requests via VA: due tommorrow

- Formal purchasing through VA, need PO or smth, no credit card ordering

  

DoD quarterly reports: blurbs to Hamid + Dakota , next week Tuesday

  

# 3-15

Updates

- LE02 showing same findings as LE01 in terms of reaction time results
- Working on gait analysis
- New exp with Dr. Shaikh
- Paper comments
- Working with Sean Li
- Working on NER poster

  

General News

- Reimbursement
- Should join IEEE
- New treadmill June - July

Scheduling

- LE01 Tuesday or Thursday next week 21 + 23: Hannah + John wright only
- LE02: start at 9 hannah, 2.5 , 2.5 lindsey
    - 1.5 Suzhou, 1.5 me
    - 9-1030, 1030-1; 1-2 lunch; 2-330 eileen, 330-530 suzhou
    - Take pictures for posters and such!!
        - Setup is visible: what’s attached to subject
        - May need to develop illustration
    - 15th for next visit?
- LE04 coming in less than 2 weeks:
    - Hannah go first, biodex, Eileen APL Day 1
    - Day 2 Eileen swap with Suzhou
- LE06 Wed 22
    - interview
    - Suzhou SNP off first PWS
    - SNP on walking, with trips
    - Thresholds
    - I’ll get next session
- S09
    - Neurology examination
    - Neuropathy progresses over time, connect that with system performance: baseline nerve conduction reading, troubleshoot any issues as nerve changes specifically
    - Typically done to detect neuropathy but is it specific enough to tell us info we want to know
- Possible diabetic candidate coming in

  

Suzhou Presentation

- Setup
    - 800 ms of perturbation
    - Stride time 1.1s, 1100ms
    - Perturbation doesn’t affect next step
- Ankle angle range for each stride
    - Consistent within session but not consistent even within the same day
- WB COM
    
    ![[Untitled 449.png]]
    
    - SNP decreases speed of sway towards right side during perturbation
    - Velocity slipping back on left side
    - WB COM vertical range during perturbation: may have dipped down more during perturbation
        - Increase of range but decrease in velocity the COM dropped downward
- Angular momentum about x and y axis during perturbation: SNP increased it during right side (x axis)
- y -axis: baseline off and on but not during pert
- Trunk angle
    - forward and backward: left and right have sig difference during pert with SNP off
    - Left and right: Dif in L + R by SNP
    - SNP leading toward better symmetry ?
- What does it mean in terms of stability
    - Decreased amount of sway indicating better stability
    - Need a technical definition for stability , vs just moving more or moving less
    - Butterfly patterns
    - Movement of COM gives you an idea of energetics and kinetics
    - Think of values as vectors vs scalers: is it moving in the direction it needs to move to keep stable
- Compare to able bodied data?
- Margins of stability: COM and COM velcoity, projects where COM will be in next step and compares that with base of stabiltiy (where foot is) to see how close the COM approaches boundary of stability (closer is more unstable)
- Recovery measures?
- Vertical ground rxn force on recovery step and stride
    - Breaking force (horizontal force)
    - No effect on either
- Right side vs left side perturbations are different but not a lot of SNP differences
- Maybe they’re not falling enough, not falling with whole body
    - Would want to see LE06 data , improved sense of body / foot position may improve it
- 3 m.s^2 limit in APL

# 3-1

Updates

- Processing gait data from new stroop experiment
    - Rxn time + speed analysis were promising, NER
- Met with Sean Li to have him work on VR project
- Meeting with Dr. Shaikh tmrw

  

General

- Linkedin post about Aarika’s PT conference: good interest
    - PT’s love free stuff, bring more stuff next time

  

Subjects

- LE01: next monday, wed, or fri
- LE02: March 18, April 1
- LE06:
    - Add IMU or sensor to detect knee movement on current prosthesis
    - Or use genium prosthesis + read sensors
    - Data cannot be pooled with transtibial data
    - May have to make cognitive a little less challenging
    - Wheelchair games starting soon possibly?
    - Check EMG, Suzhou, SNP testing, JW if time; next time DT

  

Screening

- SL-09: no TIMS
    - Were tims for us with better EMG access vs him using a motorized prosthesis one day
        - 2 cuffs smaller perc site

# 2/15

Updates

- New stroop exp
- NER submission: 21st
- Waiting on activation of our vicon license

  

General

- We have funding
- Student screening next friday
- Stair wheels coming in
- New treadmill meeting happening soon for MSL
- Aarika going to large PT conference
- Get anything you need from Daekyoo

  

Subjects

- Maybe LE01, week of 27th: Monday
- LE02: 25th , Hannah Eileen Suzhou
    - Coordinate with Suzhou for on / off order
- LE04: will discuss later
- LE06: 22nd 9a-2p
    - Reducing phantom pain meds or taking 10-10
- LE04: 27-29 march
    - + 2 screening candidates
    - Note availability + exp + where it is

  

Screening

- S0-9 screening tmrw: 2 cuffs and 2 tims?
    - Don’t have to use IM electrodes, could be useful to see how sensory motor integration works in diabetic pop

  

  

  

  

  

# 2/1

Updates

- Having trouble finding an effect: finishing LE02’s latest session
    - Run some statistical tests
- implementing a new stroop task: color word match, variance analysis, statistical analysis
- Chronic stability paper, Mike happy to contribute

  

General

- Daekyoo leaving 2/17
    - Develop how to documents for marker placement, Vicon, Visual3D
- New computer, moved cart out
- Aarika going to San Diego
- Paul Marasco leaving VA lab: we may get second thermal camera
- Open source leg: Anish is putting it together
- Carol Biomedical to make EMG board for UECU / ASCU: completed and being sent soon
    - Onkar + Lindsey will work on it

  

Subjects

- LE01 19 or 13
- LE02 25
- LE04 March 27-29
- LE06 next Wednesday: 8th
- Candidate screening almost complete, discussing with surgical team

  

Protocol modifications: latest approved version is on R drive , borrow some from implant surgery

- Increasing cap on # of people to consent
- Adding thermal imaging for diabetic
- Surface stim + vibration
- Bring able bodied up to date with implant protocol

  

To Do

- Target Neural interfaces conference

# 1/4

Updates

- Over break, dug into a detailed speed analysis for my dual task data. Attempting to split the data into various early and late segments to investigate the effect of switching tasks and any adaptation effects over time
- Speced out a new lab PC that will hopefully be approved soon
- Put in an order for a new lab camera
- Looked into some more dual task literature specifically dual motor tasks

Future Plans

- Finish up dual task data analysis
- Get a submission together for NER at the end of the month
- Start developing an improved DT experiment, dual motor or modified cognitive (N-back or color-word matching (”binary stroop”)

  

Recruitment Updates

- Aarika gave a talk with a lots of interest, one diabetic
- Interested diabetic participant wants to enroll!
- Interested participant from Seattle: going over forms, need to look at his records

  

General Updates

- Two DoD reports, general updates needed: dual task data results **Next Tuesday 10th**
- 60 minutes coming in on Jan 18th: see LE01 during stair negotiation, balance machine, APL walking exp
    - B-roll footage for neuro prosthetics
    - Working with app control ASCU, Suzhou : be able to use it instead of standalone **Be on look out for that**

  

Subject Scheduling

- LE06 Jan 11th and 13th Wed + Fri: 9-11, 12-2
- LE02 21st
- LE04 waiting to hear back

  

### To Do

- [x] DoD update paragraph
- [x] Learn ASCU control with Suzhou
- [ ] NER one page abstract submission due Jan 27: neuroengineering conf
- [x] Follow up with Matt
- [ ] Paper inventory for next time

  

# Computer

Specs

- 1 TB, i9, NVIDIA graphics , 32 GB

  

Justification

- Graphics card: [https://docs.vicon.com/display/Nexus214/Graphics+processors+for+Nexus](https://docs.vicon.com/display/Nexus214/Graphics+processors+for+Nexus)
    - [https://www.mathworks.com/support/requirements/choosing-a-computer.html](https://www.mathworks.com/support/requirements/choosing-a-computer.html) MATLAB acceleration
    - MX series isn’t good enough: [https://www.pcgamer.com/nvidias-upcoming-geforce-mx550-mobile-gpu-struggles-to-beat-amd-vega-integrated-graphics/](https://www.pcgamer.com/nvidias-upcoming-geforce-mx550-mobile-gpu-struggles-to-beat-amd-vega-integrated-graphics/)
- Windows 10: [https://docs.vicon.com/display/Nexus214/Requirements+and+upgrading](https://docs.vicon.com/display/Nexus214/Requirements+and+upgrading)
- Intel processor: [https://docs.vicon.com/display/Connect/Improving+system+performance+on+AMD+CPUs](https://docs.vicon.com/display/Connect/Improving+system+performance+on+AMD+CPUs)
- MATLAB reqs: [https://www.mathworks.com/support/requirements/matlab-system-requirements.html?s_tid=srchtitle_system requirements_1](https://www.mathworks.com/support/requirements/matlab-system-requirements.html?s_tid=srchtitle_system%20requirements_1)
- Screen: data visualization, conference prep, image analysis

  

Dell: [https://www.dell.com/en-us/shop/compare?ocs=wdr13aurcm2h,wdr13fpqph,wdr15aur40h](https://www.dell.com/en-us/shop/compare?ocs=wdr13aurcm2h,wdr13fpqph,wdr15aur40h)

MicroCenter: [https://www.microcenter.com/product/650913/dell-xps-8950-gaming-pc-platinum-collection](https://www.microcenter.com/product/650913/dell-xps-8950-gaming-pc-platinum-collection)

CDW: [https://www.cdw.com/product/lenovo-legion-t7-34iaz7-tower-core-i9-12900k-3.2-ghz-32-gb-ssd-1-tb/7139597?pfm=srh](https://www.cdw.com/product/lenovo-legion-t7-34iaz7-tower-core-i9-12900k-3.2-ghz-32-gb-ssd-1-tb/7139597?pfm=srh) but it’s windows 11 :/

- [https://www.cdw.com/product/lenovo-legion-t7-34iaz7-tower-core-i9-12900k-3.2-ghz-32-gb-ssd-1-tb/7139597?pfm=srh](https://www.cdw.com/product/lenovo-legion-t7-34iaz7-tower-core-i9-12900k-3.2-ghz-32-gb-ssd-1-tb/7139597?pfm=srh) Windows 10, only i7
- [https://www.cdw.com/product/hp-workstation-z2-g5-tower-core-i9-10900-2.8-ghz-vpro-64-gb-ssd-2/6493551?pfm=srh](https://www.cdw.com/product/hp-workstation-z2-g5-tower-core-i9-10900-2.8-ghz-vpro-64-gb-ssd-2/6493551?pfm=srh) Windows 10 but way overill, 64GB ram

  

Standalone MATLAB license: ask Will or Raychel

  

[https://www.cdw.com/product/lenovo-legion-t7-34imz5-tower-core-i9-11900k-3.5-ghz-32-gb-ssd-1-tb/7052005?pfm=srh](https://www.cdw.com/product/lenovo-legion-t7-34imz5-tower-core-i9-11900k-3.5-ghz-32-gb-ssd-1-tb/7052005?pfm=srh) 8 core, 1TB SSD, 2TB HDD, 2.5k

[https://www.cdw.com/product/lenovo-legion-t7-34iaz7-tower-core-i9-12900k-3.2-ghz-32-gb-ssd-1-tb/7139597?pfm=srh](https://www.cdw.com/product/lenovo-legion-t7-34iaz7-tower-core-i9-12900k-3.2-ghz-32-gb-ssd-1-tb/7139597?pfm=srh) 16 core,1 TB SSD, 1TB, HDDm 2.6k, 4-6 weeks backorder

[https://www.cdw.com/product/corsair-one-i300-compact-pc-core-i9-12900k-3.2-ghz-32-gb-ssd-2-tb/6867462?pfm=srh](https://www.cdw.com/product/corsair-one-i300-compact-pc-core-i9-12900k-3.2-ghz-32-gb-ssd-2-tb/6867462?pfm=srh) in stock, 16 core 2 TB SSD, 3.6k, needs keyboard and mouse

[https://www.cdw.com/product/lenovo-legion-t5-26iab7-tower-core-i7-12700-2.1-ghz-32-gb-ssd-1-tb/6987739?pfm=srh](https://www.cdw.com/product/lenovo-legion-t5-26iab7-tower-core-i7-12700-2.1-ghz-32-gb-ssd-1-tb/6987739?pfm=srh) 3060, 12 core, 1 TB SSD, 1TB HDD, 1.7k i7

  

[https://www.cdw.com/search/computers/desktops/towers/?key=nvidia%2Bgeforce%2Brtx&w=CA4&ln=0&filter=af_processor_processor_type_ca4_ss%3A("Core+i9")%2Caf_storage_hard_drive_capacity_ca4_bin_ss%3A("5|1+TB+-+1.5+TB"OR"6|1.5+TB+or+More")%2Caf_memory_ram_installed_ca4_ss%3A("32+GB")&SortBy=PriceAsc](https://www.cdw.com/search/computers/desktops/towers/?key=nvidia%2bgeforce%2brtx&w=CA4&ln=0&filter=af_processor_processor_type_ca4_ss%3a(%22Core+i9%22)%2caf_storage_hard_drive_capacity_ca4_bin_ss%3a(%225%7c1+TB+-+1.5+TB%22OR%226%7c1.5+TB+or+More%22)%2caf_memory_ram_installed_ca4_ss%3a(%2232+GB%22)&SortBy=PriceAsc) General search results

Compare:

  

Mouse:

- Nice corded mouse: [https://www.cdw.com/product/logitech-m500s-advanced-corded-mouse-mouse-usb/6144286?pfm=srh](https://www.cdw.com/product/logitech-m500s-advanced-corded-mouse-mouse-usb/6144286?pfm=srh)
- Very cheap mouse [https://www.cdw.com/product/logitech-m100-usb-wired-mouse/2074249?pfm=srh](https://www.cdw.com/product/logitech-m100-usb-wired-mouse/2074249?pfm=srh)

Monitor:

- Basic HD monitor [https://www.cdw.com/product/lenovo-d27-30-led-monitor-full-hd-1080p-27/6412636?pfm=srh](https://www.cdw.com/product/lenovo-d27-30-led-monitor-full-hd-1080p-27/6412636?pfm=srh)
- Nicer 4k [https://www.cdw.com/product/lenovo-thinkvision-e27q-20-led-monitor-qhd-27/6786295?pfm=srh](https://www.cdw.com/product/lenovo-thinkvision-e27q-20-led-monitor-qhd-27/6786295?pfm=srh)

  

# 12/16 Git Discussion

Git Presentation

- Version control, backups, sharing

  

Make github account, get user name added to APT rellinc team

  

  

# 12/14

Updates

- Getting a high processing computer for the lab - not connected to VA network
    - Visual3D seat
    - VICON handled through VA : hard to justify
- Potential candidate
    - Talking with someone from conference

  

Exp

- LE01 tomorrow 8-10
- LE02 Sat: Hannah, Daekyoo APL, Suzhou MSL
    - Jan 21?
- LE04: looking into later weeks of Jan

  

  

LE06 Thresholding

- 3 contacts with sensation with tested params
- May need to go higher / give it more time
- Next sessions
    - How high thresholds are, will they settle
    - Do final cuff
    - Phantom pain: approved questionaries
        - Lee Fischer reported changes in pain : sensory organization test results , spinal cord stim
- Better cushion or a standing break

  

New Ideas

- Daekyoo: SNP effects on walking efficiency under various stim conditions + walking speeds
    - Previous work: slow fixed paced, 0.5
    - Did not change stim intensity
    - Hypoth: most efficient walking speed affect by SNP, most efficient walking affected by stim intensity
    - 3 sessions: 30 mins of characterizing stim intensity + location, 15 walking
    - Q&A
        - Speed not normalized between subjects
        - Randomize data point s
        - Would work with longer walk times?
        - Resolution can be shaper

  

To Do

- NER deadline soon, think about abstract
- Look into camera model from Tyler’s lab:
    - Work with tripods: xx.
- Look into VICON license
- Good progress report for Jan 4 meeting

  

# 11-1

Updates

- Collected set of data from LE01
- All fellowship applications
- Data analysis for DT
- Working on getting chronic stability paper out the door

  

Upcoming surgery: transfemoral LE06 Nov 23

- Nov 9: 1230-330 for dry run in MSL
    - 130-230: exposure to implant side of thing
    - Aarika will be there to help ID muscles
- Nov 23 actual surgery
    - If you are in area + would like to be there let Hamid know asap
    - List must be signed by subj + surgeon
- Subj will be back in a week to install orange connectors + trim leads
- 2-3 weeks for first stim depending on healing : Dec 12? or week before

  

NER Baltimore

- Hamid prefers 4 pg level material to go to journals
    - Conferences are more prestigious for EE and CS
    - Prefers 1 page abstract
- 1-page abstract submission deadline **Jan 27**
    - Register for poster + podium if possible: counts as PhD requirement
    - The Brain as a Part of a Complex  
        Environment  
        » External inputs to the NS
- Conference in Baltimore: April 25th
- [https://confcats-web-assets.s3.amazonaws.com/ner/2023/ner23-cfp_web-05.pdf](https://confcats-web-assets.s3.amazonaws.com/ner/2023/ner23-cfp_web-05.pdf)
- [https://ieee-ner.org/](https://ieee-ner.org/)

  

Experiment Planning

- LE02 Nov 19th
    - Hannah 2 hr
    - Lindsey pilot

  

Data Processing

- Set up time with team to talk about processing esp Daekyoo for biomechanic metrics

  

Hannah’s SFN Poster

  

- [ ] Hamid slides
- [ ] NER 1-page abstract : DT results

  

# 10/19

New members

- Eason (PT work continuing from Anna) + Onkaar (Vicon project)

  

BMES

- First podium presentations
- Madi + James presented posters
- Takeaways
    - PROMIS pain assessment
    - Nerves respond to ultrasound
- [https://www.engineering.pitt.edu/people/faculty/gelsy-torres-oviedo/](https://www.engineering.pitt.edu/people/faculty/gelsy-torres-oviedo/): similar to SMT
    - Faster leg, calculate just noticeable difference
    - Magnitude estimation
    - Also doing H-reflex work
    - Probing gait perception
    - Trained with Amy Bastian
    - May reach out to these people + Ela Plow, Dawn Taylor here for EEG work , fNIRs
        - Working on grant for cortical activity
    - Minneapolis VA: blow air on residual + see what parts of brain light up
        - MRI, fMRI

  

New Participants

- Transfemoral implant surgery being set up: hoping for Nov
- LE03: asking about surgery date, excited

  

ReLLiNC Stuff

- Iron keys for me + Lindsey asap
    - Sign for them every year, check VA emails
- R Drive: first folder is amputee, second one is able-bodied
- System for SNP params
    - Excel file under Experiments on teams: SNP params
    - Tabs for subjects
    - Notes on subj
    - Also thresholding info or any stim related notes
- ASCU for SNP in the next two weeks

  

Participants

- LE01:
    - Hour for Hannah
    - Hour for SNP on + off assuming can do some marker setup before
- 2 hours + 1 hour
- 26th or 31st
- Saturday 19th for LE02

  

  

Presentations

- Nov 2 Hannah for SFN
- **Nov 23rd Eileen**
- Dec 14 Suzhou

  

Updates

- Just did another data collection for the DT protocol, with LE04: happy with the protocol
- Doing a lot of data analysis of the treadmill speed and accuracy of the cognitive test
    - Generate some plots for each subject
    - Met with Daekyoo to start looking at biomechanics metrics
- Lots of data analysis
- Submitted for the NSF fellowship

  

  

  

# 10/7 BMES Practice

12 mins + 3 mins questions

Suzhou: Characterizing Effects of Electrically Elicited plantar sensations on Spinal Reflex Pathways

- Concerns: background too long or specific
- Conclusion / Analysis: do they fall in line with what was set up in background
- Timing
- Background
    - Limb loss affects 1 mil, falling + fear of falling prevents daily activities
    - Plantar Sensation contribution: stability, hall recovery
    - H-reflex: understand neural pathways in neuromuscular control
        - EMS waveform
        - **slide 4: move the h-reflex label down or separate from pathway diagram**
        - Modulated by different postures, sensory inputs
    - Modulate via proprioceptive fibers: antagonist muscles, cutaneous sensation
        - Gates signal amount
        - Restoring plantar sensation → can it reintegrate in reflex pathways
    - Electrically Elicited plantar sensation
        - High denisty cuff electrodes → evoke sensations from missing limb
        - Module intensity + location based on foot-floor interactions
- Aims: 6 minutes
    - Is EPS integrated in spinal cord like natural sensation
    - How is reflex modulated by posture
- Study
    - Postures mimic phases of walking: targeting a loading amount
    - Recording H-Reflex
        - Single pulse stim to evoke reflex
        - **slide 9 kinda busy , kinda fast**
    - Example EMG results
        - M -wave then H wave
        - Some H-wave have similar morphology
        - **what is the dotted green line slide 10**
    - PCA: determining primary morphology
- Results: 9.20
    - % of trials where H-wave occurred + amplitudes
        - No sig effect on amplitude
    - Postures + electrical stim change H-reflex occurs
        - It influences pathways but…
        - **what does this mean functionally, are they able to better react to falls**
- Conclusions : 10.3
    - Largely inhibitory effect of EPS on H-reflex excitability
        - Similar to intact studies of
    - residual + EPS integrated + contributes

  

  

  

Daekyoo

  

  

# 8/31

- Maybe get access to NEC???
- Update
    - Updated DT implementation with Hannah’s idea
    - Data analysis: figured out a pipeline for DFlow side of things, working on Visual3D pipelines (can do some work offline)

  

Notes

- LE01 visit: 3-4 hrs total, 9/16
    - Be aware task may have to be made much easier
    - Use upgraded version of protocol but adjust as needed
        - Increase break time, drop down pace
    - Will have to configure SNP by myself
    - 1.5-2 hrs for me
- LE02: 9/17
    - Update protocol
- LE04
    - Update protocol

## To Do

- [ ] Check DFlow / VGait on 12th
- [ ] Continue data processing work

# 8-10

General Updates

- First data collection for the dual task experiment, refining the protocol and working out technical issues
- And working on data processing

LE04: worst case 2 hrs, best case 1.5 hrs

- Updates
    - Don’t need separate audio record, need to adjust video to be closer
    - Need to keep door closed during testing

|   |   |   |
|---|---|---|
|Setup|Marker Placement|15|
||APL Setup|10|
|Protocol Testing|Self Paced Working|15|
||Self Paced Calibration|10|
|Data Collection|Interval Calibration|5|
||Trial Block + Break|15|
||Trial Block + Break|15|
||Trial Block + Break|15|

  

- [x] Take a look ASCU how ot
- [ ] Look at protocol in R drive to see what can be done

# 7-20

## General

DoD prelim app approved! Full app due Sep 7

Boom Biomechanics podcast: 1st Wednesday of the month

## Wearable Energy Expenditure Monitor - James Baker

Adapt to lower limb amputees, altered gait, more energy expenditure

Process IMU data wireless

- SSH into RPi
- Google.colab plotting and filtering to calculate data
- Gas analysis as ground truth: Dr. Steve Collins

Progress

- Setting up Pi w/ Python, single IMU collection, plotting, SSH, 2 sensors, mounting monitor
- Simple experiments
    - Move in each axis, no rotation
    - Not getting gyroscope data with 2 sensors “hooked up”
- Walking with sensor: 5 strides
    
    ![[Untitled 450.png]]
    
- Lost heel strikes when jogging

![[Untitled 451.png]]

Future work

- Permanent connections
- RPi to wifi at bootup vs external monitor
- Stop + start data collection via button
- Testing the monitor on subjects
    - SNP effect on energy expenditure?

How To: Tec_Dev —> Files —> Wearable Energy Expenditure Monitor

  

Wearable monitor could be integrated with open source leg!

  

### Q&A

RT: IMU on thigh and shank, Stanford group only did able bodied

- Mechanical vs metabolic energy: is it correlated to metabolic?

Move it outside lab? (no wifi)

- Just need wifi to connect to laptop initially

IMUs: how is it processing the data

PCI: physiological cost index

## LE02 7/23

Hannah, Stairs, Suzhou, Eileen

  

First week of August?

  

# 6-29-2022

Update:

- Developing a dual task experiment
    - WIth self-paced treadmill walking, Vgait and visual stroop tests
    - Got introduction to the system this morning w/ Dr Hardin and Suzhou, working to program that
    - Developing experiment protocol with Suzhou, Daekyoo etc
- VR development
    
    - Implementing an IMU solution for knee joint angle tracking
    - Epiphany about the IMUs: use both and then figure out the relative angles
        - Start with leg bent at 90 for calibration
        - Plenty of papers on it, sifting through them to find a method to implement
    - OpenSim as an interesting platform: would want Xsens IMUs for it
    
      
    

- [x] DoD paragraph
- [ ] Look into V vs Astroop
    - [ ] Some amputees pay attention to audio from prosthesis

  

# 6-8-2022

Update:

Diving back into the literature to find a suitable small scale experiment. Basically want to pilot using VR as a tool and work out how best to introduce it to subjects and integrate data collection and that sort of thing. Then apply all that to the ankle simulator project

And I’ll be bugging Hamid about the chronic stability paper , but that’s the game plan

  

June 15th: Society for Neuroscience

  

Frontiers call for paper