# IIOT P3

| Pin | Connect To | Physical Pin |
| --- | ---------- | ------------ |
| VCC | 5V         | Pin 2        |
| GND | GND        | Pin 6        |
| OUT | GPIO24     | Pin 18       |

| Pin | Connect To | Physical Pin |
| --- | ---------- | ------------ |
| +   | GPIO20     | Pin 38       |
| –   | GND        | Pin 6        |


## **Concept / Theory: Working of PIR Sensor**

A PIR (Passive Infrared) sensor detects **motion by sensing changes in infrared (IR) radiation**.

* All objects with temperature above absolute zero emit **infrared radiation**
* Human body emits a strong amount of IR radiation
* PIR sensor does **not emit anything** → it is *passive*

### **How it works step-by-step:**

1. The sensor has a **pyroelectric material** that detects IR radiation
2. In normal condition, it senses a **constant IR level** from surroundings
3. When a person moves:

   * The IR pattern in front of the sensor changes
   * This change is detected by the sensor
4. The sensor converts this change into an **electrical signal**
5. Output becomes:

   * HIGH (1) → Motion detected
   * LOW (0) → No motion

### **Important Concept**

* PIR detects **change in IR**, not constant temperature
* That’s why it detects **motion**, not stationary objects


## **Internal Components (Basic Idea)**

* Pyroelectric sensor (core detector)
* Fresnel lens (focuses IR rays)
* Amplifier circuit
* Comparator circuit


## **Specifications of PIR Sensor (HC-SR501)**

* Operating Voltage: 4.5V to 20V (typically 5V)
* Output Voltage: 3.3V (digital HIGH)
* Operating Current: ~50 µA (very low power)


### **Detection Characteristics**

* Detection Range: 3 to 7 meters (adjustable)
* Detection Angle: ~120°
* Sensitivity: Adjustable using onboard potentiometer


### **Timing Features**

* Delay Time: Adjustable (from ~5 seconds to ~5 minutes)
* Trigger Modes:

  * Single Trigger (Non-repeatable)
  * Repeat Trigger (Keeps output HIGH if motion continues)


### **Output Details**

* Output Type: Digital (HIGH/LOW)
* HIGH → Motion detected
* LOW → No motion

## **Advantages**

* Low power consumption
* Easy to interface with microcontrollers
* Good for motion detection systems
* Inexpensive

## **Limitations**

* Cannot detect stationary objects
* Affected by temperature changes
* May give false triggers (heat sources, sunlight)

