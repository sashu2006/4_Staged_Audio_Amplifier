# 4-Stage Audio Amplifier Design and Simulation

## Overview
This repository contains the complete design, simulation, and analysis of a custom 4-Stage Audio Amplifier. Developed as part of the academic curriculum at IIIT Hyderabad, this project focuses on cascading multiple transistor stages to take a weak input audio signal and amplify it sufficiently to drive a low-impedance speaker load with high fidelity and minimal distortion.

## Key Features
* **Architecture:** 4 distinct cascading stages (Pre-amp, Voltage Amplifier, Driver, and Power Output).
* **Power Stage:** Class AB Push-Pull configuration to maximize efficiency while eliminating crossover distortion.
* **Verification:** Comprehensive AC sweep (frequency response) and transient analysis to verify gain and Total Harmonic Distortion (THD).
* **Tools:** LTspice / NGSPICE for complete circuit simulation and waveform analysis.

## 🧠 Design Architecture (The 4 Stages)
Designing a multi-stage amplifier requires strict attention to impedance matching and inter-stage loading. The architecture is broken down as follows:

1. **Stage 1: Preamplifier (Input Stage)**
   * **Purpose:** Provides a high input impedance to prevent loading the audio source and delivers the initial voltage gain.
   * **Configuration:** typically a Common-Emitter or differential pair optimized for low noise.

2. **Stage 2: Voltage Amplifier Stage (VAS)**
   * **Purpose:** Delivers the bulk of the voltage gain required by the system.
   * **Design Focus:** Maximizing gain bandwidth while keeping harmonic distortion in check.

3. **Stage 3: Driver Stage**
   * **Purpose:** Acts as a buffer between the high-impedance VAS and the heavy load of the power stage. Provides necessary current gain.

4. **Stage 4: Power Amplifier (Output Stage)**
   * **Purpose:** Delivers massive current to drive an 8Ω or 4Ω speaker load.
   * **Configuration:** Class AB Push-Pull topology using complementary BJTs/MOSFETs. Biased carefully using diodes or a Vbe multiplier to eliminate crossover distortion.

## Performance Metrics
* **Frequency Response:** Engineered for a flat response across the standard human audio spectrum (20 Hz - 20 kHz).
* **Distortion:** Careful biasing and feedback mechanisms implemented to keep THD as low as possible at maximum output swing.
* *(Note: Refer to the project report for exact numerical values regarding Voltage Gain (Av), Bandwidth, and THD percentages).*

## Documentation
The complete design methodology, DC biasing calculations, AC frequency response Bode plots, and transient simulation waveforms are discussed in detail in the project report (`Audio_Amplifier_Report-4.pdf`).

## Repository Structure
```text
4_Staged_Audio_Amplifier/
├── simulations/                     # LTspice/NGSPICE circuit schematic files (.asc, .net)
├── waveforms/                       # Exported plots (Bode plots, transient signals)
├── Audio_Amplifier_Report-4.pdf     # Detailed project report and mathematical analysis
└── README.md                        # Repository documentation