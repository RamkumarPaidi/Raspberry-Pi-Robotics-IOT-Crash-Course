# Lesson 05: Push-button Input

## 1. Learning Objective

In this lesson, you will learn how to read digital input from a push button connected to the Raspberry Pi.

By the end of this lesson, you will be able to:

- Understand how a push button works.
- Connect a push button to a GPIO pin.
- Configure an internal pull-up resistor.
- Detect button presses and releases.
- Control an LED using a push button.

## 2. What is a Push Button?

A push button is an input component used to open or close an electrical connection when pressed.

It allows a user to provide input to an electronic system.

Common applications include:

- Doorbells.
- Reset buttons.
- Control panels.
- Robotics controls.
- User interfaces.

A push button can be used with a Raspberry Pi to detect when someone presses or releases it.

## 3. Components Required

| Component | Quantity |
|---|---:|
| Raspberry Pi | 1 |
| Push button | 1 |
| Breadboard | 1 |
| Jumper wires | As required |
| LED and 220Ω/330Ω resistor | Optional, for the LED activity |

## 4. Circuit Connections

We will use BCM GPIO27.

| Push-button connection | Raspberry Pi connection |
|---|---|
| One terminal | GPIO27 |
| Other terminal | GND |

BCM GPIO27 corresponds to physical pin 13.

Connect the button across the appropriate pair of contacts on the breadboard. Check the button's terminal arrangement before wiring.

### Understanding the Internal Pull-up Resistor

A GPIO input should not be left floating because it may produce unpredictable readings.

GPIO Zero allows us to enable the Raspberry Pi's internal pull-up resistor.

```python
button = Button(27, pull_up=True)
```

With this configuration:

- Button released: input reads HIGH.
- Button pressed: input reads LOW.

GPIO Zero handles this logic and reports the button as pressed or released correctly.

## 5. Python Program: Detect Button Presses

Create a file named `button_input.py`.

```python
from gpiozero import Button
from signal import pause

button = Button(27, pull_up=True)

button.when_pressed = lambda: print("Button pressed!")
button.when_released = lambda: print("Button released!")

pause()
```

## 6. Understanding the Code

### Import the Button class

```python
from gpiozero import Button
```

Imports the Button class from GPIO Zero.

### Create the button object

```python
button = Button(27, pull_up=True)
```

Creates a button object connected to BCM GPIO27 and enables the internal pull-up resistor.

### Detect a button press

```python
button.when_pressed = lambda: print("Button pressed!")
```

Runs the specified action when the button is pressed.

### Detect a button release

```python
button.when_released = lambda: print("Button released!")
```

Runs the specified action when the button is released.

### Keep the program running

```python
pause()
```

Keeps the program running so that it can continue listening for button events.

## 7. Expected Output

When you run the program:

- Press the button.
- The message `Button pressed!` appears.
- Release the button.
- The message `Button released!` appears.

## 8. Practical Extension: Control an LED Using a Button

Connect an LED to BCM GPIO17 through a current-limiting resistor and GND.

Use the following program:

```python
from gpiozero import LED, Button
from signal import pause

led = LED(17)
button = Button(27, pull_up=True)

button.when_pressed = led.on
button.when_released = led.off

pause()
```

### Expected Behaviour

- Press the button: LED turns on.
- Release the button: LED turns off.

## 9. Troubleshooting

| Problem | Possible solution |
|---|---|
| Button does not respond | Check the GPIO27 connection |
| Button always appears pressed | Check button wiring and pull-up configuration |
| Button gives inconsistent readings | Check for loose wires or incorrect button orientation |
| LED does not respond | Check LED wiring and GPIO17 connection |

## 10. Challenge Activity

1. Modify the program to print a custom message when the button is pressed.
2. Make the LED turn on only while the button is pressed.
3. Try controlling two LEDs using different button events.

## 11. Key Takeaways

- A push button provides digital input.
- GPIO Zero provides the `Button` class.
- Internal pull-up resistors help prevent floating input readings.
- `when_pressed` and `when_released` allow event-based control.
- Buttons can be used to control other electronic components.

**Next Lesson:** Buzzer Control.
