# 👥 Group Members

| Student Name | Role / Responsibility |
|---|---|
| Redah Gamieldien | Testing Lead |
| Lyle Solomons | Software Lead |
| Qaasim Isaacs | Hardware Lead |
| Ethan Williams | Documentation Lead |

---

## 💡 Project Idea & Problem Statement
## Problem Statement

Currently, student identification cards are mainly used only to access campus facilities. However, classroom attendance is still recorded manually using attendance sheets.

This creates several problems:

- Attendance sheets can be lost or damaged  
- Students may sign attendance for absent friends  
- Manual attendance recording is time consuming  
- Attendance tracking becomes unreliable and prone to human error  

---

## Proposed Solution

We developed a **Smart Attendance System** using RFID and ESP32 with real-time monitoring.

### System Flow:
- RFID card is scanned
- ESP32 reads UID
- Attendance is recorded automatically
- LED + buzzer provide feedback
- Data is sent via Wi-Fi
- GitHub stores project documentation

---

## Objectives

1. Automate attendance tracking  
2. Improve accuracy and efficiency  
3. Prevent proxy attendance  
4. Demonstrate IoT application in education  

---


# 🏗️ System Architecture & Design

![System Architecture](image/System_Architecture.png)

## Design Decisions

- ESP32 chosen for Wi-Fi + processing power  
- MFRC522 used for RFID scanning  
- SPI communication ensures fast data transfer  
- LEDs + buzzer for feedback system  
- GitHub for version control  
- Designed for scalability  
---

## 🔧 Hardware Components

| Component | Description | Quantity | Purpose |
|---|---|---|---|
| ESP32 | Microcontroller | 1 | Main controller |
| MFRC522 | RFID reader | 1 | Reads student cards |
| RFID Tags | Student cards | Multiple | Identification |
| Green LED | Indicator | 1 | Success signal |
| Red LED | Indicator | 1 | Failure signal |
| Buzzer | Sound output | 1 | Audio feedback |
| 220Ω Resistors | Protection | 2 | LED safety |
| Jumper Wires | Connections | Multiple | Wiring |
| Breadboard | Prototype | 1 | Testing |
| Enclosure | Housing | 1 | Final casing |

---

## 💻 Software & Technologies

| Tool | Purpose |
|---|---|
| Arduino IDE | Programming ESP32 |
| GitHub | Version control |
| Wokwi | Simulation |
| C++ | Firmware language |
| ESP32 Wi-Fi Library | Connectivity |
| MFRC522 Library | RFID communication |

---

## 🔌 Circuit Diagram / Wiring

![Circuit Diagram](image/Circuit_Diagram.jpeg)

| Component Pin | ESP32 Pin |
|---|---|
| SDA | GPIO 5 |
| SCK | GPIO 18 |
| MOSI | GPIO 23 |
| MISO | GPIO 19 |
| RST | GPIO 22 |
| VCC | 3.3V |
| GND | GND |
| Green LED | GPIO 13 |
| Red LED | GPIO 12 |
| Buzzer | GPIO 14 |
---

# Key Functions

| Function Name | Description |
|---|---|
| `setup()` | Initializes hardware, WiFi, RFID, and Firebase |
| `loop()` | Handles RFID scanning and attendance logging |
| `getTimeStamp()` | Retrieves current date and time |
| `instantBeep()` | Plays short buzzer sound |
| `accessGranted()` | Indicates successful scan |
| `accessDenied()` | Indicates failed scan |
| `http.GET()` | Retrieves data from Firebase |
| `http.POST()` | Sends attendance data to Firebase |
| `deserializeJson()` | Parses Firebase JSON data |
| `rfid.PICC_HaltA()` | Stops RFID communication after scan |

---

## 🏭 Build Process (with photos)

## Step 1: Install Esp32 to breadboard
![Step 1](image/1.jpeg)

## Step 2:  Install MFRC522 RFID Scanner to the breadboard
![Step 2](image/2.jpeg)

## Step 3:Connect Esp32 to MFRC522 RFID scanner
![Step 3](image/3.jpeg)

## Step 4: Install the Green LED with the appropriate Ohms resistor to the breadboard
![Step 4](image/4.jpeg)

## Step 5: Install the Red LED with the appropriate Ohms resistor to the breadboard
![Step 5](image/5.jpeg)

## Step 6: Mount the Buzzer into the breadboard
![Step 6](image/6.jpeg)

## Step 7: Set up database 
![Step 7](image/7.jpeg)

## Step 8: Ensure Database is capable of logging data
![Step 8](image/8.jpeg)

## Step 9: Basic UI to test if the front-end interacts with the backend
![Step 9](image/9.jpeg)

## Step 10: Final UI Dashboard
![Step 10](image/10.1.jpeg)
![Step 10](image/10.2.jpeg)
![Step 10](image/10.3.jpeg)
![Step 10](image/10.4.jpeg)
## Step 11: Housing Unit Components
![Step 11](image/11.jpeg)

## Step 12: Complete Housing Unit Assembly
![Step 12](image/12.jpeg)
![Step 12](image/13.jpeg)

---
