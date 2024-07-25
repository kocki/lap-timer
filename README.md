# Laptime Project Summary

## Power Management
- **Batteries:** EEMB 3.7V 1100mAH LiPo batteries
- **Charging Module:** DC 5V 2.1A Mobile Power DIY Board (4.2V Charge/Discharge/Boost/Battery Protection/Indicator Module for 3.7V Lithium 18650 Li-ion)
- **Configuration:** 
  - Connect to ESP32
  - Charge battery when USB-C is powered
  - Use battery to power ESP32 when USB-C is not present

## Module and Wiring Configuration
- **Main Unit (MU):** ESP32 D1 Mini with a light sensor and an OLED screen (0.96")
- **Laser Unit (LU):** ESP32 C3-zero to control the laser
- **Gate Units (GU):** 
  - MU will handle the main logic
  - LU will be the simplest possible
- **Control Unit (CU):**
  - Decision needed: Should the first MU act as the CU, or should any MU be capable of becoming the CU?
  - Universal CU approach requires complex coding but is more flexible
  - Separate CU approach simplifies code but requires an additional ESP32

## Communication
- **Protocols:** BLE/ESPNow
- **Modes:**
  - Optimize for power efficiency when not in use
  - Ensure precision when in measuring mode

## Future Versions
- **Considerations:**
  - Ideas for future iterations not included in version 1

## User Interface
- **Displays:**
  - Use existing display modules
  - Consider using the WLED matrix 16x16 for a big time display in future versions (possibly as the CU)

## Security
- **Basic Security:**
  - Prevent easy interference with wireless communication

## Compliance and Certification
- **Version 1:** 
  - Not a priority

## Project Management and Documentation
- **Tools:** 
  - GitHub for code and documentation
  - PlatformIO for firmware development
- **Languages:**
  - C++ as the primary language

## Exclusions for Version 1
- **Environmental Testing:** Not in scope
- **Compliance and Certification:** Not a priority

