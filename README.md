# PID-Controller-based-Solar-Lawn-Mower
Designed and tuned a PID control loop to stabilize motor speed and improve energy efficiency under varying load. Published in the International Journal of Creative Research Thoughts (IJCRT).

# PID-Controller-based-Solar-Lawn-Mower

## Objective
This project designed and built an automatic, solar-powered lawn mower prototype. A PID controller keeps the cutting motor at a steady speed when the blade meets dense grass. The mower runs in automatic mode by default, can be switched to manual control, and is operated from an Android app over Bluetooth. Using a magnetometer and GPS module, it can also navigate stored waypoints. The PID controller was designed and simulated in MATLAB/Simulink, and the hardware was tested on a working prototype.

This was a team project for the B.Tech in Electrical and Electronics Engineering at Mar Athanasius College of Engineering, Kothamangalam (APJ Abdul Kalam Technological University, May 2023). The methodology and results were published in the *International Journal of Creative Research Thoughts (IJCRT)*, Volume 11, Issue 6, June 2023 (ISSN: 2320-2882, Paper ID: IJCRT2306686).

**My contribution:** I designed and tuned the PID control loop, using iterative parameter testing to stabilize motor speed and improve energy efficiency under varying load.

**Team:** Adersh Remesh, Amarjith S, Amjed Ali P, Ashly S Pathirickal
**Project Guide:** Prof. Deena George

### Skills Learned

- Designing and tuning a PID controller for DC motor speed control.
- Modelling and simulating control systems in MATLAB/Simulink.
- Circuit design and simulation in Proteus.
- Embedded systems and sensor integration with Arduino.
- Solar power system design: panel, charge controller and battery.
- Autonomous navigation using GPS, a magnetometer and obstacle sensors.
- Building a Bluetooth-controlled Android app for manual control and waypoint navigation.
- Prototype fabrication, testing and optimization, plus technical writing for a peer-reviewed journal.

### Tools & Components Used

**Software**
- **MATLAB/Simulink** for PID controller design and simulation.
- **Proteus 8 Professional** for circuit design and simulation.
- **Arduino** for the microcontroller code.
- **Android app** for Bluetooth control and waypoint navigation.

**Hardware**
- **Arduino** microcontroller
- **Solar panel** with a **solar charge controller**
- **12V 7Ah sealed lead-acid battery**
- **OG555 12V DC motor** (cutting blade) and **DC gear motors** (drive)
- **L298N motor driver**
- **Ultrasonic sensor** and **infrared sensors** for obstacle detection
- **GPS module** and **magnetometer** for location and heading
- **Hall-effect magnetic encoder** and **MG-90S micro servo**
- **Bluetooth module** for phone communication

## System Overview

Solar Panel → Charge Controller → Battery → Voltage Regulator → Microcontroller → Motor Driver → Left/Right Drive Motors
The battery also powers the cutting blade motor. The microcontroller takes input from the smartphone, GPS module, magnetometer, infrared sensors and ultrasonic sensor.

*Ref 1: System Block Diagram*
![Block Diagram](link-to-image)

## Steps

Below are the key steps taken in the project:

### 1. Research and Literature Review
Existing solar and automatic grass cutters were reviewed to find their limitations. Many commercial mowers need a guide wire around the lawn, mow in uneven patterns, cannot handle inclines and are expensive. This project aimed to overcome those limitations.

### 2. System Design and Component Selection
The chassis, power system and sensors were chosen around the weight, dimensions and power needs of the prototype. A 12V 7Ah battery with a solar charge controller was selected to power the motors and to keep the mower working on cloudy days and at night.

*Ref 2: Lawn Mower Design Model*
![Mower Design](link-to-image)

### 3. Circuit Design and Simulation
The circuit was designed and simulated in Proteus 8 Professional. It includes the solar panel and charging circuit, battery, motor drivers, ultrasonic and infrared sensors, GPS module and Bluetooth module.

*Ref 3: Proteus Circuit Diagram*
![Circuit Diagram](link-to-image)

### 4. PID Controller Design and Simulation
A PID controller was designed in MATLAB/Simulink to hold the cutting motor at a set speed of 2900 RPM. When the blade meets dense grass the motor speed drops, and the PID controller compensates for the load. The controller used **Kp = 96, Ki = 117 and Kd = 8**. The simulation showed the motor speed settling at the set point.

*Ref 4: Simulink Model and PID Controller*
![Simulink Model](link-to-image)

*Ref 5: Simulation Result (Speed vs Time)*
![Simulation Result](link-to-image)

### 5. Android App Development
An Android app was built to control the mower over Bluetooth. It has:
- Manual driving controls: forward, backward, small turns, 90° turns and stop
- Automatic and manual mode switching, and cutting motor on/off
- GPS waypoint navigation: get current location, set waypoints, start navigation and clear waypoints
- Compass functions: calibrate, set heading and compass drive (5° tolerance)

*Ref 6: Controller Application*
![App Screenshot](link-to-image)

### 6. Hardware Implementation
The chassis was built and the electrical components were assembled and integrated onto it. The prototype includes the solar panel, battery, charge controller, sensors and a hard steel cutting blade driven by a 12V 1000 rpm OG555 DC motor.

*Ref 7: Hardware Prototype*
![Hardware Front and Top View](link-to-image)

*Ref 8: Battery, Controller and Wiring*
![Battery and Components](link-to-image)

### 7. Testing and Optimization
The obstacle detection, manual and automatic modes and the cutting function were tested on a patch of land with obstacles.

## Results

- The system works very well on flat lawns, and the PID controller keeps the cutting motor speed steady as it cuts dense grass.
- It is pollution free and needs no manpower.
- Mixed operation mode (automatic and manual) with GPS and compass-based navigation.

**Limitations:** On uneven surfaces the obstacle detection can fail to detect nearby objects. On patchy lawns the mower halts when no grass is detected and needs manual control.

**Future work:** Add a grass collection box.

## Publication

*PID Controller Based Solar Lawn Mower*, Adersh Remesh, Amarjith S, Amjed Ali P, Ashly S Pathirickal and Deena George, International Journal of Creative Research Thoughts (IJCRT), Vol. 11, Issue 6, June 2023, ISSN: 2320-2882.
