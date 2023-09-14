---
Priority: Today
Status: Not started
---
- [x] Find modeling paper
- [ ] Report

  

[https://www.st-andrews.ac.uk/~wjh/hh_model_intro/](https://www.st-andrews.ac.uk/~wjh/hh_model_intro/)

[https://stackoverflow.com/questions/43758736/solving-differential-equation-until-periodicity](https://stackoverflow.com/questions/43758736/solving-differential-equation-until-periodicity)

  

Returning to the author’s results, the model was validated using data from an _in vivo_ mouse model.  US was used to stimulate the prefrontal cortex and if the threshold for stimulation was reached an EMG signal would be read from the mouse’s leg.  The parameters of the US were varied over a range of intensity and frequency values.  As shown in Figure 14, the values of the NBLS model align well with the experimental data.

---

Figure 14: Model validation from an _in vivo_ study using mice.

---

  

% Simulate BLS  
global tCm  
tCm = [0:0.000001:tSpan(2)];  
freq = 0.3;  
offset = 1.1;  
scale = 1;  
global CmOutput  
CmOutput = (scale * -sin(tCm * freq)) + offset;  
figure  
plot(tCm, CmOutput)

  

  

  

---

  

  

%% Setup EBME 456 Modeling Project

clear all  
close all  
clc

%% Parameters  
Cm = 6.554E-7;  
gK = 3.4274E-5;  
gNa = 10.8268E-5;  
gL = 2.8562E-7;  
EK = -12.1; %mV  
ENa = 114; %mV  
EL = 10.52; %mV

%% Test  
tSpan = [0 40];  
solverOptions = [];

Vm0 = 0;  
n0 = 0.34;  
m0 = 0.081;  
h0 = 0.45;  
gNa = 3.5e-5;%1e-5:0.5e-5:10e-5;

ICs = [Vm0, m0, h0, n0];  
voltageChange = 1;

legendStr2 = string([]);

[t2, output2] = ode15s(@model,tSpan, ICs, solverOptions, Cm, gK, gNa, gL, EK, ENa, EL, voltageChange);

```
legendStr2(end + 1) = strcat("g_{Na} = ",num2str(gNa));%% Plot 3hold onplot(t2, output2(:,1))title('V_m')xlabel('Time (ms)')ylabel('V_m (mV)')hold offlegend(legendStr2,'Location','eastoutside');
```

%% Model Function  
function output = model(t, input, Cm, gK, gNa, gL, EK, ENa, EL, voltageChange)

% vm = input(1); m = input(2); h = input(3); n = input(4)  
Vm = input(1);  
m = input(2);  
h = input(3);  
n = input(4);

alpham = (25 - Vm) / (10 *(exp( (25 - Vm) / 10 ) - 1));  
alphah = 0.07 * exp(-Vm / 20);  
alphan = (10 - Vm) / (100 *(exp( (10 - Vm) / 10 ) - 1));

betam = 4 * exp(-Vm / 18);  
betah = 1 / (1 + exp((30 - Vm) / 10));  
betan = 0.125 * exp(-Vm / 80);

% Part 2  
INa = gNa * m^3 * h * (Vm - ENa) * 1000;  
IK = gK_n^4_(Vm - EK) * 1000;  
IL = gL*(Vm - EL) * 1000 ;

%derivative of input: Vm, m, h, n  
if(voltageChange == 0)  
output(1) = 0;  
else  
if t > 1  
output(1) =((0.01 - gNa * m^3 * h * (Vm - ENa) * 1000 - gK_n^4_(Vm - EK) * 1000 - gL*(Vm - EL) * 1000 )/ Cm ) ;  
else  
output(1) =((0 - INa - IK - IL )/ Cm ) ;  
end  
end  
output(2) = alpham*(1 - m) - betam * m;  
output(3) = alphah*(1 - h) - betah * h;  
output(4) = alphan*(1 - n) - betan * n;

output = output';  
end