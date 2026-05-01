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

A **stepper motor** is a brushless DC motor that converts electrical pulses into **discrete mechanical motion**. Instead of rotating continuously like a conventional motor, it moves in **fixed angular steps**, allowing precise control over position and speed. The motor can rotate in both **clockwise and counterclockwise directions** depending on the sequence of signals applied.

### **28BYJ-48 Stepper Motor**

The 28BYJ-48 Stepper Motor is a widely used **unipolar stepper motor** operating at 5V. It consists of **four coils**, where:

* One common end is connected to **+5V (Red wire)**
* The other ends are connected to **Blue, Pink, Yellow, and Orange wires**

By energizing these coils in a specific sequence, the motor rotates step-by-step.

#### **Step Angle and Resolution**

### Step Calculations

- In half-step mode:  
  360° / 5.625° = **64 steps**

- In full-step mode:  
  64 / 2 = **32 steps**

The motor includes an internal **gear reduction of 64:1**, meaning the output shaft rotates once when the internal motor rotates 64 times.

- Total steps per revolution:  
  32 × 64 = **2048 steps**

- Step angle (output shaft):  
  360° / 2048 ≈ **0.18° per step**

This high resolution allows **precise angular positioning**.

---

### **ULN2003 Motor Driver**

The ULN2003 Driver Board is used to interface the stepper motor with the microcontroller. Since the motor requires higher current than the controller can supply, the driver acts as a **current amplifier** using Darlington transistor arrays.

* Inputs: IN1, IN2, IN3, IN4
* Connected to GPIO pins of the controller
* Powered using an **external 5V supply**

---

### **ESP8266 NodeMCU**

The ESP8266 NodeMCU is used to control the motor by generating digital signals.

#### **Connections:**

* IN1 → GPIO5
* IN2 → GPIO4
* IN3 → GPIO14
* IN4 → GPIO12

#### **Features of ESP8266:**

* 17 GPIO pins
* SPI communication
* I2C (software-based)
* I2S with DMA
* UART communication
* 10-bit ADC

---

### **Working Principle**

1. The ESP8266 sends HIGH/LOW signals to the driver inputs
2. The driver energizes the motor coils in sequence
3. The rotor aligns with the magnetic field generated
4. Sequential switching causes step-by-step rotation

By controlling:

* **Sequence** → Direction
* **Delay between steps** → Speed

the motor can be precisely controlled.

---

### **Conclusion of Theory**

Thus, by interfacing the stepper motor with the ESP8266 through the ULN2003 driver, **controlled and precise rotational motion** is achieved using programmed step sequences.

---

If you want, I can next format:

* **Procedure (step-by-step for lab)**
* **Circuit diagram explanation**
* **Arduino code with explanation**

