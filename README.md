![Server Cabinet Temperature Monitor](banner.jpg)

# Server Cabinet Temperature Monitor

ESPHome-based dual DHT22 temperature and humidity monitoring system for a **9U server cabinet**.

**Project Goal**: Monitor temperature differential between the top and bottom of the cabinet to detect hot spots, poor airflow, or fan failures early.

---

## Badges

![ESPHome](https://img.shields.io/badge/ESPHome-000000?style=for-the-badge&logo=esphome&logoColor=white)
![ESP8266](https://img.shields.io/badge/ESP8266-000000?style=for-the-badge&logo=esp8266&logoColor=white)
![Home Assistant](https://img.shields.io/badge/Home%20Assistant-41BDF5?style=for-the-badge&logo=home-assistant&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## Features

- Real-time Top & Bottom Temperature + Humidity
- Average Cabinet Temperature
- Temperature Delta (Top - Bottom)
- WiFi Signal Strength & Uptime Monitoring
- Fully local (no cloud dependency)

---

## Hardware Used

See [`hardware/parts-list.md`](hardware/parts-list.md)

## Wiring & Installation

See [`hardware/wiring.md`](hardware/wiring.md)

## ESPHome Configuration

Full config: [`esphome/server-cabinet-temp.yaml`](esphome/server-cabinet-temp.yaml)

## Home Assistant Template Sensors

See: [`home-assistant/template-sensors.yaml`](home-assistant/template-sensors.yaml)

## How to Replicate This Project

1. Flash the ESP8266 using ESPHome
2. Wire the two DHT22 sensors (Top → GPIO5/D1, Bottom → GPIO4/D2)
3. Copy the YAML files into Home Assistant
4. Mount sensors securely inside the cabinet

---

## Project Photos

*(Add your photos here — highly recommended)*

![Cabinet Top Sensor](hardware/photos/top-sensor.jpg)
![Cabinet Bottom Sensor](hardware/photos/bottom-sensor.jpg)
![Installed View](hardware/photos/installed.jpg)

---

## Known Issues / Notes

- DHT22 sensors can occasionally give false high readings if placed too close to hot components
- 3.3V logic only — do not use 5V on data pins
- Consider adding a small 10kΩ pull-up resistor if readings are unstable

---

**Last Updated**: May 2026  
**Author**: Duc Nguyen  
**License**: MIT