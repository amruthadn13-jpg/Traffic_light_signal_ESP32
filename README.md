# Traffic_light_signal_ESP32
**🚦 ESP32 Traffic Light Control (Wokwi Simulation)**

This project implements a simple traffic light controller using an ESP32 and three LEDs (Red, Yellow, Green).
The behavior follows a fixed time sequence and prints status messages to the Serial Monitor.

The ESP32 used in this project is manufactured by Espressif Systems and the simulation was done using the online simulator Wokwi.

**🧩 Project Overview**

The traffic light works in the following order:

Red ON – Stop

Yellow ON – Ready

Green ON – Go

Each state stays active for a fixed delay and then automatically switches to the next light.

**🔌 Pin Configuration**

The LEDs are connected to the ESP32 GPIO pins as shown below:

LED Color	ESP32 GPIO
Red	GPIO 25
Yellow	GPIO 26
Green	GPIO 27

**🔧 Pin Diagram (Connection)**
Each LED must be connected with a resistor.

GPIO 25  ── 220Ω ──► Red LED  ──► GND
GPIO 26  ── 220Ω ──► Yellow LED ──► GND
GPIO 27  ── 220Ω ──► Green LED ──► GND

Note:
The long leg of the LED (anode) goes to the resistor and GPIO pin.
The short leg (cathode) goes to GND.

**🧠 Code Explanation**

Three macros are used to represent the GPIO pins:

RED → GPIO 25

YELLOW → GPIO 26

GREEN → GPIO 27

In the setup() function:

All three LED pins are configured as output.

Serial communication is started at 9600 baud rate.

In the loop() function, the traffic sequence is executed:

The red LED is turned ON and a message is printed:
“The Red is ON Please Stop!!”

After 5 seconds, the yellow LED is turned ON and a message is printed:
“You Can start Your Vehicle!!”

After 2 seconds, the green LED is turned ON and a message is printed:
“Let's Goo!!!”

After 3 seconds, the loop repeats from the beginning.

The delay() function is used to control how long each signal stays ON.

**🧪 Simulation Platform**

This project was simulated using the Wokwi online simulator.
The simulator allows testing the ESP32 code and circuit connections without physical hardware.

**✅ Features**

Simple traffic light control logic

Uses ESP32 GPIO pins

Serial monitor messages for each signal state

Fully simulated using Wokwi

**📌 Hardware / Tools Used**

ESP32 development board

3 LEDs (Red, Yellow, Green)

3 × 220Ω resistors

Wokwi online simulator


**Author**
Amrutha D N
