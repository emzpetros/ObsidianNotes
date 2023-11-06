# To Do
- [x] update manuscript with info from mike miller
- [x] update manuscript w/ LE04 data
- [x] Update manuscript with stuff from CFINE refs
- [ ] Update intro with HC comments
- [ ] Follow up: surface stim not needed bc lack of implanted components?

  

# Fall 23 Edits
Intro reorganize: 
```
For example: determine how you would like the intro to develop: you introduce sensory neuroprosthesis, then say why it is important, then you go to the importance of the sensation from the lower limb, and then you say why implanted approaches are better, then focus on cuff electrodes and highlight the need for chronic stability. Overall, this is a good flow but it seems some parts need a little merging or deleting to keep the intro on a focused message and not jumping between different topics. Try to abbreviate a few key words to avoid repeating. Also, it felt to me that you start focusing on cuffs but you make it general all of a sudden and then you come back to cuffs again. It is ok to say intraneural electrodes are not a long-term option.
```
- Neuroprostheses are connected to body, sensory systems
- Why sensory info is important - functional challenges


Importance of sensation for LLA
Conventional prostheses fall short
Sensory neuroprostheses restore sensation 
*implanted* Approaches for LLA
- Spinal stimulation 
- Peripheral 
	- Intra neural
	- Extraneural
need to look at chronic stability in lower limb 



# Outline

- Intro
    - Briefly outline why we would want to restore sensation
        - Why via neural interface vs sensory substition
    - Challenges of current electrode technology
    - Previous work on chronic stability
        - Limited to comparing electrode types
        - Didn’t focus on lower limb
    - Our specific C-FINE system
        - Previous validation
    - Opportunity to examine multiple hardware configurations and lead routing strategies
- Methods
    - Research Participants: background characteristics
    - Hardware
        - C-Fines
        - Connector set ups
    - Surgery
        - Details on LL3,4 vs LL1,2
    - Outcome Measures
        - Impedance
            - Measurement technique: surface electrode for ground, measuring entire system
        - Charge Density
            - _at threshold_ description
- Results
    - Classification of responses
        - Table of impedance and threshold descriptions
    - Overall performance: stable contact count
    - Effect of surgical procedure
    - Lead breakages
- Discussion
    - Causes for specific contact categories
    - Concerns for long term implantation

  

**Comments**

- Describe how impedance is measured, show probe placement , scope output (2018 paper)
    - Note stimulation is monophasic charge balanced: cathodic first
- Device pathway: device to biology interface, return current, surface anode
- Impedance measurement of _entire_ system: perc + CFINE
    - Could also be altered by changeds at the interface of electrode, return path especially with ground patch method (changes in skin resistance)
- Better definitions of charge density @ just-perceived sensation, threshold charge density for receiving sensation
- “Stability” as a term, co**uld refer to device problems, interface problems, biology problems**
    - “Stableness” of stimulation could be confused with stability of stimulation parameters: subject to change over time, due to tissue healing, perception changes
    - “device failure” as the main focus : wire breakage, physical damage , corrision
        - Stability of implanted devices specifically
    - Longevity / survival of components
- Table for impedance definitions and imp threshold combinations w/ explanation
- Clarity on hardware for each
- Clarify on surgical procedure
    - Checking slack was not emphasized at first
    - In future surgeries, took care to maintain slack in leads



  

# Notes

Common points of failure here are the electrodes themselves and the connecting leads.  
Implantable electrodes for interfacing with the peripheral nervous system can be classified according to invasiveness. Extraneural, intraneural, and regenerative electrodes offer increasing levels of selectivity and signal clarity at the cost of greater nerve damage [18]. Cuff electrodes are considered extraneural and do not penetrate into nerve fascicles or through the epineurium [19]. Though they are the least invasive electrode type, chronic stability remains a critical. Generally, cuff electrodes for restoring sensation have demonstrated stable long term performance especially when compared with penetrating electrodes [20].

  
Examining the system performance over time, we also see that LL03’s system had improved overall stability throughout  data collection (_bar graphs over time_).  Whereas LL01 and LL02 saw a drop in the number of low EI / responsive contacts, LL02 had only 7 contacts with this behavior.

  

  

QD= PA*PW/S

The stimulation was a biphasic, charge-balanced, current-controlled, asymmetric, cathodic-first waveform.  PA values could range between 0 to 5.6 mA and PW between 1-255 μs.  IPIs was kept at 50 ms with a stimulation duration of 4-5 s.

Charge density (QD, μC cm−2) of stimulation was calculated

,

in which S (cm2) was the surface area of a contact in the C-FINE.  QD values were limited to established safety levels according  to the following equation

log⁡(QD)= k-log⁡(Q)

where Q is charge per phase (μC) and k was restricted to k < 1.5-1.7 [27].

  
As mentioned above, out all the participants, LL03 had the best stability.  As seen in the _Fig. Best vs Worst Bar Graphs_ LL03’s implants maintained more functional contacts and demonstrated fewer failures than either LL01 or LL02.  This subject’s system was implanted with a revised surgical procedure.

  

Nerves with C-FINE cuffs alone have been shown to remain healthy and functional but implanted systems often depend on percutaneous leads attached to the electrodes.

. Excessive pulling on percutaneous leads attached to the implanted electrodes can transmit unwanted force to the cuff or the nerve itself [21,29].

  

![[Untitled 174.png]]

  

  

# MM

version 1 = Ardiem electrode with big bead transition to Medtronic connector

version 2 = Ardiem electrode with efforts to decrease the size of the transition bead to Medtronic connector

version 3 = Ardiem electrode with the much-smaller Ardiem connector which still has a transition bead but it is _much_ less significant than when merging the two different companies' components

|   |   |   |   |   |
|---|---|---|---|---|
|**Subject**|C-FINE Nerve Location|C-FINE Dimensions (mm)|C-FINE|Perc (2 / Cuff)|
|LL01|Sciatic|10x1|V1|V1|
|Tibial|15x1.5||||
|Peroneal|15x3||||
|LL02|Proximal Sciatic|15x3|V1|V1|
|Distal Sciatic|15x2||||
|Tibial|15x1.5||||
|LL03|Sciatic|15x3|V2|V1 Contact 9-16  <br>V2 contacts 1-8|
|Proximal Tibial|12.5x1.5||||
|Distal Tibial|||||
|LL04|Proximal Sciatic|12.5x1.5|V3|V3|
|Middle Sciatic|||||
|Distal Sciatic|||||

  

  
