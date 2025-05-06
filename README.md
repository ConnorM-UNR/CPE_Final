Adaptive Climate Control Module (Evaporative Air System)

Project Summary

This embedded climate regulation system was created as an energy-conscious cooling device for arid environments.
Utilizing sensor inputs and logic-based state transitions, the system autonomously governs fan operation, identifies
system faults, and shares live environmental data with the user. Built as a hands-on project for the CPE 301 course at
the University of Nevada, Reno, the design blends hardware elements like environmental sensors, liquid level detection,
a cooling fan, and a motorized vent system.

System Capabilities

State-Based Logic Architecture:
The device cycles through four operational modes (OFFLINE, MONITOR, COOLING, FAULT) that shift automatically
according to sensor conditions.
Smart Cooling Activation:
The fan mechanism turns on once the ambient temperature surpasses a defined limit.
Fault Awareness:
Monitors water supply and enters a FAULT condition when fluid levels drop below safe margins.
User-Controlled Vent Adjustment:
Enables manual airflow direction through a potentiometer-driven stepper motor.
Real-Time System Display:
Continuously shows temperature, moisture content, and current mode on a two-line character LCD.

Hardware Utilized
- ATmega2560 Board (Arduino Mega)
- DHT11 Temperature/Humidity Sensor
- Water Presence Detector
- Bipolar Stepper Motor for Vent Movement
- 16x2 Liquid Crystal Display
- Brushless Fan

Adaptive Climate Control Module (Evaporative Air System)
- Multi-color LED Indicators (Yellow, Green, Blue, Red)
- Two Push Buttons (RESET, HALT)

Software Instructions

Install Development Environment:
- Download the Arduino IDE from the official website
- Add dependencies via Library Manager:
 - DHT.h for environmental sensing
 - LiquidCrystal.h for LCD interfacing

Program the Microcontroller:
- Open the main.ino sketch in the IDE
- Link the ATmega2560 board through USB
- Compile and deploy the code

Functional Workflow

Startup Phase:
System initializes in the OFFLINE mode (yellow LED active).

Monitoring Mode:
While in MONITOR state, it checks air conditions and updates the LCD.
Switches to COOLING when heat threshold is breached.

Cooling Operation:
Fan begins running and vent direction can be altered using the control knob.

Error Detection Routine:
If water is detected to be low, the system shifts to FAULT mode, stops the fan, and notifies the user.
Manual Shutdown:

Pressing the stop button resets the unit to OFFLINE, disabling all functions.
Adaptive Climate Control Module (Evaporative Air System)
Development Hurdles

Delayed Fan Response
- Problem: Slow activation of cooling fan
- Fix: Enhanced wiring layout and inserted startup delay code

Water Level Inaccuracy
- Problem: Random sensor glitches
- Fix: Added input validation logic and improved sensor calibration

Possible Enhancements
- Replace DHT11 with DHT22 for finer readings
- Incorporate a higher-quality fan to ensure smoother airflow

Acknowledgment
This build was carried out by Dennis Affo and Cade Canon for CPE 301 at the University of Nevada, Reno. We
appreciate the encouragement and input provided by our instructor and peers.

Usage Rights
This project is made available under the terms of the MIT License.
