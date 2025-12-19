# Load Cell Data Acquisition System using ESP32 and HX711

## 📌 Project Overview
This project implements a **data acquisition system (DAQ)** using a **load cell sensor** and a **16-bit HX711 analog-to-digital converter**.  
The system measures varying loads, displays the readings on the **serial monitor**, and uploads the data to **ThingSpeak** for real-time graphical visualization.

The complete hardware schematic was designed using **KiCad**, and the firmware was developed using the **Arduino IDE on macOS**.

---

## 🎯 Objectives
- Design a load cell based data acquisition system
- Use a **16-bit ADC (HX711)** for accurate measurement
- Display sensor data on the serial monitor
- Upload and visualize data on **ThingSpeak**
- Observe and analyze load variation at different timestamps

---

## 🧩 Components Used
- ESP32-C3 Development Board
- Load Cell (4-wire strain gauge)
- HX711 16-bit ADC Module
- Connecting wires
- USB cable (for programming and serial monitoring)

---

## 🛠️ Hardware Design
The circuit schematic was created using **KiCad**.  
The load cell output is connected to the HX711, which amplifies and converts the analog signal into digital form.  
The ESP32 reads the digital data from the HX711 using GPIO pins.

### Key Connections
| HX711 Pin | ESP32-C3 Pin |
|---------|--------------|
| VCC | 3.3V |
| GND | GND |
| DOUT | GPIO 18 |
| PD_SCK | GPIO 19 |

The RX/TX pins of the ESP32 are kept free for serial communication.

---

## 💻 Software Used
- **KiCad** – Circuit design
- **Arduino IDE (macOS)** – Firmware development
- **HX711 Library** – Load cell data acquisition
- **ThingSpeak Library** – Cloud data visualization
- **GitHub** – Version control and project hosting

---

## ⚙️ Working Principle
1. The load cell produces a small analog voltage proportional to the applied load.
2. The HX711 amplifies and converts this signal into a 16-bit digital value.
3. The ESP32 reads the digital data from the HX711.
4. The measured load is displayed on the serial monitor.
5. The data is uploaded to ThingSpeak using WiFi.
6. ThingSpeak plots the load data against time for visualization.

---

## Author

SRIKARAN MULUKA

---

## 📁 Repository Structure
