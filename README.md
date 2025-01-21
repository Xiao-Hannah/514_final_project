
# 514_final_project
# Project Title: Smart Cat Litter Box

## Project Overview

The sensing device includes a dust-proof enclosure with a load cell (pressure sensor) to measure waste levels, and I might add an air quality sensor to detect odors like ammonia to enhance its functionality. The display device uses a stepper motor-driven gauge needle to visually show cleanliness status (Clean, Needs Attention, Dirty), and a red LED lights up when it’s time to clean.

---

## Sensor Device
The sensor device consists of a load cell (5 kg) connected to an HX711 amplifier module to measure the weight of the litter box contents. The load cell detects changes in pressure caused by waste and sends analog signals to the HX711, which converts them into digital data. This data is processed by the microcontroller (e.g., ESP32 or Arduino), which calculates the cleanliness status and transmits it via Bluetooth to the display system.

![Sensor Device](images/Sensor%20Device.jpg)  
Detailed sketch of the sensor device.

---

## Display Device
The display device features a stepper motor-driven gauge needle that visually indicates the cleanliness status (Clean, Needs Attention, Dirty) and an LED that lights up when the litter box requires cleaning. The TB6612 motor driver receives control signals from the display microcontroller to drive the stepper motor. Additionally, the microcontroller directly controls the LED based on the cleanliness data received via Bluetooth from the sensor microcontroller.

![Display Device](images/Display%20Device.jpg)  
Detailed sketch of the display device.

---

## Communication and System Workflow

### Communication Diagram
This figure shows how the sensor device and display device communicate via Bluetooth. The sensor device collects data from the load cell, processes it with the microcontroller, and sends the cleanliness status wirelessly to the display device.

![Flow Diagram](images/Flow%20Diagram.jpg)  
Diagram showing communication between the sensor and display devices.

### Circuit Diagram
This detailed diagram shows how all components are physically connected. The load cell is wired to the HX711, which connects to the microcontroller. The display device includes connections between the microcontroller, motor driver, stepper motor, and LED.

![Circuit Diagram](images/Circuit.jpg)  
Detailed circuit diagram of the Smart Pet Litter Box.
