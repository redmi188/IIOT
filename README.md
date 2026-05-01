# IIOT


---

#  **HC-SR04 Ultrasonic Sensor – Working Principle**

##  **Concept / Theory**

The HC-SR04 ultrasonic sensor measures distance using **sound waves**.

### ⚙️ Working Steps:

1. A **10 microsecond pulse** is sent to the **Trigger pin**
2. Sensor sends **8 ultrasonic pulses at 40 kHz**
3. These sound waves travel through air
4. If an object is present:

   * Waves reflect back to sensor
   * Echo pin becomes HIGH and then LOW
5. If no object is detected:

   * Echo times out after **38 ms**
   * Indicates no obstacle in range

---

## 🔁 **Echo Signal Behavior**

| Condition       | Echo Output                 |
| --------------- | --------------------------- |
| Object detected | Pulse width 150 µs to 25 ms |
| No object       | 38 ms timeout               |

---

## ⚙️ **Distance Formula**

d = (t × 0.034) / 2

Where:

* d = distance in cm
* t = time (microseconds converted to duration)
* 0.034 = speed of sound in cm/µs
* divide by 2 = forward + return travel

---

# 🔌 **Connections (Arduino + HC-SR04 + Devices)**

## 📍 Ultrasonic Sensor

| HC-SR04 Pin | Arduino Pin |
| ----------- | ----------- |
| VCC         | 5V          |
| GND         | GND         |
| TRIG        | Pin 11      |
| ECHO        | Pin 12      |

---

## 📍 Additional Components

| Component | Arduino Pin |
| --------- | ----------- |
| LED       | Pin 2       |
| Buzzer    | Pin 4       |
| Motor +   | Pin 3       |
| Motor -   | Pin 6       |

---

# ⚙️ **Working Summary**

* Arduino sends trigger pulse
* Sensor emits ultrasonic waves
* Waves reflect from object
* Echo pulse width = distance
* Arduino calculates distance using time

---

# ⚠️ **Important Notes**

* Minimum range: ~2 cm
* Maximum range: ~400 cm
* Works on 5V supply
* Echo pin gives 5V → safe for Arduino
* Use stable mounting for accuracy

---

