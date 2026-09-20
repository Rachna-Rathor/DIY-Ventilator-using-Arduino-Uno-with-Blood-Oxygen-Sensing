# DIY Ventilator using Arduino Uno with Blood Oxygen Sensing

## 📌 Project Overview

The **DIY Ventilator using Arduino Uno with Blood Oxygen Sensing** is an educational embedded systems prototype designed to demonstrate how a microcontroller can monitor blood oxygen saturation (SpO₂) and use the measured value as an input for controlling airflow.

The project combines an **Arduino Uno**, a **blood oxygen (SpO₂) sensor**, and a basic ventilation mechanism. The Arduino continuously receives oxygen-level information from the sensor and uses the measured value to control the ventilation system according to predefined conditions.

The project was developed to understand the practical implementation of:

* Microcontroller-based control systems
* Sensor interfacing
* Embedded C programming
* Real-time sensor monitoring
* Automated decision-making
* Motor/airflow control
* Basic alarm and safety mechanisms

> **⚠️ Disclaimer:** This project is an educational prototype developed for learning and demonstration purposes. It is **not a certified medical ventilator and must not be used for patient treatment or clinical applications.**

---

## 🎯 Purpose of the Project

The main purpose of this project was to understand how an embedded system can:

1. Read information from a physiological sensor.
2. Process the sensor data using a microcontroller.
3. Compare the measured value with predefined conditions.
4. Automatically control an actuator based on the sensor reading.
5. Provide an alert when the measured oxygen level reaches a defined critical condition.
6. Allow manual control when required.

This project helped demonstrate the complete basic embedded-system flow:

**Sensor → Microcontroller → Processing → Decision → Actuator/Alert**

---

## 🔧 Components Used

| Component                             | Purpose                                                                 |
| ------------------------------------- | ----------------------------------------------------------------------- |
| **Arduino Uno**                       | Main microcontroller used to process sensor data and control the system |
| **Blood Oxygen (SpO₂) Sensor**        | Measures blood oxygen saturation level                                  |
| **DC Motor / Airflow Mechanism**      | Generates or controls airflow                                           |
| **Motor Driver / Transistor Circuit** | Used for controlling the motor from the Arduino                         |
| **Buzzer**                            | Provides an alert when a defined condition is detected                  |
| **LEDs**                              | Provides visual indication of system status                             |
| **Breadboard**                        | Used for prototyping the circuit                                        |
| **Jumper Wires**                      | Used for electrical connections                                         |
| **Power Supply**                      | Provides power to the circuit                                           |
| **Manual Control/Switch**             | Allows manual operation/control of the system                           |

> Component selection can vary depending on the exact hardware implementation.

---

## 🧠 How Does It Work?

The system works in a simple feedback/control sequence.

### Step 1 — Oxygen Level Measurement

The **SpO₂ sensor** detects the user's blood oxygen saturation level.

The sensor provides the measured data to the **Arduino Uno**.

### Step 2 — Data Processing

The Arduino receives the sensor reading and processes it using the programmed logic.

The microcontroller continuously checks the oxygen-level value.

### Step 3 — Condition Checking

The measured value is compared against predefined threshold conditions.

For example:

```text
Oxygen Level
     ↓
Arduino reads sensor
     ↓
Compare with predefined threshold
     ↓
 ┌───────────────┐
 │ Oxygen level  │
 │ within range? │
 └───────┬───────┘
         │
    ┌────┴────┐
    │         │
   YES       NO
    │         │
Normal      Control
operation   airflow /
            trigger alert
```

### Step 4 — Airflow Control

Depending on the programmed condition, the Arduino controls the airflow mechanism.

The motor/actuator can be switched or controlled according to the system logic.

### Step 5 — Alert System

If the measured value reaches a predefined critical condition, the system can activate a **buzzer and/or LED** to provide an alert.

### Step 6 — Manual Override

A manual control mechanism can be used to allow the operator to control the system independently of the automatic sensor-based logic.

---

## ⚙️ Basic System Architecture

```text
        ┌──────────────────┐
        │  SpO₂ Sensor     │
        │ Blood Oxygen     │
        │ Measurement      │
        └────────┬─────────┘
                 │
                 │ Sensor Data
                 ↓
        ┌──────────────────┐
        │   Arduino Uno    │
        │                  │
        │ Data Processing  │
        │ Condition Check  │
        │ Control Logic    │
        └───────┬─────┬────┘
                │     │
        ┌───────┘     └──────────┐
        ↓                        ↓
┌───────────────┐        ┌───────────────┐
│ Airflow /     │        │ Buzzer / LED  │
│ Motor Control │        │ Alert System   │
└───────────────┘        └───────────────┘

                ↑
                │
        Manual Control
```

---

## 💻 Software & Programming

### Programming Language

* **Embedded C / Arduino C++**

### Development Environment

* Arduino IDE
* Arduino Uno
* Serial Monitor for debugging and monitoring sensor readings

The program continuously reads sensor data and executes the control logic based on predefined conditions.

---

## 🔌 Arduino's Role

The Arduino Uno acts as the **central controller** of the system.

Its main responsibilities are:

* Reading SpO₂ sensor data
* Processing sensor readings
* Checking predefined conditions
* Controlling the airflow mechanism
* Activating alerts
* Handling manual control
* Continuously monitoring the system

In simple terms:

> **Arduino acts as the brain of the project.**

---

## 📊 Control Logic

The basic control logic can be represented as:

```text
START
  │
  ↓
Initialize Arduino
  │
  ↓
Initialize Sensor
  │
  ↓
Read SpO₂ Value
  │
  ↓
Process Sensor Data
  │
  ↓
Compare with Threshold
  │
  ├── Normal Condition
  │       ↓
  │   Normal Operation
  │
  └── Critical Condition
          ↓
     Adjust/Control Airflow
          ↓
     Activate Alert
          ↓
      Continue Monitoring
```

The threshold values and control behavior are defined in the Arduino program and should be treated as **prototype parameters**, not medical treatment thresholds.

---

## 🚀 Key Features

* Real-time SpO₂ monitoring
* Arduino-based embedded control
* Automatic airflow control logic
* Manual override/control
* Buzzer-based alert mechanism
* LED-based system indication
* Continuous sensor monitoring
* Embedded C programming
* Sensor-to-actuator control implementation

---

## 🛠️ Skills Demonstrated

This project demonstrates practical exposure to:

* Arduino Uno
* Embedded C
* Microcontroller programming
* Sensor interfacing
* Digital I/O
* Basic electronics
* Actuator control
* Motor control
* Real-time monitoring
* Embedded system debugging
* Hardware prototyping
* Control logic implementation

---

## 🔍 Testing & Debugging

During development, the system can be tested by:

1. Checking sensor connections.
2. Verifying sensor readings through the Arduino Serial Monitor.
3. Testing the motor/airflow mechanism independently.
4. Checking buzzer and LED functionality.
5. Testing automatic control conditions.
6. Testing the manual override.
7. Observing system behavior for different sensor readings.

---

## 📚 What I Learned

Through this project, I gained practical understanding of how different components of an embedded system work together.

### Hardware

I learned about:

* Arduino Uno
* Sensors
* Microcontroller I/O
* Motor/actuator control
* Basic circuit connections
* Prototyping and testing

### Software

I gained experience with:

* Embedded C programming
* Reading sensor data
* Conditional statements
* Control logic
* Serial communication/debugging
* Hardware-software integration

### Embedded Systems

The project helped me understand the complete process of:

**Sensing → Processing → Decision Making → Actuation**

---

## 🔮 Future Improvements

Possible improvements for a more advanced prototype include:

* More accurate and calibrated sensing
* Closed-loop airflow/pressure control
* Pressure and flow sensors
* Better motor control using PWM
* LCD/OLED display for real-time parameters
* Data logging
* Improved alarm and safety mechanisms
* Wireless monitoring
* More robust hardware enclosure
* Fail-safe mechanisms
* Extensive hardware validation and testing

---

## ⚠️ Limitations

This project is a **prototype for educational purposes**.

It does not include the extensive requirements of a certified medical ventilator, such as:

* Clinical validation
* Medical-grade sensors
* Precise pressure and flow control
* Certified safety mechanisms
* Patient-specific ventilation modes
* Regulatory compliance
* Professional medical-device testing

Therefore, this project should **not be used as a medical device or for patient treatment**.
---

## ⭐ Project Summary

This project demonstrates a basic **embedded control system** where physiological sensor data is used as an input to a microcontroller-based control mechanism.

The overall concept can be summarized as:

```text
      SENSOR
        ↓
   DATA READING
        ↓
    ARDUINO UNO
        ↓
  DATA PROCESSING
        ↓
  CONDITION CHECK
      ↙     ↘
   NORMAL   CRITICAL
     ↓         ↓
  NORMAL    AIRFLOW /
 OPERATION   ALERT
```

The project provided hands-on experience in **Arduino, Embedded C, sensor interfacing, actuator control, hardware prototyping, and embedded-system programming**.
