# IIOT


---

# 🌐 **Node-RED for IoT (Weather Monitoring System)**

---

## 📘 **Concept / Theory**

---

# 🌐 Node-RED – IoT Visual Programming Tool

Node-RED is a **visual programming tool** used for building IoT applications without writing complex code. It allows users to connect hardware devices, APIs, and online services using a **flow-based editor**.

It is widely used in IoT systems to reduce development time and simplify integration between devices and cloud services.

---

##  What is Node-RED?

Node-RED is:

* Built on **Node.js**
* Developed using **JavaScript**
* Maintained by IBM Emerging Technology team
* Open-source and free to use

It provides a **browser-based flow editor**, where you can drag, drop, and connect nodes to create applications.

---

##  Why Node-RED?

Node-RED is popular because it:

*  Open-source and free
*  Cross-platform (Windows, Linux, Raspberry Pi)
*  Visual programming (no heavy coding required)
*  Cloud-supported (IBM Cloud, etc.)
*  Supports IoT protocols (MQTT, HTTP, etc.)
*  Enables real-time automation
*  Reduces IoT development time (“fast go-to-market”)

---

##  Working Principle

Node-RED works on a **flow-based programming model**:

1. Nodes are placed in a workspace
2. Nodes are connected to form a flow
3. Data flows from one node to another
4. Each node performs a specific function

---

##  Types of Nodes in Node-RED

###  Input Nodes

Used to receive data from external sources:

* HTTP input
* IBM IoT input
* MQTT input (commonly used in IoT systems)

---

###  Function Nodes

Used for processing data:

* **Function Node** → Executes custom JavaScript logic
* **Switch Node** → Routes data based on conditions

---

###  Output Nodes

Used to send data to external systems:

* HTTP Response
* IBM IoT output
* Twilio (send SMS alerts )

---

###  Utility Nodes

* **Inject Node**

  * Generates messages manually or automatically
  * Used to start flows

* **Debug Node**

  * Displays message data in debug panel
  * Helps in testing and troubleshooting

---


---

# 💻 **Node-RED Installation Steps**

## 1️⃣ Install Node.js

Download from:
👉 [https://nodejs.org/en/](https://nodejs.org/en/)

---

## 2️⃣ Install Node-RED

Open command prompt:

```bash
npm install -g node-red
```

---

## 3️⃣ Run Node-RED

```bash
node-red
```

Then open browser:

```
http://127.0.0.1:1880/
```

---

## 4️⃣ Install Required Nodes

```bash
npm install node-red-node-arduino
npm install node-red-node-serialport
npm install node-red-dashboard
```

---

# 🔧 **Node-RED Flow Setup**

### Step 1:

Drag **Serial Input node**

---

### Step 2:

Add **Function nodes (2)**:

* Temperature function
* Humidity function

---

## 🌡️ Temperature Function Code

```javascript
var temp1 = msg.payload[6];
var temp2 = msg.payload[7];
var temp3 = msg.payload[9];
var temp4 = msg.payload[10];

var result = (temp1*10) + (temp2*1) + (temp3*0.1) + (temp4*0.01);

msg.payload = result;
return msg;
```

---

## 💧 Humidity Function Code

```javascript
var hum1 = msg.payload[0];
var hum2 = msg.payload[1];
var hum3 = msg.payload[3];
var hum4 = msg.payload[4];

var result = (hum1*10) + (hum2*1) + (hum3*0.1) + (hum4*0.01);

msg.payload = result;
return msg;
```

---

## 🐞 Step 3: Debug Nodes

* Add 2 Debug nodes
* One for temperature
* One for humidity

---

## 📊 Step 4: Dashboard Nodes

Add:

* Gauge (Temperature)
* Gauge (Humidity)

---

# 🔁 **Final Flow Working**

1. Sensor sends data via Serial
2. Node-RED reads data
3. Function nodes separate temperature & humidity
4. Debug shows raw values
5. Dashboard displays live readings

---
