# Lesson 02: Understanding GPIO Pin Numbering

## 1. Learning Objective

In this lesson, you will learn how to identify the pins on the Raspberry Pi GPIO header and understand the two common numbering systems.

By the end of this lesson, you will be able to:

- Identify the 40-pin GPIO header.
- Understand physical pin numbering.
- Understand BCM numbering.
- Identify GPIO, power and ground pins.
- Use BCM numbering consistently in Python programs.

## 2. The Raspberry Pi GPIO Header

The Raspberry Pi 3B+, Raspberry Pi 4 and Raspberry Pi 5 have a 40-pin GPIO header.

Each pin has a specific number and function.

The header includes:

- GPIO pins.
- 3.3V power pins.
- 5V power pins.
- Ground pins.
- Pins with alternate communication functions.

Refer to the official Raspberry Pi pinout documentation to identify the pins before connecting components.

## 3. Understanding the Two Numbering Systems

There are two commonly used ways to identify Raspberry Pi pins.

### A. Physical Pin Numbering (BOARD)

Physical numbering refers to the actual position of a pin on the 40-pin header.

For example:

- Physical pin 1 provides 3.3V.
- Physical pin 2 provides 5V.
- Physical pin 6 is GND.
- Physical pin 11 is GPIO17.

The physical numbering starts at pin 1 and continues to pin 40.

### B. BCM Numbering

BCM numbering refers to the GPIO number associated with the Broadcom GPIO controller.

For example:

- BCM GPIO17 corresponds to physical pin 11.
- BCM GPIO27 corresponds to physical pin 13.
- BCM GPIO22 corresponds to physical pin 15.

In GPIO Zero, you normally specify BCM GPIO numbers.

## 4. Physical and BCM Pin Comparison

| Physical pin | BCM GPIO | Function |
|---|---|---|
| 3 | GPIO2 | I2C SDA |
| 5 | GPIO3 | I2C SCL |
| 7 | GPIO4 | GPIO |
| 11 | GPIO17 | GPIO |
| 13 | GPIO27 | GPIO |
| 15 | GPIO22 | GPIO |
| 16 | GPIO23 | GPIO |
| 18 | GPIO24 | GPIO |
| 29 | GPIO5 | GPIO |
| 31 | GPIO6 | GPIO |

Note: This table contains selected examples, not the complete pinout and refer the images for all the pinouts and the numbering of them.

## 5. Why Use BCM Numbering?

In this course, we will consistently use BCM numbering.

For example:

```python
from gpiozero import LED

led = LED(17)
```

Here, `17` refers to BCM GPIO17, which is physical pin 11.

Using one numbering convention throughout the course helps avoid confusion when writing and sharing code.

## 6. Identifying GPIO Pins

Before connecting any component:

1. Identify the Raspberry Pi model.
2. Locate the 40-pin header.
3. Identify physical pin 1.
4. Refer to a reliable GPIO pinout diagram.
5. Identify the required BCM GPIO and corresponding physical pin.
6. Confirm the ground and power connections.

## 7. Important Precautions

- Never assume physical pin numbers and BCM numbers are interchangeable.
- Never connect 5V directly to a GPIO pin.
- Do not use power pins as GPIO outputs.
- Check the pinout before making connections.
- Be careful not to short adjacent pins.

## 8. Quick Knowledge Check

1. How many pins are present on the standard Raspberry Pi 40-pin header?
2. What is the difference between physical and BCM numbering?
3. Which physical pin corresponds to BCM GPIO17?
4. Which physical pin is GND in the examples above?
5. Which numbering convention does GPIO Zero use in this course?

## 9. Key Takeaways

- The Raspberry Pi has a 40-pin GPIO header.
- Physical numbering identifies the pin's position.
- BCM numbering identifies the GPIO controller number.
- GPIO Zero uses BCM numbering by default.
- Always check the pinout before connecting components.

**Next Lesson:** Introduction to GPIO Zero.
