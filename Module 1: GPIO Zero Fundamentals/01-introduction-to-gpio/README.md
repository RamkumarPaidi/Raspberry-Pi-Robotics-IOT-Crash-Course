# Lesson 01: Introduction to Raspberry Pi GPIO

## 1. Learning Objective

In this lesson, you will understand what GPIO is, why it is available on the Raspberry Pi and how it helps us interact with electronic components.

By the end of this lesson, you will be able to:

- Explain what GPIO means.
- Identify the GPIO header on a Raspberry Pi.
- Understand the difference between input and output.
- Explain digital HIGH and LOW signals.
- Identify GPIO and GND connections.

## 2. What is GPIO?

GPIO stands for **General Purpose Input/Output**.

GPIO pins are connections on the Raspberry Pi that allow it to communicate with external electronic components.

Using these pins, the Raspberry Pi can:

- Control an LED.
- Read a push button.
- Operate a buzzer.
- Control a servo motor through an appropriate interface.
- Receive information from sensors.

For example, when you write a Python program to turn on an LED, the Raspberry Pi sends an electrical signal through one of its GPIO pins.

## 3. Where are the GPIO pins?

The Raspberry Pi has a 40-pin GPIO header on its circuit board.

These pins provide different functions, including:

- General-purpose input/output.
- Power connections such as 3.3V and 5V.
- Ground connections.
- Communication interfaces such as I2C, SPI and UART.

Not every pin is a general-purpose GPIO pin. Some pins have dedicated power, ground or alternate functions.

## 4. Understanding Input and Output

GPIO pins are commonly used in two ways.

### GPIO Output

An output pin sends a signal from the Raspberry Pi to an electronic component.

Examples:

- Turning an LED on or off.
- Switching a compatible active buzzer.
- Sending a control signal to an electronic driver.

### GPIO Input

An input pin receives a signal from an external component.

Examples:

- Detecting whether a push button is pressed.
- Reading the digital output of a sensor.
- Detecting a switch position.

## 5. Understanding HIGH and LOW

Digital GPIO signals have two logic states:

| State | Meaning |
|---|---|
| HIGH | Logic 1; approximately 3.3V |
| LOW | Logic 0; approximately 0V |

For example, when an output pin is set HIGH, it can provide a signal to turn on an appropriately connected LED circuit.

When the pin is set LOW, the output signal is brought to ground level.

## 6. What is GND?

GND stands for Ground.

Ground provides a common electrical reference point for a circuit and completes the current path.

When connecting components to the Raspberry Pi, the circuit usually needs an appropriate ground connection.

## 7. Practical Understanding

Consider a simple LED circuit:

- The Raspberry Pi provides a GPIO output.
- The LED receives current through a suitable current-limiting resistor.
- The LED turns on when the circuit is driven appropriately.
- The circuit returns to GND.

You will build this circuit in Lesson 04: LED Blinking.

## 8. Quick Knowledge Check

1. What does GPIO stand for?
2. What is the purpose of a GPIO output?
3. Give one example of a GPIO input.
4. What is the approximate HIGH voltage of Raspberry Pi GPIO?
5. Why do we need GND in a circuit?

## 9. Key Takeaways

- GPIO allows the Raspberry Pi to interact with electronic components.
- GPIO pins can be configured as inputs or outputs.
- Digital signals have HIGH and LOW states.
- Ground provides a common electrical reference.
- Raspberry Pi GPIO uses 3.3V logic and must be protected from 5V signals.

**Note** The Images provided in this lesson source is [Raspberry pi Documentation](https://www.raspberrypi.com/documentation/computers/raspberry-pi.html)

**Next Lesson:** Understanding GPIO Pin Numbering.
