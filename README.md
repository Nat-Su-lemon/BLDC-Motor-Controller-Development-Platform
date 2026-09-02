# BLDC Motor Controller Development Platform

A 4-layer, three-phase brushless DC (BLDC) motor driver built as a development platform for Field Oriented Control (FOC). Designed around a DRV8323 gate driver, a discrete MOSFET power stage, and an STM32G4, the board handles a 6 to 60 V bus at up to 20 A, with broad test-point coverage and configuration access for bring-up and experimentation.

## Overview

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/bldcirl.jpg" height="280">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/bldcpcb.png" height="280">
</p>

## Key Features

- **Wide input range** — 6 to 60 V bus, up to 20 A continuous, three-phase output.
- **FOC-ready** — DRV8323 gate driver + discrete MOSFET power stage driven by an STM32G4, chosen for its math accelerator and motor-control peripherals.
- **Development-first** — broad test-point coverage and configuration access across the board for probing, tuning, and bring-up.
- **Current sensing** — Kelvin-connected shunt sensing for accurate, low-noise phase-current measurement.
- **Robust power distribution** — buck/LDO conversion, USB/motor-supply multiplexing, relay-controlled bus switching, and TVS protection.
- **CAN connectivity** — onboard CAN interface for control and telemetry.
- **Thermal and EMI management** — high-current copper pours, thermal vias, and compact switching loops to keep the power stage cool and quiet.

## System Overview

Top-level block diagram of the controller: the STM32G4 host, DRV8323 gate driver and MOSFET power stage, current sensing, power distribution, and CAN interface.

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/toplevel.png" width="80%">
</p>

## Schematics

**Microcontroller.** STM32G4 host with its motor-control peripherals, configuration, and test-point access.

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/stm32.png" width="80%">
</p>

**Gate driver and power stage.** DRV8323 three-phase gate driver with the discrete MOSFET half-bridges and Kelvin shunt current sensing.

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/drv8323s.png" width="80%">
</p>
<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/switches.png" width="80%">
</p>

**Power distribution.** Low-voltage rails via buck/LDO conversion, USB/motor-supply power multiplexing, relay-controlled bus switching, and TVS protection.

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/powerdistr.png" width="80%">
</p>

**CAN interface.** Onboard CAN transceiver for control and telemetry.

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/can.png" width="80%">
</p>



## PCB Layout

A 4-layer stackup with high-current pours and thermal vias on the power layers and compact switching loops to manage thermal and EMI performance.

**Top layer**

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/toplayer.png" width="70%">
</p>

**Bottom layer**

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/botlayer.png" width="70%">
</p>

**Power layer**

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/powerlayer.png" width="70%">
</p>

## Mechanical

<p align="center">
  <img src="https://raw.githubusercontent.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/main/assets/mechanical.png" width="70%">
</p>

📄 **[Download the full schematic PDF](https://github.com/Nat-Su-lemon/BLDC-Motor-Controller-Development-Platform/blob/main/assets/BLDC%20Motor%20Controller.pdf)**
