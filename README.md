# 🤖 WiFi-Controlled Robot using Raspberry Pi

This project explores the development of a **WiFi-controlled robot** using **Raspberry Pi**, designed as part of an IoT and networking course. The robot is navigated through IP-based control and integrates motor drivers, sensors, and Python scripts to receive commands remotely over a wireless network.

---

## 🎯 Objective

To understand networking principles by building a small-scale robot that can be controlled over WiFi using IP commands and Raspberry Pi. The goal is to simulate real-world IoT applications where devices can be operated remotely over the internet.

---

## 🛠️ Hardware Used

- 🧠 Raspberry Pi (any 3/4 model)
- 🔌 Osoyoo/L298N Motor Driver Circuit (used both, shifted due to failure)
- 🔋 Battery Pack (for motors and Raspberry Pi)
- 🛞 DC Motors + Wheels
- 🔄 PCA9685 PWM Controller (for servo/LED control)
- 📏 Line Tracking Sensor
- 🔌 Jumper wires, breadboard, chassis

---

## 🧑‍💻 Software/Tools Used

- Python 3
- GPIO and `Adafruit_PCA9685` libraries
- Putty / SSH for remote control
- Raspbian OS
- `i2c-tools` and `raspi-config` for hardware access

---

## 📶 How It Works

1. Raspberry Pi connects to a local WiFi network.
2. User accesses the Pi via SSH (Putty) and uses IP address commands to control the bot.
3. Motor driver receives commands via GPIO signals.
4. PCA9685 controls servo motors/LEDs if connected.
5. Line tracking sensor is mounted for future expansion into auto-navigation.

---

## 🧪 Procedures & Configuration

- Enable `SSH` and `I2C` on Raspberry Pi using `sudo raspi-config`.
- Install required libraries:

```bash
sudo pip3 install adafruit-pca9685
sudo apt-get install python3-rpi.gpio


Wiring is done as per standard Raspberry Pi robot guides.

IP-based commands sent via Putty terminal.

**⚠️ Challenges Faced**
First circuit (L298N) burned due to current fluctuation

GPIO motor signals failed during deployment

Debugged issues using Raspberry Pi and motor forums

Switched to Osoyoo driver + PCA9685 for more stable current control

**🚀 Future Enhancements**
Add camera module to stream live video

Host a simple Flask-based web interface for control

Integrate sensor data logging to cloud (e.g., Firebase or MQTT)

Use onboard ML model for basic obstacle or pattern recognition

**📸 Sample Design & Controls**
Currently under refinement — final prototype will include:

Direction control via keyboard/WiFi commands

Camera feed over Flask server

Auto-navigation with line sensors (WIP)

**🔗 References & Tutorials**
https://rootsaid.com/robot-control-over-wifi/

https://osoyoo.com/2020/08/01/how-to-use-osoyoo-model-pi-l298n-motor-driver-board-in-raspberry-pi-robot-car/

YouTube Guide 1

YouTube Guide 2

👨‍🔬 Authors
Yashwanth Sai

Sandpita Subir Khare
📅 Aug 2021 – Dec 2021
📍 [Project under Networking & IoT course]
