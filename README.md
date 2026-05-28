# pianotuner
Prototype/planning project for building an automated piano tuning device.

## Planning stack
- **PCB schematic + board**: KiCad
- **Mechanical parts + assembly**: Autodesk Inventor
- **Firmware/controller**: Arduino framework on **ESP32-WROOM**

## Project idea
Build a portable device that listens to piano strings, estimates pitch error, and drives a tuning key mechanism in small controlled steps.

## How to execute (planning first, no parts required yet)
1. Define requirements (target piano types, tuning accuracy, portability, budget).
2. Split architecture into modules:
   - Audio sensing (microphone + analog front-end)
   - Control electronics (ESP32-WROOM + drivers + power)
   - Mechanical drive (motor + coupling to tuning pins)
3. Design electronics in KiCad:
   - Create schematic with ESP32-WROOM, mic input, motor driver, power regulation, and connectors.
   - Route PCB for signal quality and safe motor current paths.
4. Design mechanics in Inventor:
   - Model motor mount, tuner-key adapter, and enclosure parts.
   - Build full assembly and check clearances, alignment, and serviceability.
5. Plan firmware in Arduino:
   - Capture audio, detect fundamental frequency, compute cents error.
   - Add control loop to command motor step size/direction based on pitch error.
   - Include safety limits, calibration mode, and manual override.
6. Prepare a bill of materials (BOM) for later purchasing:
   - ESP32-WROOM dev board/module
   - MEMS/electret microphone + conditioning circuit
   - Stepper/DC gear motor + driver
   - Power supply/battery + regulators
   - Bearings/couplers/fasteners/enclosure hardware
7. Validate virtually before buying parts:
   - Electrical checks in KiCad (ERC/DRC)
   - Mechanical interference checks in Inventor assembly
   - Firmware flow simulation/prototyping with mocked sensor data
