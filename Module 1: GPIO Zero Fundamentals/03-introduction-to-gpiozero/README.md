# Lesson 03: Introduction to GPIO Zero

## 1. Learning Objective

In this lesson, you will learn about the GPIO Zero Python library and how it simplifies controlling electronic components using the Raspberry Pi.

By the end of this lesson, you will be able to:

- Explain what GPIO Zero is.
- Install and import the library.
- Create a basic LED object.
- Understand common GPIO Zero methods.
- Run a simple Python program using Thonny.

## 2. What is GPIO Zero?

GPIO Zero is a Python library that makes it easier to control electronic components connected to Raspberry Pi GPIO pins.

Instead of writing low-level instructions to control individual pins, GPIO Zero provides simple Python objects for common components.

For example:

```python 
from gpiozero import LED

led = LED(17)
led.on()
```

This program creates an LED object on BCM GPIO17 and turns it on.

## 3. Installing GPIO Zero

Open the Raspberry Pi terminal and run:

```bash
sudo apt update
sudo apt install python3-gpiozero
```

To verify the installation:

```bash
python3 -c "import gpiozero; print('GPIO Zero installed successfully')"
```

If the message appears without an error, the library is available to Python.

## 4. Importing GPIO Zero

To use a component, import its corresponding class.

For example:

```python
from gpiozero import LED
```

Here:

- `from gpiozero` identifies the library.
- `import LED` imports the LED class.

GPIO Zero provides classes for different components, including:

| Component | GPIO Zero class |
|---|---|
| LED | `LED` |
| PWM LED | `PWMLED` |
| Push button | `Button` |
| Active buzzer | `Buzzer` |
| Servo motor | `Servo` |

## 5. Creating an LED Object

```python
from gpiozero import LED

led = LED(17)
```

The `LED(17)` instruction creates an LED object connected to BCM GPIO17.

Remember that the LED must also be connected correctly using a current-limiting resistor and GND.

## 6. Common GPIO Zero Methods

| Method or property | Purpose |
|---|---|
| `led.on()` | Turns the LED on |
| `led.off()` | Turns the LED off |
| `led.toggle()` | Changes the LED state |
| `led.blink()` | Makes the LED blink |
| `led.close()` | Releases the GPIO resource |
| `led.value` | Reads or sets the LED state |

## 7. First GPIO Zero Program

```python
from gpiozero import LED
from time import sleep

led = LED(17)

led.on()
sleep(2)

led.off()
sleep(2)

led.close()
```

### Code Explanation

1. Import the LED class.
2. Import `sleep` to create a time delay.
3. Create an LED object on BCM GPIO17.
4. Turn the LED on.
5. Wait for two seconds.
6. Turn the LED off.
7. Release the GPIO resource.

## 8. Running the Program in Thonny

1. Open Thonny IDE.
2. Create a new Python file.
3. Copy the program.
4. Save it as `gpiozero_intro.py`.
5. Connect the LED circuit.
6. Run the program.
7. Observe the LED.

## 9. Quick Knowledge Check

1. What is GPIO Zero?
2. How do you import the LED class?
3. What does `LED(17)` mean?
4. Which method turns an LED off?
5. Why do we use `sleep()`?

## 10. Key Takeaways

- GPIO Zero simplifies Raspberry Pi hardware programming.
- Components are represented using Python objects.
- GPIO Zero uses BCM numbering by default.
- Different components have different classes and methods.
- Thonny can be used to write and execute GPIO Zero programs.

**Next Lesson:** LED Blinking.
