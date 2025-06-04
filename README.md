# Dashboard Design Using CAN Bus

## 📌 Project Overview

This embedded system project demonstrates a **multi-node CAN-based communication system** designed to simulate a vehicle dashboard. It reads and displays **engine temperature**, **fuel level**, and handles **left/right indicators**, using **CAN protocol** for inter-node communication.

## 🎯 Objective

To display:
- **Engine temperature**
- **Fuel percentage**
- **Left and right indicator signals**

...using **CAN Bus** across distributed microcontroller nodes.

---

## 🧠 Key Concepts Covered

- Embedded C Programming
- LPC2129 Microcontroller Architecture
- ADC (Analog-to-Digital Converter) Interfacing
- CAN (Controller Area Network) Protocol
- Real-Time Clock (RTC) usage
- DS18B20 Temperature Sensor Interfacing
- LCD Display Control
- External Interrupts (EINT0 & EINT1)

---

## 🔧 Hardware Requirements

- LPC2129 Microcontroller
- MCP2551 CAN Transceiver
- DS18B20 Temperature Sensor
- Fuel Gauge
- LCD Display
- LEDs (for indicators)
- Switches
- USB to UART Converter

---

## 💻 Software Requirements

- Embedded C
- Keil µVision (C Compiler for ARM)
- Flash Magic (Flashing Tool)

---

## 🔄 Project Structure

### 1. **MAIN NODE**
- Reads engine temperature using DS18B20
- Displays temperature and RTC (Time, Date, Day) on LCD
- Handles left/right indicators via external interrupts
- Receives fuel percentage from FUEL NODE and displays on LCD
- Sends indicator status to INDICATOR NODE via CAN

### 2. **FUEL NODE**
- Reads analog fuel sensor via on-chip ADC
- Sends fuel percentage to MAIN NODE via CAN

### 3. **INDICATOR NODE**
- Listens for indicator status from MAIN NODE
- Controls left/right LEDs accordingly

---

## 🧪 Testing Sequence

1. Test LCD display output (characters, integers, strings)
2. Test ADC with a potentiometer
3. Read and display fuel level from fuel gauge
4. Interface DS18B20 and display temperature
5. Check external interrupts EINT0 and EINT1
6. Interface and verify RTC
7. Test CAN communication with test code
8. Integrate all modules for each node

---

## 📁 File Structure

- `MAIN_NODE.c` – Main node logic
- `FUEL_NODE.c` – Fuel sensor node logic
- `INDICATOR_NODE.c` – Indicator signal node
- `adc_driver.c`, `can.c`, `rtc.c`, etc. – Supporting drivers
- `lcd.c`, `ds18b20.c`, `interrupt.c` – Peripheral interfaces

---

## ✅ Final Output

Once each module works individually, integrate the system to:
- Continuously monitor engine temperature and fuel level
- Show readings on LCD
- Use CAN protocol to coordinate indicator signals
- Blink indicator LEDs based on driver input

---

## 📃 License

This project is for academic and learning purposes. Modify and distribute freely.

## 👨‍💻 Author

Developed by Goutham Kumar 
For Final Year Embedded Systems Project  
Guided by [Instructor or Institution Name if needed]

---

**ALL THE BEST 👍**
