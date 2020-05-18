# Control System Design of Ball and Plate
#### MECA482 - Control System Design
### Angel Mendoza, Chen Hung Yang, Jonathan Gomez, Marco Machuca, John Danley
-----------------------------------------------------------------------------------------
## 1. Introduction
 **Description of the project:**

The ball and plate system consists of a tiltable plate controlled by two motors at perpendicular orientations with a ball positioned on the plate. The goal is to develop the Simulink model that controls the X and Y axis of the plate system in Coppelia Sim Edu.

test

test

#### Table of Contents
- [1. Introduction](#1-Introduction)
- [2. Modeling](#2-Modelling)
- [3. Basic Algorithm](#3-Basic-Algorithm)
- [4. Controller Design and Simulations](#4-Controller-Design-and-Simulations)
  - [4.1. test](#41-test)
  - [4.2. test](#42-test)
- [5. Checklist](#5-Checklist)
  - [5.1. test2](#51-test2)
  - [5.2. test3](#52-test3)
- [6. References](#6-References)
  
-----------------------------------------------------------------------------------------
## 2. Modelling
The system is simulated in Coppelia Sim Edu utilizing a plate that is supported by two revolute joints on the individual sides that control the tilting mechanism for the balance of the ball. The control system described is to hold a freely rolling ball in a specific position on the plate using a senor for a feedback loop to maintain the position of the ball. For measuring the ball position, a camera sensor was used to provide feedback information.

### 2.1 
test:
* **test**: test
* **test**: test
* **test**: test
* **test**: test
* **test**: test

The data is processed in the following way:
* The camera observes the position of the ball in CoppeliaSim and sends the data to Matlab
* Matlab recieves data from Coppelia
* Simulink retrieves the data from the Matlab workspace and calculates the rotation of the motors, 
* test
* test

-----------------------------------------------------------------------------------------
## 3. Sensor Calibration
Vision system needs calibration:
* I don't know if this is needed because there is no physical system
* test

-

<p align = "center">
  <img src = "https://user-images.githubusercontent.com/65521928/82173337-ac787500-9881-11ea-9ed6-5ecc7b0c784f.png" height = "360px" style="margin:10px 10px">
</p>

-----------------------------------------------------------------------------------------
## 4. Controller Design and Simulations
A controller was developed to balance the ball on the plate with the following specifications:
* Settling time: Ts(s) ≤ 3.0
* Percent Overshoot: %OS ≤ 10

test

### 4.1. Force Calculations
To mathematically develop the proper equations to relate the necessary angle of lift on the balance plate (α) to the distance the ball has strayed away from the balance plate’s target location (x). Using the free body diagram below (Figure 1), forces from the ball’s inertia (Fr) and due to gravity on the ball (Fg) can be mapped out to determine the proper functions. 

<p align = "center">
  <img src = "https://user-images.githubusercontent.com/65521928/82175334-886c6200-9888-11ea-8444-ffbccba078fc.png" height = "360px" style="margin:10px 10px">
</p>

The sum of forces can be written:

<p align = "center">
  <img src = "https://user-images.githubusercontent.com/65521928/82176611-1b5acb80-988c-11ea-8478-a5c56a67b5a1.png" height = "360px" style="margin:10px 10px">
</p>

Relating the angle of tilt of the plate (α) to the force on the ball by gravity (Fg) gives the following equation: 

<p align = "center">
  <img src = "https://user-images.githubusercontent.com/65521928/82176622-2150ac80-988c-11ea-9fc1-96699cde30c8.png" height = "360px" style="margin:10px 10px">
</p>

Using torque, an equation can be formed relating force of intertia to ball radius (rb) with the proper torque equaton of the rolling ball:

<p align = "center">
  <img src = "https://user-images.githubusercontent.com/65521928/82176629-2877ba80-988c-11ea-805e-8a4c82cd2360.png" height = "360px" style="margin:10px 10px">
</p>

Fr and Fg can be used to construct the new force equation for ball displacement vs lift angle of plate.

### 4.2. Subheading Test 2
test of second subheading: **test**.

<p align = "center">
  <img src = "insertimglinkhere" height = "360px" style="margin:10px 10px">
</p>

-----------------------------------------------------------------------------------------
## 5. Checklist
Deliverables:
* Project Presentation
* Webpage
* Mathematical model of the system using MATLAB/Simulink
* show that the algorithm facilitates the design requirements
* Test algorithms on the physical system

-----------------------------------------------------------------------------------------
## 6. References

[1] Subramanian, Raaja Ganapathy, et al. "Uniform ultimate bounded robust model reference adaptive
PID control scheme for visual servoing." Journal of the Franklin Institute 354.4 (2017): 1741-1758.

[2] Kildare, R., Hansen E., Leon, E., PID Control of Furuta Pendulum, Control System Design Project Fall
2019

### Use this for inserting images into the middle of the document
<p align = "center">
  <img src = "insertimglinkhere" height = "360px" style="margin:10px 10px">
</p>

-----------------------------------------------------------------------------------------
