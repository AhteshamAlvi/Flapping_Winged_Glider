# Flapping Winged Glider (RoboRaptor)

Bio-Inspired Articulated Wing Glider for Wind Characterization and Flapping Flight Research

Ahtesham Alvi · Piyush Sethy · Saiarun Jayanthi <br>
FIRE Bio-Inspired Robotics — University of Maryland: College Park <br>
Advisor: Dr. Lena Johnson

---
## Table of Contents

- [Overview](#overview)
- [Research Goal](#research-goal)
- [Overview](#overview)
- [Final Firmware Version](#final-firmware-version)
- [Prototyping](#prototyping)
- [Mechanical Design](#mechanical-design)
- [Firmware and Control](#firmware-and-control)
- [Wind Sensing and Data Logging](#wind-sensing-and-data-logging)
- [Experimental Results](#experimental-results)
- [Repository Structure](#repository-structure)
- [Hardware Components](#hardware-components)
- [Key Engineering Insights](#key-engineering-insights)
- [Future Work](#future-work)
- [Acknowledgments](#acknowledgments)
- [License](#license)

---
## Overview

This project develops a bio-inspired, tethered flapping wing glider designed to investigate how atmospheric wind conditions interact with articulated wing kinematics in lightweight robotic flight systems. The platform combines a bird-inspired airframe, servo-actuated flapping wings, onboard sensing, and wind telemetry logging to experimentally characterize the behavior of mechanically flapping gliders under real wind conditions.

The system functions as an aeroelastic test platform rather than a powered drone. Instead of continuous propulsion, it leverages aerodynamic lift from wind while actively modulating wing motion through servo actuation. This enables controlled experiments on wind-assisted flight, flapping dynamics, and structural-aerodynamic coupling in lightweight robotic wings.

---

## Research Goal

The objective is to create a tethered gliding robot with articulating wings capable of measuring and characterizing how wind influences flapping and gliding behavior in bio-inspired aerial robots. The platform enables experimental study of atmospheric energy interaction with mechanical flapping systems and supports exploration of passive-active hybrid flight modes.

---

## Overview

This research project consists of four distinct parts (other than the final report):

Mechanical Structure <br>
A lightweight, bird-inspired winged airframe using carbon-fiber spars, flexible membrane wings, and 3D-printed servo mounts and joints designed to withstand cyclic flapping loads.

Actuation and Control <br>
Metal-gear high-torque servos drive articulated wing spars. Arduino-based firmware controls flapping motion, torque behavior, and receiver input for manual or programmed wing actuation.

Sensing and Telemetry <br>
Onboard sensors measure environmental and motion data (temperature, wind vector components, inertial motion). Data is logged via an OpenLog SD module for time-series analysis.

Experimental Validation <br>
Wind-dependent flight trials are recorded via telemetry logs and video to correlate aerodynamic performance with mechanical and control configurations.

---

## Final Firmware Version

The final integrated control firmware for the RoboRaptor platform is:

**CompleteCode_v6.ino**

This version consolidates:

* Servo flapping control
* High-torque actuation logic
* Receiver/remote input handling
* Sensor acquisition
* OpenLog SD telemetry output

Earlier firmware files (ControlCode_v*, PrecisionControl, HighTorqueMotorControl, etc.) represent intermediate development stages and are retained for reference and historical comparison, but **CompleteCode_v6.ino** should be used for deployment and experiments.

---

## Prototyping

Prototype 1 — Sparrow/Falcon Static Wings <br>
Wooden dowel frame with plastic film wings. Failed due to structural fragility and unstable joints.

Prototype 2 — Sparrow/Falcon with Actuation <br>
Introduced servo mounts and actuating spars. Wooden spars fractured under load during flight.

Prototype 3 — Eagle Glider <br>
Transitioned to carbon-fiber spars and improved wing geometry. Achieved stable gliding flight in winds above ~7 mph.

Prototype 4 — Eagle with Articulated Wings <br>
Integrated servo-driven flapping, electronics plate, and improved membrane material. Achieved controlled flapping and directional flight.

---

## Mechanical Design

The mechanical system focuses on load-bearing servo mounts and articulated wing spars capable of sustaining cyclic flapping stresses.

Key design features:

* Carbon-fiber structural spars for stiffness-to-weight efficiency
* Flexible membrane wings for aeroelastic deformation tolerance
* 3D-printed servo mounts optimized for fatigue resistance
* Modular covers and electronics enclosure
* Bird-inspired wing geometries (Sparrow, Falcon, Eagle models)

Multiple mount iterations reflect optimization for torque capacity, vibration damping, and oscillatory load survival.

---

## Firmware and Control

Arduino-based firmware evolved from simple servo tests to integrated flapping control with torque and input handling.

Functional modules include:

* Servo motion and flapping generation
* High-torque actuation control
* Precision timing and motion tuning
* Receiver input decoding
* Remote interface handling
* Sensor data acquisition
* OpenLog SD telemetry output

Later “CompleteCode” versions integrate these subsystems into a unified controller.

---

## Wind Sensing and Data Logging

Wind and motion data are recorded as time-series telemetry during flight tests. Logged values include environmental and inertial measurements sampled at ~30–35 Hz and written to SD via OpenLog.

Example telemetry fields:

* Timestamp
* Temperature
* Wind vector components
* Resultant wind magnitude
* Inertial motion (gyro/accel)

These datasets support analysis of aerodynamic response, flapping behavior, and environmental coupling.

---

## Experimental Results

The articulated Eagle prototype demonstrated:

* Stable tethered gliding in natural wind
*  Servo-driven flapping motion
*  Directional control capability
*  Successful onboard wind data logging

Performance confirmed that carbon-fiber spars and metal-gear servos resolved earlier structural and torque limitations.

---

## Repository Structure

```
Flapping_Winged_Glider/
  CAD/                      CAD and 3D-print files
  Field_testing_files/      Wind logs and videos
  Glider-Code/              Arduino control code
    basecode_files/           Building blocks of code files
  Final_Research_Report/    Report, poster, bibliography
```

---

## Hardware Components

Arduino Nano microcontroller <br>
MG92B metal-gear servo motors <br>
Carbon-fiber wing spars <br>
Flexible membrane wing material <br>
OpenLog SD data logger <br>
Environmental and inertial sensors <br>
3D-printed structural mounts and joints

---

## Key Engineering Insights

Flapping torque requirements exceed plastic servo capability <br>
Cyclic bending fatigue dominates mount design constraints <br>
Wing inertia and structural stiffness directly affect control tuning <br>
Wind magnitude strongly influences flapping stability <br>
Lightweight aeroelastic structures outperform rigid frames

---

## Future Work

Integrated multi-sensor suite (temperature, IMU, altimeter) <br>
Wireless telemetry transmission <br>
Improved membrane wing material (nylon fabric) <br>
Permanent sealed electronics enclosure <br>
Closed-loop wind-adaptive flapping control <br>
Expanded wing geometry optimization

---

## Applications

Atmospheric energy harvesting research <br>
Bio-inspired aerial robotics <br>
Lightweight flapping wing design <br>
Wind-assisted flight systems <br>
Environmental sensing platforms <br>

---

## Acknowledgments

FIRE Bio-Inspired Robotics Program <br>
University of Maryland: College Park <br>
Dr. Lena Johnson

---

## License

Educational and research use.
