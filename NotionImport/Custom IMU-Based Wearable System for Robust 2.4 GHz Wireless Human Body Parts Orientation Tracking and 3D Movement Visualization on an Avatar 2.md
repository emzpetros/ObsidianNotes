---
Authors: David González-Ortega,David Oviedo-Pastor,Francisco J. Díaz-Pernas,Héctor J. Aguado,Javier González-Alonso,Mario Martínez-Zarzuela
pdf name: sensors-21-06642-v3.pdf
DOI: https://doi.org/10.3390/s21196642
Publication date: 10/06/2021
Literature Type: Paper
Relevant project(s): Ankle Sim
Objective of study: |-
  Feasibility of a low cost IMU tracking solution, communication via 2.3 GHz channels
  Good for Bluetooth + WiFi busy situations 
  10 sensors max, at least 50 Hz

  IMU2Segment approach w/ quaternions
  Real-time data acq + visualization in Unity 
Theory: |-
  High end solutions: Xsens MTw Awinda [31],Perception Neuron [32], Opal (APDM) [16,19,33], or Physiolog (Gait Up) 
  - Expensive hardware + license fees
Citations: "0"
Core paper?: No
Journal: Sensors
Key terms: IMU,Unity,full body kinematics,kinematics
Name:
  - "[[Custom IMU-Based Wearable System for Robust 2.4 GHz Wireless Human Body Parts Orientation Tracking and 3D Movement Visualization on an Avatar]]"
Status: First Pass
---
# System Hardware

![[Untitled 597.png]]

  

## Communication

![[Untitled 598.png]]

FreeRTOS OS for data acq + transmission via USB dongle

- Master slave scheme , max 60Hz for real-time movement

  

## IMUs

Heading reset performed on power on when all are //

Standard rigged Unity avatar:

- Configurable joints

![[Untitled 599.png]]

![[Untitled 600.png]]

1. Calibration
    - T pose
    - Record initial quaternion
    - Compute orientation relative to global space
2. Translate to Unity coordinate system
3. Rotate bone from initial quaternion to calculated one

  

Absolute positions not trackable: i.e. walking will just move in place

- Can still estimate joint angles
- Body segments represented independently

  

# Experiments

Static test of an arm analogue and calculated joint angle: max error, 0.6 degrees

Dynamic test moving upper arm: two sensors on arm, one on spine as point of ref

Applying slerp in Unity to smooth movement

  

Errors < 5 degrees

![[10_CustomSensors_JumpingJacks.mp4]]

![[10_CustomSensors_JumpingJacks_Camera.mp4]]

Communication

  

![[XsensDOTsensors_ArmsRise.mp4]]