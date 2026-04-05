<div align="center">

# Vehicle Control System Hardware Design

![Status: Prototype](https://img.shields.io/badge/Status-Prototype-yellow?style=flat-square)
![MCU: ATmega328P](https://img.shields.io/badge/MCU-ATmega328P-blue?style=flat-square)
![Interface: CAN Bus | LoRa](https://img.shields.io/badge/Interface-CAN_|_LoRa-00599C?style=flat-square)

</div>

This repository contains the hardware design (schematic and PCB) files and test firmware for the project. The system is based on the **ATmega328P** microcontroller, designed to read, process, and transmit vehicle data over long distances.

## Hardware Features & Integrations

The design is a custom printed circuit board (PCB) operating at a 5V logic level, consolidating various communication modules onto a single board.

* **Power Management:** The system's 5V requirement is supplied by an **LM2596** step-down (buck) regulator module powered via a standard DC Jack.
* **Microcontroller:** DIP-28 package **ATmega328P** utilizing an external crystal oscillator circuit.
* **In-Vehicle Communication (CAN Bus):** Access to the vehicle's network via an **MCP2515** CAN controller module connected through the SPI interface (J3 socket).
* **Telemetry (LoRa):** **LoRa** module integration with a dedicated UART socket (M0, M1, RX, TX, AUX) for long-range wireless data transmission.
* **Location Tracking (GPS):** A GPS module connected to a secondary hardware/software UART line (J5 socket) for speed, location, and timing (PPS) data.
* **Status Indicators:** 6 dedicated debug LEDs connected to pins PC0-PC5 to easily visualize system status, communication packets, or error codes.

## Pinout Summary
* `PC0 - PC5` : Status LEDs (D1 - D6)
* `PB3, PB4, PB5` : SPI Line (MCP2515 CAN Module)
* `PD0, PD1, PD2, PD3, PD4` : LoRa UART and Control (RX, TX, M0, M1, AUX)
* `PD6, PD7` : GPS UART and PPS signals

---

## Schematic

![AKS Şematik](./images/AKS_Schematic.png)

---

## PCB

![AKS PCB](./images/AKS_Pcb.png)

---
## Contributors
<a href="https://github.com/ravzagulsahin">
  <img src="https://github.com/ravzagulsahin.png" width="50px" style="border-radius: 50%;" alt="Contributor 1"/>
</a>
<a href="https://github.com/Aytunctr">
  <img src="https://github.com/Aytunctr.png" width="50px" style="border-radius: 50%;" alt="Contributor 2"/>
</a>
