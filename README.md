# USB-TO-EtherCAT-Adapter-Board

A compact USB-to-EtherCAT adapter board that allows a USB host system to communicate with an EtherCAT network. An STM32 microcontroller handles the USB side and exchanges data with a LAN9252 EtherCAT slave controller, which manages the fieldbus protocol and drives two RJ45 ports for daisy-chain operation. The board is bus-powered from USB and designed in KiCad for industrial automation, embedded systems, and real-time networking use.

---

## Key Goals

**1. Reliable protocol bridging**
Provide a stable conversion path between USB and EtherCAT so a standard host machine can participate in a deterministic industrial network without dedicated fieldbus hardware.

**2. Standards-compliant hardware design**
Follow proper high-speed design practice — controlled differential routing, correct termination, clean power distribution, and stable clocking — so the board meets EtherCAT physical-layer requirements and operates reliably in noisy environments.

**3. Compact and practical integration**
Keep the board bus-powered, self-contained, and small enough to sit inline in an existing network, with edge-mounted connectors, mounting holes, and a debug header for easy deployment and development.

---

## Features

**Communication**
Full signal chain from USB host through the microcontroller to the EtherCAT slave controller, with two RJ45 ports allowing the adapter to be placed anywhere in a daisy-chained network.

**Design quality**
Length-matched differential pairs, proper termination networks, dedicated filtered supply rails, per-pin decoupling, and independent clock sources for the controller and the EtherCAT device.

**Usability**
Single-cable USB power, on-board 3.3 V regulation, status LEDs, reset switch, SWD programming header, and mounting holes for enclosure fitting.

---

## Hardware

| Item | Detail |
|---|---|
| Microcontroller | STM32F411CEUx (ARM Cortex-M4) |
| EtherCAT slave controller | Microchip LAN9252 |
| Configuration memory | 24LC512 I²C EEPROM |
| Network ports | 2x RJ45 (IN / OUT, integrated magnetics) |
| Host interface | USB |
| Power | USB bus powered, AMS1117-3.3 regulator |
| Debug | 4-pin SWD header |
| Design software | KiCad |

---

## Software and Tools Used

| Tool | Purpose |
|---|---|
| **KiCad** | Schematic capture, PCB layout, DRC/ERC |
| **KiCad Symbol & Footprint Editor** | Custom symbols and footprints |
| **KiCad 3D Viewer** | Mechanical and visual verification |
| **Gerber Viewer** | Fabrication output verification |

---

## Outputs / Deliverables

- Schematic (KiCad + PDF export)
- PCB layout (KiCad + PDF export)
- Gerber files (fabrication-ready)
- Drill files
- Bill of Materials (BOM)
- Pick and place file
- 3D render

---

## Images

| Schematic | PCB Layout | 3D View |
|---|---|---|
| ![Schematic](images/schematic.png) | ![Layout](images/layout.png) | ![3D](images/3d_view.png) |

---

## Applications

- Industrial automation and motion control
- EtherCAT slave/master development and testing
- Embedded systems requiring fieldbus connectivity
- Real-time networking and data acquisition setups

---

## Status

Design complete, verified through ERC/DRC and 3D review. *(Update once fabricated and hardware-tested.)*

---

## License

*(Add your preferred license, e.g. MIT, CERN-OHL-P, or CC BY 4.0.)*

## Author

**Sudesh Pandit**
*(Add GitHub/LinkedIn links here.)*
