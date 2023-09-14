  

# GRF

COP = applicaiton point of GRF, no z (GRMoment - torque)

Body weight: average GRF + divide by 9.8

Left y values flipped bc of reference point

- neg to position mid stance

propulsive force increase → longer intact step length → more symmetrical

  

Cutoff below threshold

- LE01 drags heel

  

Step length + width: COP measurements, grpah x and y values visually

  

Butterlfy plot: COP net

- Can scale by mass to get centered at 0,0

Heel marker: position data

- x is medial/lateral

  

Initial + terminal double support phase: heel off,

- Initial for R = terminal for left

  

Step width not only indicator of instability

  

integral of power → work

- Mech. efficiency

Position data subject to interference from treadmill movement

- Heel marker can compensate for outliers
- To save time, use heel markers

  

WB_COM:

  

## R Code

FP1 = Left

# Speed

Coefficient of variation

And moving average

# Timing

Vicon Labeling: 15-30 min / 10 min block

Visual3D: 15 mins / ten minute file 3:05-

  

## Calculations

0.004s capture

Convert from timestamp to nearest frame

  

~562 seconds in dflow: 9.5 minutes

Frames in c3d: 56544

  

To make it ~9 minutes of footage: 56544 / 540 seconds = 99 frames / second

100Hz: Ts = 0.01

  

**Dflow: sample every 0.004 → 300 Hz**

# Response Standard:

- If first response is wrong then corrected, INCORRECT
- If response is given after next color shown, INCORRECT
- Errors due to color confusion in early trials , INCORRECT
- If correct response then changes answer, INCORRECT
- If “um” then correct answers, INCORRECT
- If two responses past initial appear, INCORRECT

  

Before interval added manually

![[Untitled 612.png]]

# Notes

Make all cols “Number” type in CSV before import

Events: A = start, B = walk, C = VStroop, D = AStroop, E = end of task

Format as is: # EVENT A - COUNT 1

Left is Red from back

![[Untitled 613.png]]

  

DFflow: freq = 300, ts = 0.003

- 50500 entries =

Vicon: freq = 100 Hz, ts = 0.01

  

Expecting about 144 seconds

  

  

  

## Daekyoo

Peak to Peak range of WB AM

  

GRF perpendicular distance to COM = moment of arm

cross product ^ x GRF = ex

  

COM, COP distance correlated with step length in AP

- Tells us stability
- How much we deviate from base of support

WB AM

- dynamic gait stability measure

  

APL treadmill: center of treadmill

- Y is backward, forward
- X is left, right
- Z is up and down

Midstance point using AP GRF: y direciton

- Braking, propulsion

  

Stride = same

  

Hugh Herr 2008 paper

  

  

Heel marker for step length on treadmill

- Max distance during double stance time

  

Looking for double limb support time, step width,

- May not find changes in step length, influenced by individual stepping pattern

Can have asymmetry with stability

- Need measure of both

  

Look at GRF impulse as well:

- Increased stance time can up the force produced with same peak values

  

Look at speeds when they answer + respond

- Mean stride velocity x`

Outliers

- raw - mean; cut out above standard deviation

### Tools

[https://www.motion-labs.com/software_c3d_utilities.html](https://www.motion-labs.com/software_c3d_utilities.html)

  

  

- [x] Parse dflow file for order of tasks?
- [x] Figure out Csv issue… [Split by space and comma]
- [x] Find start time
    - [x] Split into 30 second time chunks

  

# 12/7

Marker Gait Events

![[Untitled 614.png]]

![[Untitled 615.png]]

![[Untitled 616.png]]

- Original
    - HS = blue
    - TO = orange
- Marker
    - HS = green
    - TO = red
- new HS is slightly early
- TO have an average dif of -1.29 frames
    
    - Cut off of 0.06 blue vs 0.061 black
    
    ![[Untitled 617.png]]
    
- HS have an average dif of 5.135
    
    - Cut off of 0.085
    
    ![[Untitled 618.png]]
    
    ![[Untitled 619.png]]
    

  

Original gait events

- L, R

![[Untitled 620.png]]

![[Untitled 621.png]]

  

LE02 (good data)

- L HS, R HS, L TO, R TO

![[Untitled 622.png]]

  

LE01

- L TO, LHS, R TO, R HS
    
    ![[Untitled 623.png]]
    

- i = 2
    
    ![[Untitled 624.png]]
    

- i = 3
    
    ![[Untitled 625.png]]
    

- i = 4
    
    ![[Untitled 626.png]]
    

  

Stride to stride variability :

- Stride two steps
- PSt to int stride
- Add int and pst _step length_
- Should be low
- Don’t compare between legs

Stance to swing phase ratio:

- 2t factor: stance to swing time phase ratio

Stance time + push off slightly larger with SNP

  

  

  

  

  

# MATLAB

function [OUTPUT1] = GaitEvent(INPUT1)

% Static posture  
% Find how much weight each participant has  
%--------------------------------------------------------------------------  
% % Define vertical GRF for each foot from static trial  
% GRF_L = INPUT1.Variable{1,1};  
% GRF_R = INPUT1.Variable{2,1};  
% COP_L = INPUT1.Variable{3,1};  
% COP_R = INPUT1.Variable{4,1};  
% GRM_L = INPUT1.Variable{5,1};  
% GRM_R = INPUT1.Variable{6,1};

% OG  
% GRF_L = INPUT1.Variable{3,1};  
% GRF_R = INPUT1.Variable{4,1};  
% COP_L = INPUT1.Variable{1,1};  
% COP_R = INPUT1.Variable{2,1};  
% GRM_L = INPUT1.Variable{5,1};  
% GRM_R = INPUT1.Variable{6,1};

% LE04 stim off 1  
% start =  
% end =

% LE04 stim on 2

GRF_L = INPUT1.Variable{3,1}(2906:17306,:);  
GRF_R = INPUT1.Variable{4,1}(2906:17306,:);  
COP_L = INPUT1.Variable{1,1}(2906:17306,:);  
COP_R = INPUT1.Variable{2,1}(2906:17306,:);  
GRM_L = INPUT1.Variable{5,1}(2906:17306,:);  
GRM_R = INPUT1.Variable{6,1}(2906:17306,:);

LFT_CGPos = INPUT1.Variable{8,1}(2906:17306,:);  
LSK_CGPos = INPUT1.Variable{11,1}(2906:17306,:);  
LTH_CGPos = INPUT1.Variable{13,1}(2906:17306,:);  
LegCGPos_L = (LFT_CGPos+LSK_CGPos+LTH_CGPos)/3;  
clear LFT_CGPos LSK_CGPos LTH_CGPos

RFT_CGPos = INPUT1.Variable{26,1}(2906:17306,1);  
RSK_CGPos = INPUT1.Variable{29,1}(2906:17306,1);  
RTH_CGPos = INPUT1.Variable{31,1}(2906:17306,1);  
LegCGPos_R = (RFT_CGPos+RSK_CGPos+RTH_CGPos)/3;  
clear RFT_CGPos RSK_CGPos RTH_CGPos

% OG  
%{  
LFT_CGPos = INPUT1.Variable{8,1};  
LSK_CGPos = INPUT1.Variable{11,1};  
LTH_CGPos = INPUT1.Variable{13,1};  
LegCGPos_L = (LFT_CGPos+LSK_CGPos+LTH_CGPos)/3;  
clear LFT_CGPos LSK_CGPos LTH_CGPos

RFT_CGPos = INPUT1.Variable{26,1};  
RSK_CGPos = INPUT1.Variable{29,1};  
RTH_CGPos = INPUT1.Variable{31,1};  
LegCGPos_R = (RFT_CGPos+RSK_CGPos+RTH_CGPos)/3;  
clear RFT_CGPos RSK_CGPos RTH_CGPos  
%}

% LFT_CGPos = INPUT1.Variable{8,1};  
% LSK_CGPos = INPUT1.Variable{11,1};  
% LegCGPos_L = (LFT_CGPos+LSK_CGPos)/2;  
% clear LFT_CGPos LSK_CGPos  
%  
% RFT_CGPos = INPUT1.Variable{26,1};  
% RSK_CGPos = INPUT1.Variable{29,1};  
% LegCGPos_R = (RFT_CGPos+RSK_CGPos)/2;  
% clear RFT_CGPos RSK_CGPos

%--------------------------------------------------------------------------

% fc = 6;  
% fs = 1000;  
%  
% [b,a] = butter(4,fc/(fs/2));  
% GRF_L = filter(b,a,GRF_L);  
% GRF_R = filter(b,a,GRF_R);  
% GRM_L = filter(b,a,GRM_L);  
% GRM_R = filter(b,a,GRM_R);  
% COP_L = filter(b,a,COP_L);  
% COP_R = filter(b,a,COP_R);  
% clear fc fs a b

%--------------------------------------------------------------------------  
% GRF (Left Foot)  
GRF_L_temp = find(GRF_L(:,3)<30);

GRF_L(GRF_L_temp,:) = 0;  
COP_L(GRF_L_temp,:) = NaN;  
clear GRF_L_temp

for i=1:size(GRF_L,1)

```
if GRF_L(i,3) == 0    Event_L(i,1) = 0;elseif GRF_L(i,3) ~= 0    Event_L(i,1) = 1;else    disp('Error')end
```

end  
clear i

Event_L_temp = [Event_L; 0];

for i=1:size(Event_L_temp,1)-1  
Event_L_diff(i,1) = Event_L_temp(i+1,1) - Event_L_temp(i,1);  
end  
clear i

L_first = find(Event_L_diff(:,1)==1);  
L_first = L_first + 1;  
L_last = find(Event_L_diff(:,1)==-1);

clear Event_L_temp  
clear Event_L  
clear Event_L_diff

L_first_temp = L_first;  
L_last_temp = L_last;

if size(L_first,1) == size(L_last,1)  
equal = 1;  
else  
equal = -1;  
end

if equal == -1 && L_first(1,1) > L_last(1,1)  
L_last(1,:) = [];

```
else    disp('They equal to each other!')
```

end

clear equal L_first_temp L_last_temp

%--------------------------------------------------------------------------  
% GRF (Right Foot)

GRF_R_temp = find(GRF_R(:,3)<30);

GRF_R(GRF_R_temp,:) = 0;  
COP_R(GRF_R_temp,:) = NaN;  
clear GRF_R_temp

for i=1:size(GRF_R,1)

```
if GRF_R(i,3) == 0    Event_R(i,1) = 0;elseif GRF_R(i,3) ~= 0    Event_R(i,1) = 1;else    disp('Error')end
```

end  
clear i

Event_R_temp = [Event_R; 0];

for i=1:size(Event_R_temp,1)-1  
Event_R_diff(i,1) = Event_R_temp(i+1,1) - Event_R_temp(i,1);  
end  
clear i

R_first = find(Event_R_diff(:,1)==1);  
R_first = R_first + 1;  
R_last = find(Event_R_diff(:,1)==-1);

clear Event_R_temp  
clear Event_R  
clear Event_R_diff

R_first_temp = R_first;  
R_last_temp = R_last;

if size(R_first,1) == size(R_last,1)  
equal = 1;  
else  
equal = -1;  
end

if equal == -1 && R_first(1,1) > R_last(1,1)  
R_last(1,:) = [];

```
else    disp('They equal to each other!')
```

end

clear equal R_first_temp R_last_temp

%--------------------------------------------------------------------------  
% Combine GRF_L and GRF_R  
GRF_RL = GRF_R + GRF_L;

GRF_L_r = sqrt((GRF_L(:,1).^2)+(GRF_L(:,2).^2)+(GRF_L(:,3).^2));  
GRF_R_r = sqrt((GRF_R(:,1).^2)+(GRF_R(:,2).^2)+(GRF_R(:,3).^2));  
GRF_RL_r = sqrt((GRF_RL(:,1).^2)+(GRF_RL(:,2).^2)+(GRF_RL(:,3).^2));

% Combine GRM_L and GRM_R  
TEMP_R = find(GRF_R(:,3)==0);  
TEMP_L = find(GRF_L(:,3)==0);  
GRM_R(TEMP_R,:) = 0;  
GRM_L(TEMP_L,:) = 0;  
clear TEMP_R  
clear TEMP_L

GRM_RL = GRM_R + GRM_L;

%--------------------------------------------------------------------------  
% Compute the net COP

COP_R(isnan(COP_R)) = 0;  
COP_L(isnan(COP_L)) = 0;

COP_net_x = ((COP_R(:,1).*GRF_R(:,3))+(COP_L(:,1).*GRF_L(:,3)))./GRF_RL(:,3);  
COP_net_y = ((COP_R(:,2).*GRF_R(:,3))+(COP_L(:,2).*GRF_L(:,3)))./GRF_RL(:,3);  
COP_net_z = ((COP_R(:,3).*GRF_R(:,3))+(COP_L(:,3).*GRF_L(:,3)))./GRF_RL(:,3);

COP_net = [COP_net_x,COP_net_y, COP_net_z];  
clear COP_net_x COP_net_y COP_net_z

%--------------------------------------------------------------------------  
% Save measures in OUTPUT1  
OUTPUT1.GRF_L = GRF_L;  
OUTPUT1.GRF_R = GRF_R;  
OUTPUT1.GRF_RL = GRF_RL;  
% OUTPUT1.GRF_L_r = GRF_L_r;  
% OUTPUT1.GRF_R_r = GRF_R_r;  
% OUTPUT1.GRF_RL_r = GRF_RL_r;  
OUTPUT1.GRM_L = GRM_L;  
OUTPUT1.GRM_R = GRM_R;  
OUTPUT1.GRM_RL = GRM_RL;  
OUTPUT1.COP_L = COP_L;  
OUTPUT1.COP_R = COP_R;  
OUTPUT1.COP_net = COP_net;  
OUTPUT1.L_first = L_first;  
OUTPUT1.L_last = L_last;  
OUTPUT1.R_first = R_first;  
OUTPUT1.R_last = R_last;  
OUTPUT1.LegCGPos_L = LegCGPos_L;  
OUTPUT1.LegCGPos_R = LegCGPos_R;

vars = {'COP_L','COP_R','COP_net','GRF_L','GRF_L_r','GRF_R','GRF_R_r',...  
'GRF_RL','GRF_RL_r','GRM_L','GRM_R','GRM_RL','WB_COM_Dist',...  
'L_first','L_last','R_first','R_last','LegCGPos_L','LegCGPos_R'};  
clear(vars{:})  
clear vars  
%--------------------------------------------------------------------------  
end

  

  

COMPUTATION

function [OUTPUT2] = Computation(INPUT1,OUTPUT1,ProstheticSide,m)

mg = m*9.81;  
%--------------------------------------------------------------------------  
% Call measures from OUTPUT1

GRF_L = OUTPUT1.GRF_L;  
GRF_R = OUTPUT1.GRF_R;  
GRF_RL = OUTPUT1.GRF_RL;

COP_L = OUTPUT1.COP_L;  
COP_R = OUTPUT1.COP_R;  
COP_net = OUTPUT1.COP_net;

L_first = OUTPUT1.L_first;  
L_last = OUTPUT1.L_last;  
R_first = OUTPUT1.R_first;  
R_last = OUTPUT1.R_last;

WB_COM_Dist = INPUT1.Variable{44,1};

L_Heel = INPUT1.Variable{10,1};  
R_Heel = INPUT1.Variable{28,1};

%--------------------------------------------------------------------------

if ProstheticSide == 1

```
GRF_Pst = GRF_R;GRF_Int = GRF_L;COP_Pst = COP_R;COP_Int = COP_L;Pst_first = R_first;Pst_last = R_last;Int_first = L_first;Int_last = L_last;Pst_Heel = R_Heel;Int_Heel = L_Heel;
```

elseif ProstheticSide == 0

```
GRF_Pst = GRF_L;GRF_Int = GRF_R;COP_Pst = COP_L;COP_Int = COP_R;Pst_first = L_first;Pst_last = L_last;Int_first = R_first;Int_last = R_last;Pst_Heel = L_Heel;Int_Heel = R_Heel;
```

else

```
disp('Error for finding IC and TO')
```

end

Heel_diff = abs(Pst_Heel(:,2)-Int_Heel(:,2));

==Difference in y position of heel markers across every frame==

%--------------------------------------------------------------------------

Pst_diff = Pst_last(1:end-1,1)-Pst_first(1:end-1,1);  
Int_diff = Int_last(1:end-1,1)-Int_first(1:end-1,1);

==For every HS, TO pair calculate the difference in frames==

temp_Pst = find(Pst_diff(:,1)<30 | Pst_diff(:,1)>180);  
temp_Int = find(Int_diff(:,1)<30 | Int_diff(:,1)>180);

==Check if any difference is less than 30 or greater than 180 frames , is so clear those entries==

if isempty(temp_Pst)==0

```
Pst_first(temp_Pst,:) = [];Pst_last(temp_Pst,:) = [];Int_first(temp_Int,:) = [];Int_last(temp_Int,:) = [];clear temp_Pst temp_Int Pst_diff Int_diffelsedisp('Nothing was wrong!')endif size(Int_first,1)<size(Pst_first,1)	sz = size(Int_first,1);elseif size(Int_first,1)>size(Pst_first,1)	sz = size(Pst_first,1);elseif size(Int_first,1)==size(Pst_first,1)	sz = size(Pst_first,1);else	disp('Error for number of Pst_first or Int_first!')endfor i=1:sz-2% Definition
```

==Compare HS_int vs TO_pst then size: size = shorter one==

==If they are equal use TO_pst==

==Here size = 135==

==For each row of gait events from 1 to size -== **==TWO==**

==Store the frame of all 4 events in the output==

Finding intact_TO of previous cycle:

Intact leg: find where intact TO < current row of Pst_TO [1]

If there is nowhere this occurs

find where int_HS < current_Pst_TO

int_TO_pre = the entries of same index as ^ but in int_TO

else

int_TO_Pre = int_last(entires of [1] in int_TO

```
% Foot first and lastPst_ft_first{i,1} = Pst_first(i,1);Pst_ft_last{i,1} = Pst_last(i,1);Int_ft_first{i,1} = Int_first(i,1);Int_ft_last{i,1} = Int_last(i,1);% Intact Legtemp1 = find(Int_last(:,1)<Pst_last(i,1));if isempty(temp1)    temp11 = find(Int_first(:,1)<Pst_last(i,1));    Int_last_pre = Int_last(temp11(end,1),1);    clear temp11else     Int_last_pre = Int_last(temp1(end,1),1);end
```

  

Using int_TO_previous find other gait events

pst_first_exc = latest entry where pst_HS where it is less than int_last_pre

pst_TO_exc = first entry in pst_TO where pst_HS_exec > pst_TO_exe

Similar formulations follow

```
% Prosthetic Legtemp2 = find(Pst_first(:,1)<Int_last_pre);Pst_first_exc = Pst_first(temp2(end,1),1);temp3 = find(Pst_last(:,1)>Pst_first_exc);Pst_last_exc = Pst_last(temp3(1,1),1);temp4 = find(Int_first(:,1)>Int_last_pre);Int_first_exc = Int_first(temp4(1,1),1);temp5 = find(Int_last(:,1)>Int_first_exc);Int_last_exc = Int_last(temp5(1,1),1);temp6 = find(Pst_first(:,1)>Pst_first_exc);Pst_first_post = Pst_first(temp6(1,1),1);temp7 = find(Pst_last(:,1)>Pst_first_post);Pst_last_post = Pst_last(temp7(1,1),1);temp8 = find(Int_first(:,1)>Int_first_exc);Int_first_post = Int_first(temp8(1,1),1);clear temp1 temp2 temp3 temp4 temp5 temp6 temp7 temp8
```

  

WB_COM and COP_net: segments of associated file based on current gait cycle + boundary gait cycle events before and after

GRF for R, L and combined

COP similar

  

% Classification

```
% WB_COM_DistWB_COM_Dist_C{i,1} = WB_COM_Dist(Pst_first_exc:Pst_first_post-1,:);    % Pst strideWB_COM_Dist_C{i,2} = WB_COM_Dist(Pst_first_exc:Pst_last_exc-1,:);  % Pst stanceWB_COM_Dist_C{i,3} = WB_COM_Dist(Int_first_exc:Int_first_post-1,:);    % Int strideWB_COM_Dist_C{i,4} = WB_COM_Dist(Int_first_exc:Int_last_exc-1,:);  % Int stance% COP_netCOP_net_C{i,1} = COP_net(Pst_first_exc:Pst_first_post-1,:);    % Pst strideCOP_net_C{i,2} = COP_net(Pst_first_exc:Pst_last_exc-1,:);  % Pst stanceCOP_net_C{i,3} = COP_net(Int_first_exc:Int_first_post-1,:);    % Int strideCOP_net_C{i,4} = COP_net(Int_first_exc:Int_last_exc-1,:);  % Int stance% GRF_RLGRF_RL_C{i,1} = GRF_RL(Pst_first_exc:Pst_first_post-1,:)/mg;    % Pst strideGRF_RL_C{i,2} = GRF_RL(Pst_first_exc:Pst_last_exc-1,:)/mg;  % Pst stanceGRF_RL_C{i,3} = GRF_RL(Int_first_exc:Int_first_post-1,:)/mg;    % Int strideGRF_RL_C{i,4} = GRF_RL(Int_first_exc:Int_last_exc-1,:)/mg;  % Int stance% GRF_PstGRF_Pst_C{i,1} = GRF_Pst(Pst_first_exc:Pst_first_post-1,:)/mg;    % Pst strideGRF_Pst_C{i,2} = GRF_Pst(Pst_first_exc:Pst_last_exc-1,:)/mg;  % Pst stanceGRF_Pst_C{i,3} = GRF_Pst(Int_first_exc:Int_first_post-1,:)/mg;    % Int strideGRF_Pst_C{i,4} = GRF_Pst(Int_first_exc:Int_last_exc-1,:)/mg;  % Int stance% COP_PstCOP_Pst_C{i,1} = COP_Pst(Pst_first_exc:Pst_first_post-1,:);    % Pst strideCOP_Pst_C{i,2} = COP_Pst(Pst_first_exc:Pst_last_exc-1,:);  % Pst stanceCOP_Pst_C{i,3} = COP_Pst(Int_first_exc:Int_first_post-1,:);    % Int strideCOP_Pst_C{i,4} = COP_Pst(Int_first_exc:Int_last_exc-1,:);  % Int stance% GRF_IntGRF_Int_C{i,1} = GRF_Int(Pst_first_exc:Pst_first_post-1,:)/mg;    % Pst strideGRF_Int_C{i,2} = GRF_Int(Pst_first_exc:Pst_last_exc-1,:)/mg;  % Pst stanceGRF_Int_C{i,3} = GRF_Int(Int_first_exc:Int_first_post-1,:)/mg;    % Int strideGRF_Int_C{i,4} = GRF_Int(Int_first_exc:Int_last_exc-1,:)/mg;  % Int stance% COP_IntCOP_Int_C{i,1} = COP_Int(Pst_first_exc:Pst_first_post-1,:);    % Pst strideCOP_Int_C{i,2} = COP_Int(Pst_first_exc:Pst_last_exc-1,:);  % Pst stanceCOP_Int_C{i,3} = COP_Int(Int_first_exc:Int_first_post-1,:);    % Int strideCOP_Int_C{i,4} = COP_Int(Int_first_exc:Int_last_exc-1,:);  % Int stance% Step lengthSL_Pst{i,1} = mean(Heel_diff(Pst_first_exc:Int_last_pre,1),1);SL_Int{i,1} = mean(Heel_diff(Int_first_exc:Pst_last_exc,1),1);SL_symm{i,1} = (SL_Pst{i,1}/SL_Int{i,1})*100;clear TEMP% Stance timeST_Pst{i,1} = (Pst_last_exc-Pst_first_exc)*0.01;ST_Int{i,1} = (Int_last_exc-Int_first_exc)*0.01;ST_symm{i,1} = (ST_Pst{i,1}/ST_Int{i,1})*100;% Double-limb support time (Prosthetic Leg)DST_ini{i,1} = abs(((Int_last_pre-Pst_first_exc)+1)*0.01);DST_ter{i,1} = abs(((Pst_last_exc-Int_first_exc)+1)*0.01);DST_symm{i,1} = (DST_ini{i,1}/DST_ter{i,1})*100;% Single-limb support timeSST_Pst{i,1} = abs((Int_first_exc-Int_last_pre)*0.01);SST_Int{i,1} = abs((Pst_first_post-Pst_last_exc)*0.01);SST_symm{i,1} = (SST_Pst{i,1}/SST_Int{i,1})*100;
```

  

Step Length

Mean heel difference between two gait events

Symmetry is comparative measure

Stance Time

frame difference between events * ts aka 0.01 seconds / frame

  

DL Support time: both feet on ground

initial: int_TO_previous till pst_HS_current + 1?

```
% Step lengthSL_Pst{i,1} = mean(Heel_diff(Pst_first_exc:Int_last_pre,1),1);SL_Int{i,1} = mean(Heel_diff(Int_first_exc:Pst_last_exc,1),1);SL_symm{i,1} = (SL_Pst{i,1}/SL_Int{i,1})*100;clear TEMP% Stance timeST_Pst{i,1} = (Pst_last_exc-Pst_first_exc)*0.01;ST_Int{i,1} = (Int_last_exc-Int_first_exc)*0.01;ST_symm{i,1} = (ST_Pst{i,1}/ST_Int{i,1})*100;% Double-limb support time (Prosthetic Leg)DST_ini{i,1} = abs(((Int_last_pre-Pst_first_exc)+1)*0.01);DST_ter{i,1} = abs(((Pst_last_exc-Int_first_exc)+1)*0.01);DST_symm{i,1} = (DST_ini{i,1}/DST_ter{i,1})*100;% Single-limb support timeSST_Pst{i,1} = abs((Int_first_exc-Int_last_pre)*0.01);SST_Int{i,1} = abs((Pst_first_post-Pst_last_exc)*0.01);SST_symm{i,1} = (SST_Pst{i,1}/SST_Int{i,1})*100;
```

end  
clear i

OUTPUT2.Pst_ft_first = Pst_ft_first;  
OUTPUT2.Pst_ft_last = Pst_ft_last;  
OUTPUT2.Int_ft_first = Int_ft_first;  
OUTPUT2.Int_ft_last = Int_ft_last;

OUTPUT2.SL_Int = SL_Int;  
OUTPUT2.SL_Pst = SL_Pst;  
OUTPUT2.SL_symm = SL_symm;

OUTPUT2.ST_Int = ST_Int;  
OUTPUT2.ST_Pst = ST_Pst;  
OUTPUT2.ST_symm = ST_symm;

OUTPUT2.DST_ini = DST_ini;  
OUTPUT2.DST_ter = DST_ter;  
OUTPUT2.DST_symm = DST_symm;

OUTPUT2.SST_Int = SST_Int;  
OUTPUT2.SST_Pst = SST_Pst;  
OUTPUT2.SST_symm = SST_symm;

OUTPUT2.GRF_RL = GRF_RL_C;  
OUTPUT2.GRF_Pst = GRF_Pst_C;  
OUTPUT2.GRF_Int = GRF_Int_C;

OUTPUT2.COP_net = COP_net_C;  
OUTPUT2.COP_Pst = COP_Pst_C;  
OUTPUT2.COP_Int = COP_Int_C;

OUTPUT2.WB_COM_Dist = WB_COM_Dist_C;

% Added  
OUTPUT2.temp = Int_first_exc  
OUTPUT2.temp2 = Pst_last_exc

%--------------------------------------------------------------------------

end