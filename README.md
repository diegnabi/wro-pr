Engineering materials
====

This repository contains engineering materials of a self-driven vehicle's model participating in the WRO Future Engineers competition in the season 2023.

## Content

* `t-photos` contains 2 photos of the team (an official one and one funny photo with all team members)
* `v-photos` contains 6 photos of the vehicle (from every side, from top and bottom)
* `video` contains the video.md file with the link to a video where driving demonstration exists
* `schemes` contains one or several schematic diagrams in form of JPEG, PNG or PDF of the electromechanical components illustrating all the elements (electronic components and motors) used in the vehicle and how they connect to each other.
* `src` contains code of control software for all components which were programmed to participate in the competition
* `models` is for the files for models used by 3D printers, laser cutting machines and CNC machines to produce the vehicle elements. If there is nothing to add to this location, the directory can be removed.
* `other` is for other files which can be used to understand how to prepare the vehicle for the competition. It may include documentation how to connect to a SBC/SBM and upload files there, datasets, hardware specifications, communication protocols descriptions etc. If there is nothing to add to this location, the directory can be removed.

## Introduction

_This part must be filled by participants with the technical clarifications about the code: which modules the code consists of, how they are related to the electromechanical components of the vehicle, and what is the process to build/compile/upload the code to the vehicle’s controllers.

* We are Student Design Engineer team from the Vocational High School Manuel Mendez Liciaga from San Sebastian Puerto Rico. Our team consists of Diego Alejandro, Irachelee Villarrubia and Victor Gonzalez.

* The modules used in the code for the robot are: When the program starts, if then else statements, Repeat, Repeat until, Not, Greater than statements, less than statements, Equal statements, Color Sensor is "Color"?, When "Selected Sensor" returns closer than "Selected amount" of "Selected Meassurment", "Set yaw angle to 0", Current Yaw Angle, "Selected Motor" start at "Selected amount of power", "Selected Motor" Set relative position to 0, "Selected Motor" Go to relative position "Selected Position" at "Selected speed", Stop "Selected Motor", Set "Selected Motor' to brake at a stop, "Selected Motor" Set acceleration to Medium, "Selected Motor" Run "Selected Rotation" for "selected Amount", Variables, My blocks, Exit Program.

* The module "When Program Starts" runs all of the code below it which includes one driving motor, one steering motor, two color sensors, and two ultrasound sensors. The: if then else statements, Repeat, Repeat until, Not, Greater than statements, less than statements, and Equal statements all set conditions for the robot which also connect with every component. Color Sensor is "Color"? connects to the Color sensor at the bottom of the robot which watches the lines so it can determine when turning is necessary. When "Selected Sensor" returns closer than "Selected amount" of "Selected Meassurment" refers to the ultrasonic sensor which is constantly feeding in the information about how close the robot is to the inner and outer walls to avoid collision. "Set yaw angle to 0", and Current Yaw Angle both work with the internal gyroscope, first by resetting it to 0 for the straights, and the current yaw angle is used to keep the robot moving in a straight line since most of the times it can drift sideways because of the front wheels. "Selected Motor" start at "Selected amount of power", "Selected Motor" Set relative position to 0, "Selected Motor" Go to relative position "Selected Position" at "Selected speed", Stop "Selected Motor", Set "Selected Motor' to brake at a stop, "Selected Motor" Set acceleration to Medium, "Selected Motor" Run "Selected Rotation" for "selected Amount" all work with the driving and power motors. "Relative position motors work exclusively with the steering motor whilst the rest of the motor-related modules work with the power motor, by telling it at what speed acceleration and for how long it should run. Lastly the variables in this code were used to count how many times the robot had gone through a corner section since we had some problems where it would not repeat the indicated times. Lastly the "My blocks" are essentially functions which can be created differently from each other, in our case we used it for the turning code which was easier to understand and modify if needed.
