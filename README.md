# IIOT P4

| DHT11 Pin | Connect To | Physical Pin |
| --------- | ---------- | ------------ |
| VCC       | 5V         | Pin 2        |
| GND       | GND        | Pin 6        |
| DATA      | GPIO4      | Pin 7        |


## 🌡️ **Working of DHT11 Sensor**

The DHT11 is a digital sensor used to measure:

* **Temperature (°C)**
* **Humidity (%)**

---

## 🧠 **Basic Working Principle**

The DHT11 has two main sensing parts:

1. **Humidity Sensor**

   * Uses a **capacitive sensing element**
   * It absorbs moisture from air
   * Change in humidity → changes capacitance → converted into electrical signal

2. **Temperature Sensor**

   * Uses an **NTC thermistor**
   * Resistance changes with temperature
   * This change is converted into temperature value

---

## ⚙️ **Step-by-Step Working**

1. **Start Signal**

   * The microcontroller (like Raspberry Pi 4 Model B) sends a **start signal** to DHT11

2. **Sensor Response**

   * DHT11 replies with a response signal to confirm communication

3. **Data Transmission**

   * Sensor sends **40 bits of data** serially

4. **Data Format (40 bits)**

   ```
   8 bits  → Humidity (integer)
   8 bits  → Humidity (decimal)
   8 bits  → Temperature (integer)
   8 bits  → Temperature (decimal)
   8 bits  → Checksum
   ```

5. **Data Processing**

   * Microcontroller reads these bits
   * Converts them into temperature and humidity values

---

## 🔁 **Signal Timing Concept**

* Data is sent as HIGH and LOW pulses
* Length of HIGH pulse determines:

  * Short pulse → 0
  * Long pulse → 1

👉 So communication is **time-based digital signal**

---

## ⚠️ **Important Characteristics**

* Works on **single-wire communication**
* Needs **pull-up resistor (10kΩ)**
* Has **slow response (1–2 seconds delay)**

---

## 🚫 **Limitations**

* Low accuracy compared to advanced sensors
* Slow sampling rate
* Sensitive to noise and wiring issues



sudo apt update
sudo apt install python3-pip python3-venv libgpiod2
mkdir dht_project
cd dht_project

python3 -m venv venv
source venv/bin/activate
(venv) pi@raspberrypi:~/dht_project $

pip install adafruit-circuitpython-dht
pip install RPi.GPIO
