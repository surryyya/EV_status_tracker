# ⚡ Real-Time EV Status Tracking System

> An IoT-based embedded system to monitor battery health, temperature, and motor condition of an electric vehicle in real time using ESP32.

---

## 📌 Overview

Electric vehicles depend heavily on battery performance and system reliability. However, real-time monitoring of key parameters is not always available in low-cost or prototype setups.

This project was built to understand and implement a simple, practical solution for tracking important EV parameters such as battery charge, temperature, and vibration. The system continuously monitors these values and provides real-time feedback, helping in early fault detection and safer operation.

---

## 🎯 Objective

To design a real-time EV monitoring system that:

* Tracks battery and system health
* Detects abnormal conditions early
* Enables remote monitoring using IoT

---

## ⚙️ System Description

The system is built using an ESP32 microcontroller connected to multiple sensors.

* A voltage sensor measures battery voltage from a 3-cell Li-ion pack
* A temperature sensor monitors thermal conditions
* A vibration sensor detects abnormal motor behavior

The ESP32 processes this data and transmits it wirelessly via Wi-Fi. The data can be viewed in real time using a mobile dashboard (Blynk).

---

## 🔄 Working Principle

The sensors continuously collect real-time data from the EV system.

The ESP32:

1. Reads sensor inputs
2. Converts raw values into meaningful units
3. Estimates battery State of Charge (SoC)
4. Compares values with predefined thresholds
5. Triggers alerts or actuators when needed
6. Sends data to a mobile dashboard

This allows continuous monitoring of the system’s condition.

---

## ⚡ Key Features

### 🔋 Battery SoC Monitoring

Battery voltage is measured and used to estimate the State of Charge (SoC) in real time.

⚠️ An LED warning is triggered when the battery level drops below a set threshold.

---

### 🌡️ Temperature Monitoring & Protection

Temperature is monitored using a DS18B20 sensor.

If overheating is detected:

* ⚠️ LED warning is activated
* 🌬️ 12V DC fan turns ON automatically

---

### ⚙️ Motor Vibration Sensing *(Unique Feature)*

A vibration sensor (SW-420) is used to detect abnormal motor behavior.

This helps in:

* Early fault detection
* Preventing unexpected breakdowns
* Reducing maintenance costs

This feature is especially useful in EV logistics and delivery fleets.

---

### 📱 IoT-Based Remote Monitoring (Blynk)

All sensor data is sent via Wi-Fi and displayed on the Blynk mobile app.

This enables real-time monitoring of:

* Battery status
* Temperature
* Vibration levels

---

## 🛠️ Hardware Components

* ESP32
* DS18B20 Temperature Sensor
* Voltage Sensor Module (0–25V)
* SW-420 Vibration Sensor
* Rechargeable Li-ion Cells
* LEDs
* 12V DC Fan

---


## 🤔 Why This Project Matters

This project focuses on practical EV challenges like battery safety and system monitoring.

* Detects early signs of component failure
* Implements thermal protection similar to real EV systems
* Introduces predictive maintenance concepts

It shows how embedded systems and IoT can be used to improve EV reliability and safety in a cost-effective way.

---

## 🚀 Future Scope

### 1) Machine Learning Integration

Sensor data can be used to train models for:

* Fault prediction
* Anomaly detection
* Smart maintenance decisions

---

### 2) Large-Scale EV Fleet Monitoring

The system can be expanded to monitor multiple vehicles through a centralized cloud dashboard.

Useful for:

* EV logistics
* Delivery fleets
* Smart mobility platforms

---


