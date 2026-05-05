# Wiring Diagram & Instructions

## Connections

### Top Sensor (Hot Air - Ceiling Area)
- **VCC** (Pin 1) → 3.3V on NodeMCU
- **DATA** (Pin 2) → GPIO5 (D1)
- **NC** (Pin 3) → Not Connected
- **GND** (Pin 4) → GND on NodeMCU

### Bottom Sensor (Cool Air - Floor Area)
- **VCC** (Pin 1) → 3.3V on NodeMCU
- **DATA** (Pin 2) → GPIO4 (D2)
- **NC** (Pin 3) → Not Connected
- **GND** (Pin 4) → GND on NodeMCU

**Important Notes**:
- Use 3.3V logic (DHT22 is **not** 5V tolerant on data pin)
- Add a 10kΩ pull-up resistor between DATA and VCC if you experience unstable readings (optional but recommended)
- Keep sensor wires away from high-power cables to reduce interference

## Recommended Mounting
- Top sensor: Near the top exhaust area
- Bottom sensor: Near the bottom intake vents
- Secure with zip ties or small 3D printed mounts