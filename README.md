# IIOT


An ultrasonic sensor (like HC-SR04) measures distance using **sound waves**.

1. The sensor sends out **ultrasonic waves** (high-frequency sound, ~40 kHz).
2. These waves travel through air and hit an object.
3. The waves reflect back to the sensor.
4. The sensor measures the **time taken** for the wave to return.
5. Distance is calculated using:

d = v*t/2

Where:
d = distance
v = speed of sound (~343 m/s)
t = time taken

Division by 2 is done because the wave travels **to the object and back**.

---

## **Specifications of Ultrasonic Sensor (HC-SR04)**

* Operating Voltage: 5V
* Operating Current: ~15 mA
* Frequency: 40 kHz
* Range: 2 cm to 400 cm
* Accuracy: ±3 mm
* Measuring Angle: ~15°
* Trigger Input Pulse: 10 microseconds
* Output Signal: Digital pulse (Echo pin)
* Pins: VCC, GND, TRIG, ECHO

---

## **Specifications of Raspberry Pi 4 Model B**

* Processor: Quad-core ARM Cortex-A72 (1.5 GHz)
* RAM: 2GB / 4GB / 8GB options
* GPIO Pins: 40 pins (3.3V logic)
* USB Ports: 2 × USB 3.0, 2 × USB 2.0
* Power Supply: 5V (via USB-C)
* Wi-Fi: 802.11ac (built-in)
* Bluetooth: 5.0
* Ethernet: Gigabit Ethernet
* Operating System: Linux-based (Raspberry Pi OS)
* Storage: microSD card

---

## **Simple Summary**

* Ultrasonic sensor uses **echo of sound** to measure distance
* Raspberry Pi reads the **time signal** and calculates distance
* Important: Sensor works at **5V**, Pi GPIO works at **3.3V** → use voltage divider

---

If you want, I can also convert this into **exam-ready answer format (with diagram)** or **PDF notes** 👍
