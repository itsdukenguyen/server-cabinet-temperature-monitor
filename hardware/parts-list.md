# Parts List

## Core Components

| Item                              | Model / Link                                      | Quantity | Notes |
|-----------------------------------|---------------------------------------------------|----------|-------|
| Microcontroller                   | HiLetgo NodeMCU ESP8266 (CP2102)                 | 1        | Main board |
| Temperature & Humidity Sensor     | HiLetgo DHT22 AM2302                              | 2        | Top + Bottom |
| Jumper Wires                      | Male-to-Female Dupont Wires                       | ~10      | For connections |
| USB Power Cable                   | Micro USB or USB-C to USB                         | 1        | Power from server PSU or adapter |
| Enclosure / Mounting              | 3D printed bracket or zip ties                    | -        | Secure inside cabinet |
| Optional: Heat Shrink / Electrical Tape | -                                              | -        | Insulation |

**Total Estimated Cost**: ~$15–25 USD

## Pinout Reference

- **Top DHT22** → GPIO5 (D1)
- **Bottom DHT22** → GPIO4 (D2)
- VCC → 3.3V on NodeMCU
- GND → GND