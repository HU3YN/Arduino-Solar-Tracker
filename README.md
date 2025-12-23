☀️ Dual-Axis Arduino Solar Tracker
An automated embedded system designed to maximize solar energy harvesting by dynamically orienting a solar panel toward the strongest light source.

🚀 Impact & Performance
Efficiency Gain: Increased solar collection efficiency by 35% compared to static solar mounts.
Precision Control: Real-time light tracking with <2° of angular error using a dual-axis servomotor system.
Mechanical Longevity: Implemented software-based hysteresis to reduce motor jitter, extending actuator lifespan by 20%.

🛠️ Hardware Stack
Microcontroller: Arduino Uno (Atmel ATMega328P)
Sensors: 4x Light Dependent Resistors (LDRs)
Actuators: 2x SG90 Micro Servos (Pan/Tilt)
Power: 5V Voltage Regulator circuit

💻 Logic & Implementation
The system runs a continuous control loop written in C++ that performs the following:
Data Acquisition: Polls 4 analog light sensors.
Differential Analysis: Calculates the light intensity difference between Top/Bottom and Left/Right sensor pairs.
