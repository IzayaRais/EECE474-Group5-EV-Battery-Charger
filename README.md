# Interleaved Boost PFC with Half-Bridge LLC Resonant Converter — EV Battery Charger

<p align="center">
  <img src="figures/circuit_diagram/circuit_render.png" alt="Circuit Diagram" width="720"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Simulation-MATLAB%20Simulink-orange?style=flat-square&logo=mathworks"/>
  <img src="https://img.shields.io/badge/Topology-Interleaved%20Boost%20PFC%20%2B%20LLC-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Application-EV%20Battery%20Charging-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=flat-square"/>
  <img src="https://img.shields.io/badge/Institution-MIST%2C%20Bangladesh-red?style=flat-square"/>
</p>

---

## Table of Contents

- [Overview](#overview)
- [Motivation](#motivation)
- [System Architecture](#system-architecture)
- [Design Specifications](#design-specifications)
- [Stage 1 — Interleaved Boost PFC](#stage-1--interleaved-boost-pfc)
- [Stage 2 — Half-Bridge LLC Resonant Converter](#stage-2--half-bridge-llc-resonant-converter)
- [Control Strategy](#control-strategy)
- [Key Waveforms](#key-waveforms)
- [Simulation Results](#simulation-results)
- [Repository Structure](#repository-structure)
- [How to Run the Simulation](#how-to-run-the-simulation)
- [Tools Used](#tools-used)
- [References](#references)
- [Authors](#authors)

---

## Overview

This project presents the **design and MATLAB Simulink simulation** of a high-efficiency two-stage AC-DC EV battery charger. The system takes standard AC mains input (220 V, 50 Hz) and delivers a regulated DC output suitable for charging electric vehicle battery packs.

The two-stage architecture separates the **power quality correction** (PFC stage) from the **galvanic isolation and output regulation** (LLC stage), enabling each converter to be independently optimized for its function.

---

## Motivation

The rapid global expansion of EV infrastructure demands on-board chargers that are:

- **Efficient** — to minimize heat and maximize range per charge
- **Grid-friendly** — low current harmonics, near-unity power factor to reduce strain on the power grid
- **Safe** — galvanic isolation between the AC grid and the high-voltage battery pack
- **Compact** — high switching frequency enables smaller magnetics and capacitors

The **interleaved boost PFC + half-bridge LLC** topology directly addresses all four requirements and is widely adopted in commercial Level 2 on-board EV chargers.

---

## System Architecture

```
            AC Mains Input
           220 V rms, 50 Hz
                  │
                  ▼
    