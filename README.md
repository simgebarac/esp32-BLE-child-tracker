# 🛡️ ESP32 & Flutter BLE Child Tracker

This project is a smart tracking system developed using **ESP32** and **Bluetooth Low Energy (BLE)** technology. The **Flutter** mobile application monitors the **RSSI** (Received Signal Strength Indicator) values from the device to estimate distance and provide real-time safety alerts.



## ✨ Features
* 🔍 **Smart Scanning:** Automatically detects and lists active BLE devices in the vicinity.
* 📈 **Real-Time RSSI Analysis:** Updates signal strength every second for precise monitoring.
* 🚦 **Dynamic Alerts:** Visual feedback based on distance (Safe/Warning/Danger).
* 📱 **Modern UI:** User-friendly, dark-themed interface built with Material Design.
* 🛠️ **Device Management:** Ability to add, name, track, and delete multiple devices.

## 🛠️ Tech Stack
* **Mobile Framework:** Flutter (Dart)
* **Hardware:** ESP32 (BLE Server Mode)
* **Core Libraries:** `flutter_blue_plus`, `permission_handler`

## 📡 How It Works
The app calculates the safety status based on the signal strength (dBm) using the following logic:

| Signal Strength | Status | Visual Indicator |
| :--- | :--- | :--- |
| **> -60 dBm** | ✅ SAFE | Green Color |
| **-60 to -80 dBm** | ⚠️ MOVING AWAY | Orange Color |
| **< -80 dBm** | 🚨 DANGER! | Red Color |
