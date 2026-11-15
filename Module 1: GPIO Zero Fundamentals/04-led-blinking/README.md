# Lesson 04: LED Blinking

## 1. Learning Objective

In this lesson, you will build your first practical Raspberry Pi GPIO project: a blinking LED.

By the end of this lesson, you will be able to:

- Connect an LED to a Raspberry Pi.
- Understand LED polarity.
- Use a resistor to limit current.
- Control an LED using GPIO Zero.
- Change the blinking interval.

## 2. What is an LED?

LED stands for Light Emitting Diode.

An LED is an electronic component that produces light when current flows through it in the correct direction.

An LED has two terminals:

- Anode: Positive side, usually the longer leg.
- Cathode: Negative side, usually the shorter leg.

An LED must be connected with the correct polarity.

## 3. Components Required

| Component | Quantity |
|---|---:|
| Raspberry Pi | 1 |
| Red LED | 1 |
| 220Ω or 330Ω resistor | 1 |
| Breadboard | 1 |
| Jumper wires | As required |

## 4. Circuit Connections

We will use BCM GPIO17.

| LED connection | Raspberry Pi connection |
|---|---|
| Anode (long leg) | GPIO17 through a resistor |
| Cathode (short leg) | GND |

GPIO17 corresponds to physical pin 11.

GND can be connected to physical pin 6.

### Circuit arrangement

```text
GPIO17 (Physical pin 11)
          |
       Resistor
          |
       LED Anode
       LED Cathode
          |
GND (Physical pin 6)
```

The resistor can be placed before or after the LED in this series circuit.

## 5. Python Program

Create a file named `blink_led.py`.

```python
from gpiozero import LED
from time import sleep

led = LED(17)

while True:
    led.on()
    sleep(1)

    led.off()
    sleep(1)
```

## 6. Understanding the Code

### Import the LED class

```python
from gpiozero import LED
```

Imports the LED class from GPIO Zero.

### Import sleep

```python
from time import sleep
```

Allows us to introduce a time delay.

### Create the LED object

```python
led = LED(17)
```

Defines an LED connected to BCM GPIO17.

### Turn the LED on

```python
led.on()
```

Sets the output to turn on the LED.

### Introduce a delay

```python
sleep(1)
```

Waits for one second.

### Turn the LED off

```python
led.off()
```

Turns the LED off.

### Repeat the process

```python
while True:
```

Repeats the instructions continuously until the program is stopped.

## 7. Expected Output

When you run the program:

- The LED turns on for one second.
- The LED turns off for one second.
- The process repeats continuously.

Stop the program using the Stop button in Thonny or Ctrl+C in the terminal.

## 8. Experiment with Different Speeds

Try changing the delay:

```python
sleep(0.5)
```

The LED will blink faster.

```python
sleep(2)
```

The LED will blink more slowly.

## 9. Alternative: Using the blink() Method

GPIO Zero also provides a built-in blink method.

```python
from gpiozero import LED

led = LED(17)

led.blink(on_time=1, off_time=1)
```

This automatically blinks the LED with one-second ON and OFF intervals.

## 10. Troubleshooting

| Problem | Possible solution |
|---|---|
| LED does not turn on | Check LED polarity |
| LED does not blink | Check the GPIO connection |
| LED remains off | Check the resistor and GND connections |
| Python import error | Verify GPIO Zero installation |
| Program reports GPIO errors | Check whether another program is using the pin |

## 11. Challenge Activity

Try these activities:

1. Make the LED blink every half-second.
2. Make the LED turn on for three seconds and off for one second.
3. Use the `blink()` method to create a different blinking pattern.

## 12. Key Takeaways

- An LED has an anode and cathode.
- A current-limiting resistor is required.
- GPIO Zero makes LED control simple.
- The `on()` and `off()` methods control the LED.
- The `sleep()` function controls timing.

**Next Lesson:** Push-button Input.
