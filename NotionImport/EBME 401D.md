---
Priority: Today
Area: School
Status: In progress
---
- [x] M11
- [x] Introduce
- [x] M1
- [x] HW8
- [x] ECG project
- [x] [https://lafeber.com/vet/basic-information-sheet-for-the-cockatiel/](https://lafeber.com/vet/basic-information-sheet-for-the-cockatiel/)
    - [x] Look into common mode signal rejection [https://www.researchgate.net/publication/349931849_Design_of_Op-Amp_Based_ECG_Signal_Acquisition_Using_MULTISIM](https://www.researchgate.net/publication/349931849_Design_of_Op-Amp_Based_ECG_Signal_Acquisition_Using_MULTISIM)
    - [x] [https://biomedical-engineering-online.biomedcentral.com/articles/10.1186/1475-925X-4-50](https://biomedical-engineering-online.biomedcentral.com/articles/10.1186/1475-925X-4-50)
    - [x] [https://www.ti.com/lit/an/sbaa188/sbaa188.pdf](https://www.ti.com/lit/an/sbaa188/sbaa188.pdf)
- [x] Run multisim
    - [x] VC, VD, Raw input, final output
- [ ] HW 14

  

Homework assignments were decently reasonable by themselves. It was the lack of teaching around them that sometimes became an issue.  
Additionally update your assignments!! There were a couple errors / unclear parts of problem prompts that I had to hear corrected about via word of mouth. I also heard that these errors had been there for YEARS and gone uncorrected.

The most problematic part of the assigned work was the ECG project. I actually really like the overall concept of taking a real signal and processing it. It applies a lot of concepts well. However, there were several avoidable obstacles in this project. For one, Multisim is a continual issue whenever it is used. I spent multiple hours struggling with what components to use and what settings to set the function generator too. outputting data was time consuming and would often crash before finishing.

Many of these issues could be avoided with an updated project prompt!! These were all logistics, how to set up the signal input (same for everyone) and get the output (how many seconds, relevant settings to check in multisim etc). All of this if included in the project prompt would have saved me probably half a day. No exaggeration. Instead I heard how to do most of this by word of mouth and by bugging the TAs.

These issues prevented me from working on the actual circuit and processing design!! which should have been the focus

Finally in the third portion of the course (Gratzl) we had an additional lab assignment which we did not receive full details on until the last 3 weeks of class. This project was not indicated in the syllabus and put undue workload on students. Unlike the ECG project it did not have clear relevance to our learning beyond this specific optics area as well which was frustrating. Also asking students to buy lab materials even with reimbursement should not be an expectation.  
Additionally, in the third portion of the course our take home exam was 14 pages long! With 74 questions over half of which were problem solving / drawing / essay style questions. This is an incredible amount of content to ask students to cover. Either the content needs to be cut down or it needs to be split into reasonable assessments like quizzes after each unit.

  

Durand: Dr. Durand provided lots of practice problems which was helpful during review. However, some review of basic concepts would have been beneficial before this. While there's something to be said about approaching a problem incorrectly and learning I think more team needed to be dedicated to reinforcing basic concepts in review. Additionally, not everyone comes from a strong background in circuits so going over basic concepts as maybe optional videos or linking resources would have been extremely helpful.

Gratzl: Dr. Gratzl does seem to care about students and their learning. However, there's a disconnect in his teaching. During review sessions he passively waits for students to ask questions and assumes if no one does that we understand everything well. When prompted he does explain concepts well but he needs to have a more active role in teaching. Having us watch videos and expecting us to fully grasp everything we do and don't understand is a lot to ask. Sometimes as a student you don't realize how much you miss until it is reiterated in class or put in a different context. There are not opportunities for this kind of clarification.

McGivney: Dr. McGivney continues to be a fantastic professor. She can communicate concepts well, has authentic rapport with the students, and contributes to our learning with approachable but challenging assignments. I felt I learned the most during her portion of the course and was the least stressed out during it as well which counts for a lot.

There was a lot of confusion regarding the in-person component of the class. It was listed as web-learning but we were then expected to show up for a 2 hour review session every week. This should have been communicated early on so people could fit their other classes around it and not have conflicts.

Overall, I am not a fan of asynchronous classes. Having the review sessions for in person instruction was definitely a huge help but there still needed to be better communication and organization about them.

Overall, the course needs mostly logistical help.

- Making sure assignments are updated in Durand's section
- Updating the ECG project prompt to prevent headaches in the basic set up of the project
- Communicating the expectation of review sessions and if possible scheduling them before the class starts so conflicts with other classes can be worked out
- NOT assigning a huge lab assignment last minute without prior warning
- Having effective review sessions to reiterate content and not relying only on prerecorded lectures

%  
% %% Import Data  
% image = imread('Blue.jpg');  
%  
% figure;  
% imshow(image);  
% title('Original Image');  
%  
% % roi = drawpolygon  
% load('roi.mat')  
%  
% %% ROI  
% mask = createMask(roi, image);  
%  
%  
% roiImage = uint8(double(image) .* repmat(mask, [1 1 size(image,3)]));  
% roiImage = imrotate(roiImage, 8);  
%  
% figure;  
% imshow(roiImage);  
% title('Beam');  
%  
%  
% %% Intensity  
% % cropRoi = drawrectangle;  
% load('cropRoi.mat')  
%  
% cropped = imcrop(roiImage, cropRoi.Position);  
%  
% grayscale = rgb2gray(cropped);  
%  
% figure;  
% imshow(grayscale);  
% title('Grayscale');  
% %% Intensity  
% intensities = grayscale(20, :);  
% intensities = fliplr(intensities);  
%  
% figure;  
% plot(intensities)  
% xlabel('Pixel')  
% ylabel('Grayscale Value')  
% title('Image Intensity')  
% % xlim([10 675])  
%  
% %% Fit Beer's Law  
%  
% % over 5 cm  
% % a = 1.5 ;%1/cm  
% I = initialIntensity * exp(-a * d* c);

  

![[Untitled 167.png]]

![[Untitled 168.png]]

![[Untitled 169.png]]

  

  

  

  

  

  

![[Untitled 170.png]]

![[Untitled 171.png]]

% [https://www.mathworks.com/matlabcentral/answers/497221-signal-decomposition-for-a-mixed-signal](https://www.mathworks.com/matlabcentral/answers/497221-signal-decomposition-for-a-mixed-signal)

% [https://www.mathworks.com/help/matlab/math/basic-spectral-analysis.html](https://www.mathworks.com/help/matlab/math/basic-spectral-analysis.html)  
% [https://www.mathworks.com/help/matlab/ref/fft.html](https://www.mathworks.com/help/matlab/ref/fft.html)

![[Untitled 172.png]]

# M1 Electrical Safety

Physiological Effects

- Danger from muscles contracting ( falls, can’t breathe) and interruption of heart conduction
- Thresholds (A): 0.002-0.01 (perceive), 0.006 (min let-go), 0.018-0.022 (respiratory paralysis), 0.075-0.4 (ventricular fibrillation), 1-6 (entire heart contracts), 10+
- Parameters
    - Macroshocks = current at two points on body surface (some may pass through heart) vs microshocks = current direct through the heart (keep > 10uA to avoid)

Distribution of Power

![[Untitled 173.png]]

- Requirements on maximal potentials between surfaces (500mW, 40mW critical)
- Requirements on grounding of circuitries, separate system for each patient
- Ground faults possible: short betwixt hot conductor + ground
    - Conductors isolated from ground
    - Failure in one detected via line-isolation monitor

Macroshock Hazards

- Skin resistance usually limits current through body
    - 200 Ohm / limb, 100 trunk
    - Barrier interrupted during many medical procedures
- Equipment w/ metal casings that are ungrounded can cause macro shocks if something fails internally
    - Issue can occur with cords / cables + other jxn to outlet
    - Failure of ground isn’t automatically detected until dangerous shock levels, should be checked
    - Fluids can make normally safe equipment hazardous

Microshock Hazards: need electrical connection to heart

- Leakage currents: flow betwixt conductors at differing potentials
    - All it takes is one connected circuit to have a fault, microshock can flow out through other properly grounded systems
- Connection from chassis to heart AND connection form body to ground → microshock if ground of chassis breaks
- Can occur betwixt conductive surfaces as well
- Common devices: cardiac electrodes, liquid catheters for bp measurement, blood draw, tracer / drug injection

Standards and Codes

- Code = mandatory, standard = mandatary but voluntary compliance
- Various limits set chassis leakage at 100-500 uA and patient-lead leakage to 10-100

Basic Shock Prevention: isolation or all conductive surfaces at same potential (may not be ground)

Protection: Power Distribution

- Grounding system: patient-equipment grounding point goes to ref. ground to building service ground
- Isolated power systems protect from macroshock due to ground faults, also spark prevention
- Ground-fault circuit interrupters: disconnects power when ground fault occurs, prevent macroshocks (indirectly microshocks )
    - Monitoring difference between hot + neutral conductor, difference would flow to ground somewhere
    - Not for use where loss of power stops life-support equipment

Protection: Equipment Design

- Well grounded devices: esp at weak points like cords
- Leakage current reduction via insulation, layour
- Double insulation by electrically separating chassis + outer case - protects from macro + micro
- Operate at low voltage
- Isolation amplifier: break up ohmic continuity but still transport the signal
    - Transistor, optical, capacitive approaches
- Isolate or prevent electrical route to heart: insulated connectors, catheters

Electrical Safety Analyzers : cost vs efficiency tradeoff

Testing Electric Systems

- Receptacles, ground system limit resistance dif between receptacle + ref ground, isolated power system LIM working

Tests of Electric Appliances

- Ensure ground pin to chassis resistance difference < 0.15 ohm: test with flexed power cord
- Leakage current limited to 500 or 300uA for patient care areas
- Pateint leads: < 50 uA, <10 for isolated leads
    - Test betwixt pairs
    - Test current flow if line voltage were applied - isolation / risk current (< 50uA)s