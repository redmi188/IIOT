# IIOT

| NodeMCU Pin Label | GPIO Number | Used For |
| ----------------- | ----------- | -------- |
| D1                | GPIO5       | IN1      |
| D2                | GPIO4       | IN2      |
| D5                | GPIO14      | IN3      |
| D6                | GPIO12      | IN4      |


| ULN2003 Driver Pin | Connect To NodeMCU |
| ------------------ | ------------------ |
| IN1                | D1 (GPIO5)         |
| IN2                | D2 (GPIO4)         |
| IN3                | D5 (GPIO14)        |
| IN4                | D6 (GPIO12)        |

| ULN2003 Pin | Connect To                       |
| ----------- | -------------------------------- |
| VCC         | 5V (External supply recommended) |
| GND         | GND (Common with NodeMCU)        |

🔌 Stepper Motor
The 28BYJ-48 motor plugs directly into the ULN2003 board
No manual wiring needed between motor and driver ✔

Here’s a clean, **practical-ready “Concept/Theory” section** for your experiment:

---

## **Concept / Theory**

A **stepper motor** is a type of brushless DC motor that converts electrical pulses into **discrete mechanical movements (steps)**. Unlike conventional motors, it does not rotate continuously but moves in **precise angular increments**, making it ideal for applications requiring accurate position control.

The **28BYJ-48 Stepper Motor** is a commonly used **unipolar stepper motor** that operates on low voltage (5V). It consists of multiple coils arranged in phases. When these coils are energized in a specific sequence, the motor shaft rotates step-by-step. The typical step angle of this motor is **5.625° per step**, combined with an internal gear reduction, resulting in high precision.

Since the stepper motor requires more current than a microcontroller can provide, a driver circuit is used. The **ULN2003 Driver Board** acts as an interface between the motor and the microcontroller. It contains a set of Darlington transistor arrays that amplify the current, allowing safe control of the motor coils.

The **ESP8266 NodeMCU** is a Wi-Fi-enabled microcontroller used to control the motor. It sends digital signals (HIGH/LOW) to the driver board pins. By generating a **step sequence** (e.g., full-step or half-step), the ESP8266 controls:

* Direction of rotation (clockwise or anticlockwise)
* Speed of rotation (by adjusting delay between steps)
* Position of the motor shaft

### **Working Principle**

The rotation of the stepper motor is based on **electromagnetic induction**:

1. Current flows through a coil → creates a magnetic field
2. The rotor aligns with the energized coil
3. Switching the current to the next coil → rotor moves to the next position
4. Repeating this sequence → continuous step-by-step rotation

A common **full-step sequence** is:

* Step 1: Coil A energized
* Step 2: Coil B energized
* Step 3: Coil C energized
* Step 4: Coil D energized

By repeating this sequence, the motor completes one full revolution.

### **Key Advantages**

* Precise position control without feedback
* Simple control using digital signals
* Reliable and repeatable motion

Thus, by interfacing the stepper motor with the ESP8266 via the ULN2003 driver, controlled rotational motion is achieved using programmed step sequences.

