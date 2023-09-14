# SNP

- [ ] Verify params are up to date: Teams doc
    - [ ] Verify model is using correct file in pre-load settings (restart MATLAB to apply changes)
    - [ ] Verify 0 indexing from UECU vs 1 indexing in MATLAB / lab notes
    - [ ] If needed, rebuild hex file from model
        - Files under R:/SL/Standalone
- [ ] Verify outputs: PW change on scope
    - [ ] LMTTOOL: start server for COSMIC C
    - [ ] Load hex using COSMIC C
        - If not working…
        - Under C:/UECU: run Ram hex file, then hello.hex [Restart after each]
    - [ ] Oscilloscope
    - [ ] Oscil. cables
    - [ ] Test board
    - [ ] Check heel
    - [ ] Check toe
    - [ ] Check mid foot
- [ ] Gather all materials
    - [x] Fanny pack
    - [x] zip ties
    - [x] tape
    - [x] Insole
    - [x] Woodstock
    - [x] Woodstock battery
    - [x] UECU
    - [x] UECU batteyr
    - [ ] Phone stand

  

0 indexed in initialParams

- min, max, ref:
- Amplitudes are levels not actual values

LE01

- Ground patch; goes on bony part of hip
- First discharge it with orange
- green part of UECU perc cable

Need USCU 25 with radio board

- Plug 1 + 2

Woodstock needs battery: AAs

- Green light for on
- zip tie to prosthesis

  

Programming

- LMTOOLs: stop + start server
- C coder, build

MATLAB

- Init params in same folder as UECU v.05
- UECU lite block library is fine
- Need UECU specific model
- main subsystem→ stim on—>check for 2 stim on for 2 perc board
- Model properties —> preload fxns: should see changes come up in var window

UECE: hold to turn off, turn on then press again

  

  

  

# Marker Set Up

1. CamsDigitalFP setting
2. Check config on DFLOW
3. Take static trial
4. 27 markers total

  

# Data Collection

Take static trial

Take baseline walking with Sim ON and Stim OFF

  

In D-Flow

1. Reset markers used for self-paced tracking
2. Adjust file naming
    1. Baseline or ST_VS or DT
3. Arrange output windows of Main, VStroop, and Walk scripts

  

Participant

- Verify stim is ON

  

SNP

- Green = stim on / select
- Red = stim off / back
- White = cycle through options
- Power: press and hold to turn off (Screen flashes), press once to turn on, again to start loaded program
- Troubleshooting:
- Correct COM port for program
    - Not running multiple instances of ULoad
    - Battery has power
    - Perc board connections are secure

  

In D-Flow Run Window

1. DFlow: Play
2. Vicon + DFlow: Record Data
3. ~~Participant stomps~~
4. Start treadmill at slow fixed pace and increase to self-selected pace
5. Activate self paced mode
6. Begin video
7. Start task