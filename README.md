# Server Cabinet Temperature Monitor

ESPHome-based dual-sensor temperature and humidity monitoring system for a 9U server cabinet.

**Project Goal**: Monitor temperature differential between the top and bottom of the cabinet to detect hot spots, poor airflow, or fan failures early.

## Hardware Used

| Component                    | Model / Details                        | Quantity |
|-----------------------------|----------------------------------------|----------|
| Microcontroller             | HiLetgo NodeMCU ESP8266 (CP2102)      | 1        |
| Temperature/Humidity Sensor | HiLetgo DHT22                          | 2        |
| Power                       | USB 5V (from server PSU or wall adapter) | 1     |
| Enclosure                   | 3D printed / zip-tied inside cabinet   | -        |

**Sensor Placement**:
- Top sensor: Near the ceiling of the cabinet (hot air rises)
- Bottom sensor: Near the floor / intake area

## Wiring

- DHT22 Top → GPIO5 (D1)
- DHT22 Bottom → GPIO4 (D2)
- VCC → 3.3V
- GND → GND

Full wiring details in [`hardware/wiring.md`](hardware/wiring.md)

## ESPHome Configuration

Full config: [`esphome/server-cabinet-temp.yaml`](esphome/server-cabinet-temp.yaml)

## Home Assistant Integration

Template sensors for:
- Average Cabinet Temperature
- Maximum Temperature
- Temperature Delta (Top - Bottom)

See: [`home-assistant/template-sensors.yaml`](home-assistant/template-sensors.yaml)

## Features

- Real-time temperature & humidity (top + bottom)
- Calculated average and delta
- WiFi signal strength monitoring
- Uptime tracking
- Fully local control via ESPHome

## Future Enhancements

- Add alerts if delta > 10°F
- Add cabinet fan automation
- Migrate to ESP32 for better range / features
- Add OLED display

## How to Replicate This Project

1. Flash the ESP8266 using ESPHome
2. Wire the two DHT22 sensors
3. Add the YAML to ESPHome in Home Assistant
4. Add template sensors
5. Mount inside server cabinet

---

**Last Updated**: May 2026
**Author**: Duc Nguyen