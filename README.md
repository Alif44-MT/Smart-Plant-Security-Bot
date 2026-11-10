Smart Plant Security Bot

An Arduino-based autonomous robot that patrols a plant area by following a black line, avoids obstacles on its path, and detects intruders with a PIR sensor. When an intruder is detected, it sends an SMS alert through a GSM module. Built for CSE 438 (Robotics) at the University of Asia Pacific, Dhaka.


## Project Demo Video
[Watch Demo Video](https://drive.google.com/file/d/1tuD8K_utSBLFmq2zpLKNq5p76Jg-mif8/view?usp=drive_link)

## How It Works



## Purpose

Plants in gardens, nurseries, or small facilities need constant watching, but a person cannot be there all the time. This robot automates that job. It follows a fixed line around the plant area, stops and reroutes when an obstacle blocks its path, and raises an alert when someone attacks or disturbs the plants, so the owner is notified even when they are away.

## Features

Line following: IR sensors keep the robot on the black track.

Obstacle detection: A 360° ultrasonic sensor scans around the robot. When an obstacle blocks the line, the robot stops, moves aside, and searches for the line again before continuing.

Intruder detection: A PIR sensor watches the plant area for people attacking or disturbing the plants.

SMS alerts: When an intruder is detected, a GSM module sends an SMS to a pre-set phone number.

Status display: An I2C LCD shows the robot's current state.

## Hardware Components

Arduino board (microcontroller)

L298N motor driver

DC motors and wheels

IR sensors (line following)

Ultrasonic sensor (obstacle detection)

PIR sensor (intruder detection)

GSM module (SMS alerts)

I2C LCD display

Servo motor (if used for 360° ultrasonic scanning)

Battery / power supply

## How It Works – Step by Step

The robot starts and follows the black line using the IR sensors.

The ultrasonic sensor scans 360° around the robot. If an obstacle appears on the line, the robot stops, moves aside, and searches for the line again.

Once it finds the line, the robot resumes patrolling.

The PIR sensor watches the plant area. If it detects someone attacking or disturbing the plants, the Arduino updates the LCD and sends an SMS alert through the GSM module.

## Software and Tools

Arduino IDE (C/C++)

GSM, LCD (I2C), and ultrasonic libraries (as used in the project)

## Challenges Faced

Motor direction and wiring issues with the L298N driver, fixed by correcting the jumper settings and motor connections.

IR sensor polarity problems that made the robot misread the line, fixed by checking and correcting the sensor logic.

Iterative code refinement to make line following smooth and stable.

## Future Improvements

Add a soil moisture sensor to monitor plant health in addition to security.

Send camera or image alerts along with SMS.

Replace the fixed line with a route that adapts to the environment.
