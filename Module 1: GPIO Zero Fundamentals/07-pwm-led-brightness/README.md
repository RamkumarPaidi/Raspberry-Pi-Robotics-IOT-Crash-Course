# Lesson 07: PWM and LED Brightness Control

## 1. Learning Objective

In this lesson, you will learn about Pulse Width Modulation (PWM) and how it can be used to control the brightness of an LED.

By the end of this lesson, you will be able to:

- Explain the basic concept of PWM.
- Understand duty cycle.
- Use the GPIO Zero `PWMLED` class.
- Adjust LED brightness using Python.
- Create a gradual LED fading effect.

## 2. What is PWM?

PWM stands for **Pulse Width Modulation**.

It is a technique used to control the average power delivered to a component by switching a signal ON and OFF very quickly.

By changing the proportion of time the signal stays ON, we can control the average output.

This proportion is called the duty cycle.

## 3. Understanding Duty Cycle

Duty cycle is the percentage of one PWM cycle during which the signal remains ON.

| Duty cycle | LED appearance |
|---|---|
| 0% | Off |
| 25% | Low brightness |
| 50% | Medium brightness |
| 75% | Higher brightness |
| 100% | Full brightness |

These are illustrative brightness levels. Actual perceived brightness depends on the LED and the human eye.

## 4. How Does PWM Control LED Brightness?

Imagine an LED being switched ON and OFF very quickly.

- At a low duty cycle, the LED is ON for a smaller portion of each cycle.
- At a higher duty cycle, the LED is ON for a larger portion of each cycle.
- At 100% duty cycle, the LED remains ON continuously.

Because the switching happens quickly, the human eye perceives different brightness levels.

## 5. Components Required

| Component | Quantity |
|---|---:|
| Raspberry Pi | 1 |
| LED | 1 |
| 220Ω or 330Ω resistor | 1 |
| Breadboard | 1 |
| Jumper wires | As required |

## 6. Circuit Connections

We will use BCM GPIO17.

| LED connection | Raspberry Pi connection |
|---|---|
| Anode (long leg) | GPIO17 through a resistor |
| Cathode (short leg) | GND |

GPIO17 corresponds to physical pin 11.

The resistor is required to limit current through the LED.

## 7. Introduction to PWMLED

GPIO Zero provides a class called `PWMLED` for controlling LED brightness.

Example:

```python
from gpiozero import PWMLED

led = PWMLED(17)
```

Unlike the basic `LED` class, `PWMLED` allows us to set the LED brightness using a value between 0 and 1.

| Value | Brightness setting |
|---|---|
| `0` | Off |
| `0.25` | 25% |
| `0.5` | 50% |
| `0.75` | 75% |
| `1` | Full brightness |

## 8. Python Program: Different Brightness Levels

Create a file named `pwm_led.py`.

```python
from gpiozero import PWMLED
from time import sleep

led = PWMLED(17)

while True:
    led.value = 0.2
    sleep(1)

    led.value = 0.5
    sleep(1)

    led.value = 1.0
    sleep(1)

    led.value = 0
    sleep(1)
```

## 9. Understanding the Code

### Import PWMLED

```python
from gpiozero import PWMLED
```

Imports the PWMLED class.

### Create the LED object

```python
led = PWMLED(17)
```

Creates a PWM-controlled LED on BCM GPIO17.

### Set brightness

```python
led.value = 0.5
```

Sets the PWM duty cycle to approximately 50%.

### Introduce a delay

```python
sleep(1)
```

Waits for one second before changing the brightness again.

## 10. Practical Extension: LED Fading

Now let's gradually increase and decrease LED brightness.

```python
from gpiozero import PWMLED
from time import sleep

led = PWMLED(17)

while True:
    for brightness in range(0, 101, 5):
        led.value = brightness / 100
        sleep(0.05)

    for brightness in range(100, -1, -5):
        led.value = brightness / 100
        sleep(0.05)
```

### Expected Behaviour

- The LED gradually becomes brighter.
- It reaches full brightness.
- It gradually becomes dimmer.
- The process repeats.

## 11. Troubleshooting

| Problem | Possible solution |
|---|---|
| LED does not turn on | Check LED polarity and wiring |
| Brightness does not change | Confirm you are using `PWMLED` |
| LED brightness is too low | Check the LED and resistor values |
| GPIO error | Check pin availability and GPIO Zero configuration |

## 12. Challenge Activity

1. Change the brightness levels to 10%, 30%, 60% and 100%.
2. Create a slow fading effect.
3. Make the LED fade in and out using different delay values.
4. Try changing the PWM frequency and observe the effect, if your GPIO Zero setup supports it.

## 13. Key Takeaways

- PWM stands for Pulse Width Modulation.
- Duty cycle controls the proportion of time the signal is ON.
- PWM can be used to control LED brightness.
- GPIO Zero provides the `PWMLED` class.
- The `value` property ranges from 0 to 1.

**Congratulations! You have completed Module 1: GPIO Zero Fundamentals.**

You are now ready to explore electronic components and build your first robotics projects.
