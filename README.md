# Raspberry Pi Robotics & IoT Crash Course

### Learn Python. Explore Electronics. Build Robots. Connect Things.

A beginner-friendly, hands-on learning course designed to introduce students and educators to Raspberry Pi, Python programming, electronics, robotics and Internet of Things (IoT) using GPIO Zero and Flask.

---

## 🚀 About the Project

The **Raspberry Pi Robotics & IoT Crash Course** is a practical learning resource that helps beginners explore physical computing, robotics and IoT through hands-on activities.

Instead of learning programming concepts only through theory, learners will connect electronic components, write Python programs, build working robotics projects and create simple web-based interfaces to interact with Raspberry Pi.

This course follows a learn-by-doing approach, with step-by-step instructions, circuit diagrams, wiring guides, example programs and practical challenges.

## 🎯 Learning Objectives

By completing this course, learners will be able to:

- Understand Raspberry Pi and its GPIO pins.
- Write basic Python programs using GPIO Zero.
- Control LEDs, buttons and buzzers.
- Understand PWM and control component behaviour.
- Interface servo motors and DC motors.
- Understand and use motor drivers.
- Build a simple servo-controlled robotic gripper.
- Build and program a two-wheeled robot.
- Explore basic sensor integration and obstacle detection.
- Understand the fundamentals of Internet of Things (IoT).
- Create simple web applications using Python Flask.
- Control and monitor Raspberry Pi GPIO components through a web browser.

## 🛠️ Hardware Requirements

The course is designed around the following hardware:

- Raspberry Pi 3B+, Raspberry Pi 4 or Raspberry Pi 5.
- MicroSD card with Raspberry Pi OS.
- Breadboard and jumper wires.
- LEDs and resistors.
- Push buttons and buzzer.
- Servo motor (SG90).
- DC gear motors.
- Motor driver (TB6612FNG).
- Ultrasonic distance sensor (HC-SR04).
- Robot chassis and wheels.
- Suitable external power supplies.

Refer to the Bill of Materials for the complete component list.

## 💻 Software Requirements

- Raspberry Pi OS.
- Python 3.
- GPIO Zero library.
- Flask.
- Thonny IDE.
- Git and GitHub.
- A web browser for accessing Flask applications.

## 📚 Course Modules

### Module 1: GPIO Zero Fundamentals

Get started with Raspberry Pi GPIO programming.

**Topics:**

- Introduction to Raspberry Pi GPIO.
- Understanding GPIO pin numbering.
- Introduction to GPIO Zero.
- LED blinking.
- Push-button input.
- Buzzer control.
- PWM and LED brightness control.

### Module 2: Understanding Electronic Components

Explore the electronic components used in robotics projects.

**Components covered:**

- LEDs.
- Push buttons.
- Buzzers.
- Servo motors.
- DC gear motors.
- Motor drivers.
- Ultrasonic sensors.

Each component guide includes its working principle, pin identification, wiring instructions and practical Python examples.

### Module 3: Project – Servo Robotic Gripper

Build a simple robotic gripper controlled using a servo motor.

**Features:**

- Open and close the gripper.
- Control servo positions using Python.
- Understand servo angles and movement.
- Optional push-button control.

### Module 4: Project – Two-Wheeled Robot

Build a basic two-wheeled robotic vehicle using Raspberry Pi.

**Features:**

- Forward and backward movement.
- Left and right turns.
- Motor speed control.
- Stop functionality.
- Optional ultrasonic obstacle detection.

### Module 5: Introduction to IoT Using Python Flask

Understand how Raspberry Pi can communicate with users through a web-based interface.

Learn the fundamentals of IoT by creating simple web applications using Python Flask.

**Topics:**

- Introduction to Internet of Things (IoT).
- Understanding client-server communication.
- Introduction to Flask and web applications.
- Creating a basic Flask web server on Raspberry Pi.
- Understanding routes and HTTP requests.
- Creating a simple HTML-based control interface.
- Connecting Flask applications with GPIO Zero.
- Controlling LEDs through a web browser.
- Displaying sensor information on a web page.
- Accessing the Raspberry Pi web application from another device on the same Wi-Fi network.

**Practical Project: Raspberry Pi Web-Based Device Controller**

Build a simple web application that allows users to:

- Turn an LED ON and OFF through a web browser.
- View the current device status.
- Interact with Raspberry Pi GPIO using a web interface.
- Explore the basic principles of remote device control.

This module introduces the foundation of IoT-based monitoring and control.

## 📂 Repository Structure

```text
raspberry-pi-robotics-iot-crash-course/
│
├── README.md
├── LICENSE
│
├── docs/
│   ├── getting-started.md
│   ├── raspberry-pi-setup.md
│   ├── gpio-pinout.md
│   ├── safety-guidelines.md
│   └── troubleshooting.md
│
├── 01-gpiozero-fundamentals/
│
├── 02-electronic-components/
│
├── 03-project-servo-gripper/
│
├── 04-project-two-wheel-robot/
│
├── 05-iot-with-flask/
│   ├── README.md
│   ├── 01-flask-basics/
│   ├── 02-web-led-control/
│   └── 03-sensor-monitoring/
│
├── 06-resources/
│   ├── bill-of-materials.md
│   ├── gpio-pin-reference.md
│   └── student-challenges.md
│
└── 07-future-extensions/
```

## ⚡ Getting Started

### 1. Set Up Raspberry Pi

Install Raspberry Pi OS and ensure Python 3 and Thonny IDE are available.

### 2. Install GPIO Zero

Open the Raspberry Pi terminal and run:

```bash
sudo apt update
sudo apt install python3-gpiozero
```

### 3. Install Flask

Install Flask using pip:

```bash
python3 -m pip install flask
```

For externally managed Python environments, use a virtual environment rather than installing packages into the system Python environment.

### 4. Clone This Repository

```bash
git clone https://github.com/YOUR-USERNAME/raspberry-pi-robotics-iot-crash-course.git
```

Replace `YOUR-USERNAME` with your GitHub username.

### 5. Open the Project

Open the cloned repository folder and explore the learning modules.

Use Thonny IDE to open and execute the Python programs.

### 6. Start Building

Follow the modules in sequence, understand the circuits, connect the components and experiment with the provided programs.

## ⏱️ Estimated Learning Duration

The initial course is designed for approximately **12–14 hours** of hands-on learning.

| Module | Estimated Duration |
|---|---:|
| GPIO Zero Fundamentals | 3 hours |
| Understanding Electronic Components | 2 hours |
| Servo Robotic Gripper | 2 hours |
| Two-Wheeled Robot | 4 hours |
| Introduction to IoT Using Flask | 2 hours |
| **Total** | **13 hours** |

The duration may vary depending on the learner's experience and hardware setup.

## 🔌 Safety Guidelines

- Disconnect power before modifying circuit connections.
- Always use appropriate current-limiting resistors with LEDs.
- Raspberry Pi GPIO pins use 3.3V logic and are not 5V tolerant.
- Never connect motors directly to Raspberry Pi GPIO pins.
- Use suitable external power supplies for motors and servos.
- Connect grounds appropriately when using external power supplies.
- Use voltage dividers or suitable level shifting for 5V sensor outputs.
- Check component specifications before making connections.
- Do not expose Flask applications directly to the public internet without appropriate security measures.
- Use the Flask control interface only on a trusted local network during initial learning activities.

## 🌱 Future Extensions

The following projects may be added in future versions:

- Line-following robot.
- Bluetooth-controlled robot.
- Wi-Fi-controlled robot.
- Robotic arm.
- IoT-based monitoring and control.
- Sensor-based automation.
- Web-based robotics control.
- Additional Raspberry Pi IoT projects.

These extensions can be explored after completing the initial crash course.

## 🤝 Contributions

Suggestions, improvements and contributions are welcome!

Students, teachers, educators and robotics enthusiasts are encouraged to explore the repository, experiment with the projects and contribute to making this learning resource better.

## 📜 License

The Python source code in this repository is licensed under the MIT License.

Educational documentation, original circuit diagrams and learning materials may be licensed under Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0), where indicated.

Please check the individual licence notices before reusing materials.

---

### Build. Experiment. Learn. Connect.

**Making Robotics and IoT Accessible Through Hands-on Learning.**
