Knee and ankle

Load cell

Powered, Al

Brushless drone motors: efficient, harder to control?

Battery Life:

Ankle: 2 stage belt drive, 4 bar linkage

- 30 range of motion: 10 dorsi, 28 plantar
- Can change to 15 degrees

  

Series Elastic Actuator: shock absorbance,

- Can add more springs to create more torque

New model

- Less complex
- Drive line same
- 4 bar linkage gone
- Dorsi Plantar flexion
- SEA

Documentation online

Solidworks files

  

Control

- Low, mid, high
- low: maintian position + torque, where it’s supposed to be
    - Feedback loops
    - Step test to discrete values + bandwidth test
    - 11-20hz tracking well
    - Force test: move it with a cracker
- Mid: state machine, knows state, pass commands to low level
    - Impedance control : virtual spring + damper
    - Alter stiffness —> less compliant : stair up + down
- High: detect what you’re doing
    - Raspberry Pi: python
    - State transitions are hard:
        - Dr Hargroves process, decoding EMG
    - EMG: indirect control
    - Detect action (heel strike): look back in time
        - Predict next action
        - Updating patterns
    - Train from scratch?

  

Attachment method improving

- 8 groups have used it
- 3 yrs ago

  

Force sensor:

- Load cell
- IMUs for ankle detection

Latency

- Rise times for ankle + knee: 28ms
- 10ms betwixt cycles

Control EMG type?

  

IMU angle detection

  

56,000