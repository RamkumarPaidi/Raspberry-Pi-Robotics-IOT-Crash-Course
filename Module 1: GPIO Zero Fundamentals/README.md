# Module 1: GPIO Zero Fundamentals

## Overview

Welcome to Module 1 of the Raspberry Pi Robotics & IoT Crash Course!

In this module, you will learn how to interact with electronic components using the GPIO pins of a Raspberry Pi. You will use Python and the GPIO Zero library to control outputs, read inputs and build simple electronic circuits.

By the end of this module, you will be able to control LEDs, read push-button inputs, operate a buzzer and adjust LED brightness using PWM.

## Learning Objectives

By completing this module, you will be able to:

- Understand the purpose of Raspberry Pi GPIO pins.
- Identify GPIO pins using physical and BCM numbering.
- Understand the basics of the GPIO Zero Python library.
- Connect and control an LED.
- Read input from a push button.
- Control a buzzer using Python.
- Understand Pulse Width Modulation (PWM).
- Adjust LED brightness using GPIO Zero.

## Lessons

| Lesson | Topic |
|---|---|
| 01 | Introduction to Raspberry Pi GPIO |
| 02 | Understanding GPIO Pin Numbering |
| 03 | Introduction to GPIO Zero |
| 04 | LED Blinking |
| 05 | Push-button Input |
| 06 | Buzzer Control |
| 07 | PWM and LED Brightness Control |

## Hardware Requirements

- Raspberry Pi 3B+, Raspberry Pi 4 or Raspberry Pi 5
- Raspberry Pi power supply
- Breadboard
- LEDs
- 220Ω or 330Ω resistors
- Push button
- Compatible active buzzer
- Jumper wires

## Software Requirements

- Raspberry Pi OS
- Python 3
- Thonny IDE
- GPIO Zero library

### Installing GPIO Zero

Open the Raspberry Pi terminal and run:

```bash
sudo apt update
sudo apt install python3-gpiozero
```

Verify the installation:

```bash
python3 -c "import gpiozero; print('GPIO Zero installed successfully')"
```

## Getting Started

Follow the lessons in order. Each lesson introduces a concept and builds on the knowledge from the previous lesson.

For every practical activity:

1. Read the explanation.
2. Identify the required components.
3. Follow the circuit connections.
4. Write and run the Python program.
5. Observe the output.
6. Try the challenge activity.

## Important Safety Guidelines

- Disconnect the Raspberry Pi power before changing circuit connections.
- Raspberry Pi GPIO pins operate at 3.3V and are not 5V tolerant.
- Never connect 5V directly to a GPIO pin.
- Always use a current-limiting resistor with an LED.
- Do not connect motors or high-current components directly to GPIO pins.
- Check component voltage and current ratings before connecting them.

## Expected Outcome

After completing this module, you will have the basic knowledge required to connect electronic components to a Raspberry Pi and control them using Python.

These fundamentals will be used in the upcoming robotics and IoT projects.

**Build. Experiment. Learn. Connect.**
