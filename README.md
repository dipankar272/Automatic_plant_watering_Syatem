Automatic Plant Watering System using Arduino
Meet Sprouter – the modern indoor planter that automatically waters your plants, herbs, and vegetables, revolutionizing your gardening experience.

How It Works
Sprouter has an integrated water reservoir that pumps water to keep the soil hydrated. A soil moisture sensor periodically measures soil moisture levels, regulating the water flow. If the soil is too dry, the water pump automatically switches ON and turns OFF once the desired moisture level is reached.

If you tend to underwater your plants, Sprouter ensures they get just the right amount of water. If you overwater to compensate for neglect, it prevents drowning your plants or seeds.

Sprouter’s water reservoir holds around 500 ml (17 fl oz), allowing you to neglect your plants for up to a month before refilling.



The optional Bluetooth feature allows manual control of the water pump via a smartphone app.

Electronic Design


Components Required:
Arduino UNO
5V Relay Module
Water Pump
Tube
Soil Moisture Sensor
Jumper Wires
LCD Display (JHD 162A)
9V Battery
Tools:
Soldering Iron
Working of Key Components
Pump Control
The MOSFET acts as a switch controlled by the Arduino since the Arduino cannot directly power the DC Pump.
A resistor connected to the gate of the MOSFET prevents damage.
A flyback diode across the pump dissipates stored energy when the pump turns off.
Anode of the diode → Drain of the MOSFET
Cathode of the diode → 9V supply rail
Source of the diode → GND
Moisture Sensor
Feeds an analog value to the Arduino.
The threshold moisture level is user-calibrated depending on the plant type.
Bluetooth Module
Uses serial communication to transfer data between the Arduino and Smartphone.
Software & Bluetooth Configuration
Software
The Moisture Sensor is connected to an analog input pin on the Arduino.
A threshold value determines whether the pump should be ON/OFF.
You can find the source code on GitHub: [Sprouter GitHub/Code] (Insert GitHub link here)
Feel free to modify & contribute to the repository.
Smartphone App & Bluetooth Setup
The HC-05 Bluetooth module allows communication between the smartphone and Arduino.

The app sends values ‘48’ (ON) and ‘49’ (OFF) to control the pump.
How to Connect
Open the Bluetooth app.
Scan for discoverable devices and pair with HC-05.
Click on ‘Switch Mode’ and toggle the button to control the pump wirelessly.
Download the app here:
Bluetooth Serial Monitor

