🔵 Practical 1: Controlling Appliances using Bluetooth
🎯 Aim / Objective

To interface a Bluetooth module (HC-05) with Arduino Uno and design a mobile application using MIT App Inventor to control electrical appliances wirelessly.

🧰 Apparatus / Tools / Equipment / Resources
Arduino Uno
HC-05 Bluetooth Module
LED / Relay Module
Resistor (220Ω)
Jumper Wires
Smartphone (Android)
Arduino IDE
MIT App Inventor
📚 Concept / Theory

Bluetooth is a wireless communication technology used for short-range data transmission between devices. In this experiment, the HC-05 Bluetooth module is used to establish communication between a smartphone and the Arduino Uno.

The HC-05 module communicates with Arduino using serial communication (UART). When a command is sent from the mobile application, it is received by the Bluetooth module and forwarded to the Arduino. Based on the received command, the Arduino performs specific actions such as turning an appliance ON or OFF.

This system demonstrates the basic concept of wireless control and forms the foundation for home automation and IoT-based applications.

🔌 Connections with Arduino
HC-05 VCC is connected to 5V of Arduino
HC-05 GND is connected to GND
HC-05 TX is connected to Arduino RX (Pin 0)
HC-05 RX is connected to Arduino TX (Pin 1)
LED (or relay module) is connected to digital pin 13 through a resistor

Note: RX and TX connections should be removed while uploading the program to avoid communication errors.

⚙️ Procedure
Assemble the circuit by connecting the HC-05 module and LED to the Arduino as per the given connections.
Open Arduino IDE and upload the program to the Arduino board.
Install a Bluetooth control application or create a custom app using MIT App Inventor.
Turn on Bluetooth on the smartphone and pair it with the HC-05 module using the default password (1234 or 0000).
Open the mobile application and connect to the HC-05 device.
Press the ON button to send a command and turn ON the LED/appliance.
Press the OFF button to turn OFF the LED/appliance.
Observe the output and verify proper operation.
🔄 Algorithm
Start the system
Initialize serial communication
Wait for incoming Bluetooth data
Check if data is received
If command corresponds to ON, turn the appliance ON
If command corresponds to OFF, turn the appliance OFF
Repeat the process continuously
🔁 Flow / Block Diagram of MIT App Inventor
Start application
Scan available Bluetooth devices
Select HC-05 from the list
Establish Bluetooth connection
User presses ON/OFF button
Application sends corresponding command
Arduino receives command and controls appliance
📊 Observations
The Bluetooth module successfully paired with the smartphone.
Commands sent from the mobile application were received by the Arduino.
The LED/appliance responded correctly to ON and OFF commands.
Serial monitor displayed the received data correctly.

(Attach screenshot of Serial Monitor showing received characters)

🧮 Calculations

No mathematical calculations are required for this experiment.
However, the baud rate used for serial communication is 9600 bits per second.

✅ Result

The Bluetooth-based appliance control system was successfully implemented. The LED (or connected appliance) was controlled wirelessly using a smartphone application.

(Attach image of mobile application interface)

🧾 Conclusion

The experiment successfully demonstrated wireless control of appliances using Bluetooth communication. The HC-05 module effectively enabled serial communication between the smartphone and Arduino. The mobile application developed using MIT App Inventor provided a user-friendly interface for controlling the appliance.

This practical helps in understanding the fundamentals of embedded systems, wireless communication, and forms a base for advanced applications such as home automation and IoT systems.
