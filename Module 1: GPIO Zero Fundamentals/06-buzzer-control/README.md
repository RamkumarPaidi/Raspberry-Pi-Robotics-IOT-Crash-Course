# Lesson 06: Buzzer Control

## 1. Learning Objective

In this lesson, you will learn how to generate sound using a buzzer connected to the Raspberry Pi.

By the end of this lesson, you will be able to:

- Understand what a buzzer is.
- Differentiate between active and passive buzzers.
- Connect a compatible active buzzer.
- Control a buzzer using GPIO Zero.
- Create a simple sound alert.

## 2. What is a Buzzer?

A buzzer is an electronic component that produces sound when it receives an electrical signal.

Buzzers are commonly used in:

- Alarm systems.
- Doorbells.
- Electronic devices.
- Robotics projects.
- Warning and notification systems.

## 3. Types of Buzzers

There are two common types of buzzers.

### Active Buzzer

An active buzzer contains an internal oscillator and produces sound when suitable DC power is applied.

It can be controlled using simple ON and OFF signals.

### Passive Buzzer

A passive buzzer does not contain the same internal tone-generating circuit. It requires a changing electrical signal to produce sound.

Different signal frequencies can be used to generate different tones.

**In this lesson, we will use an active buzzer.**

## 4. Components Required

| Component | Quantity |
|---|---:|
| Raspberry Pi | 1 |
| Compatible active buzzer | 1 |
| Jumper wires | As required |
| Breadboard | 1 |

Use a buzzer that is compatible with the Raspberry Pi's 3.3V GPIO control. Check its voltage and current specifications.

If the buzzer requires more current than a GPIO pin can safely supply, use a suitable transistor driver circuit and an appropriate external supply.

## 5. Circuit Connections

For a suitable low-current, 3.3V-compatible active buzzer:

| Buzzer connection | Raspberry Pi connection |
|---|---|
| Positive (+) | BCM GPIO22 |
| Negative (-) | GND |

BCM GPIO22 corresponds to physical pin 15.

Do not connect a 5V buzzer directly to a GPIO pin. Use an appropriate driver circuit if required by the buzzer specifications.

## 6. Python Program

Create a file named `buzzer.py`.

```python
from gpiozero import Buzzer
from time import sleep

buzzer = Buzzer(22)

buzzer.on()
sleep(1)

buzzer.off()
```

## 7. Understanding the Code

### Import the Buzzer class

```python
from gpiozero import Buzzer
```

Imports the Buzzer class from GPIO Zero.

### Create the buzzer object

```python
buzzer = Buzzer(22)
```

Creates a buzzer object on BCM GPIO22.

### Turn the buzzer on

```python
buzzer.on()
```

Activates the buzzer.

### Wait for one second

```python
sleep(1)
```

Keeps the buzzer active for one second.

### Turn the buzzer off

```python
buzzer.off()
```

Stops the sound.

## 8. Practical Extension: Repeated Sound Alert

Try the following program:

```python
from gpiozero import Buzzer
from time import sleep

buzzer = Buzzer(22)

for i in range(3):
    buzzer.on()
    sleep(0.5)

    buzzer.off()
    sleep(0.5)
```

### Expected Behaviour

The buzzer produces three short beeps.

## 9. Troubleshooting

| Problem | Possible solution |
|---|---|
| No sound | Check buzzer polarity and connections |
| Buzzer does not activate | Confirm it is an active buzzer |
| Buzzer is very quiet | Check the component specifications and supply |
| Raspberry Pi resets or behaves unexpectedly | Check current requirements and use a suitable driver |
| GPIO error | Check whether another program is using the pin |

## 10. Challenge Activity

1. Create a buzzer alert with five short beeps.
2. Change the duration of each beep.
3. Create a simple warning alert using a push button and buzzer together.

## 11. Key Takeaways

- A buzzer is used to generate sound.
- Active buzzers can be controlled with simple ON and OFF signals.
- Passive buzzers require a changing signal.
- GPIO Zero provides the `Buzzer` class.
- Always check the buzzer's voltage and current requirements.

**Next Lesson:** PWM and LED Brightness Control.
