# Solar-Powered-Smart-Irrigation-System
An ESP8266-based solar-powered smart irrigation system with real-time environmental monitoring, Firebase integration, and automatic irrigation control.

![ESP8266](https://img.shields.io/badge/ESP8266-IoT-blue)
![Blynk](https://img.shields.io/badge/Blynk-IoT-green)
![Firebase](https://img.shields.io/badge/Firebase-Realtime%20Database-orange)
![Arduino](https://img.shields.io/badge/Arduino-IDE-00979D)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

> An ESP8266-based solar-powered smart irrigation system featuring automatic watering, environmental monitoring, Firebase cloud storage, and remote control through the Blynk IoT mobile application.

<img width="669" height="431" alt="image" src="https://github.com/user-attachments/assets/54f91281-cff6-49a1-b4b3-ab8ee1f606d4" />

# Table of Contents
1. Introduction
2. Features
3. Hardware
4. System Architecture
5. Software
6. Getting Started
7. Results
8. Future Work
9. Contact
10. License

# 1. Introduction

# 2. Features

🌞 Solar Powered
- Operates entirely from a photovoltaic charging system with rechargeable Li-ion batteries.

💧 Automatic Irrigation
- Automatically activates the water pump based on soil moisture conditions.

📱 Remote Monitoring
- Monitor environmental parameters and manually control the irrigation system using the Blynk IoT mobile application.

☁️ Cloud Data Logging
- Uploads sensor data to Firebase Realtime Database for cloud storage.

🌡️ Environmental Monitoring
- Measures temperature, humidity, light intensity, soil moisture, and CO₂ concentration in real time.

🔋 Battery Monitoring
- Estimates remaining battery voltage using a voltage divider circuit.

🛠️ Open Source
- Complete hardware design, firmware source code, PCB files, and documentation are included.

# 3. Hardware

## 3.1 BOM
| Component | Qty |
| --------- | --- |
| Solar panel 6v 10W | 1 |
| ESP8266 | 1 |
| DHT11 | 1 |
| 18650 | 3 |
| TP4056 | 1 |
| Relay | 1 |
| XL6009 | 2 |
| LCD1602 | 1 |
| Pump | 1 | 

## 3.2 Block Diagram
'''
graph TD
    Power(["<b>Power Block</b><br>(Solar panel, charging circuit, <br>storage battery, boost converter)"])
    Sensor(["<b>Sensor Block</b><br>(DHT11, push button)"])
    Control(["<b>Control Block</b><br>(ESP8266)"])
    UI(["<b>Interaction Block</b><br>(Blynk app)"])
    Output(["<b>Output Block</b><br>(Relay, display)"])

    %% Các đường mũi tên kết nối
    Power --> Control
    Sensor --> Control
    Control --> Output
    
    %% Đường nét đứt 2 chiều thể hiện kết nối WiFi
    Control -. "WiFi" .-> UI
    UI -. "WiFi" .-> Control
    '''
## 3.3 Schematic 
