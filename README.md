# Dual-Axis Arduino Solar Tracker

A dual-axis solar tracker that points a solar panel at the brightest light using four light sensors and two servo motors.

This was a six-person class project for De Anza College E10 (Intro to Engineering), Sept to Dec 2025. The goal was a more efficient way to charge phones outdoors. The Arduino code and the 3D-printed parts (arm, base, bottom, middle and LDR mount) came from online files, and the parts were printed at school.

**My part:** I wired the circuit, printed the base and modified it so it could rotate fully, and worked on the Arduino code with two teammates. The team built and tested it together.

## Hardware

- Microcontroller: Arduino Uno (ATmega328P)
- Sensors: 4 light-dependent resistors (LDRs)
- Actuators: 2 SG90 micro servos (pan and tilt)
- Power: 5V voltage regulator circuit
- 3D-printed frame, soldered connections

## How it works

The Arduino runs a continuous control loop written in C++:

1. Reads the 4 analog light sensors.
2. Averages the top, bottom, left and right sensor pairs.
3. When the difference between a pair passes a fixed threshold, it moves the matching servo 1 degree at a time toward the brighter side.

## Results and limits

- It followed a phone flashlight in real time. Testing was indoors with a flashlight, not in sunlight.
- Measured range: about 160 degrees horizontal and about 40 degrees vertical. The vertical range is small because the vertical motor was misplaced.
- Rotation is limited in code so the arm does not break itself.
- The battery charging test was skipped because a part was missing.
- Next steps from the project report: add a charge controller and an LCD.

## Files

- `Solar Tracker Code.ino`: the Arduino sketch
- `3D-Files`: the printed parts
- `Solar Cell Circuit Diagram.png`: the circuit diagram
- `Final Project Report.docx`: the class report
- `Demo`: demo of the tracker following a light
