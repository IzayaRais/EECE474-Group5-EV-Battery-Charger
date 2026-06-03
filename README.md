# EECE 474 — Group 5: Interleaved Boost PFC with Half-Bridge LLC Resonant Converter-Based EV Battery Charger

**Course:** EECE 474 — Power Electronics  
**Institution:** Military Institute of Science and Technology (MIST), Dhaka, Bangladesh  
**Group:** 05

---

## Project Overview

This project presents the design and simulation of a two-stage EV battery charger:

1. **Stage 1 — Interleaved Boost PFC (Power Factor Correction):** Converts AC mains input to a regulated DC link voltage while achieving near-unity power factor and low THD.
2. **Stage 2 — Half-Bridge LLC Resonant Converter:** Provides galvanic isolation and regulated DC output suitable for EV battery charging, operating at resonant frequency for high efficiency.

The full system is modeled and simulated in **MATLAB Simulink**.

---

## Repository Structure

```
.
├── report/
│   └── Group05_Report.pdf              # Final project report
├── presentation/
│   ├── Group05_Presentation.pptx       # Final presentation slides
│   └── EECE474_Presentation_Template.pptx
├── simulation/
│   └── EV_Charger_Simulink_Model.slx   # MATLAB Simulink model
├── figures/
│   ├── circuit_diagram/                # Circuit schematics (Visio, PNG)
│   └── waveforms/
│       ├── svg/                        # Waveform exports (SVG)
│       └── png/                        # Waveform exports (PNG, 150 dpi)
├── references/
│   └── Interleaved_Boost_PFC_LLC_EV_Charger_Reference.pdf
└── README.md
```

---

## Key Waveforms

| Waveform | Description |
|----------|-------------|
| `PE_DC_Link` | DC link voltage across the PFC output capacitor |
| `PE_I_and_V` | Input AC current and voltage (PFC stage) |
| `PE_IIR` | Interleaved inductor currents (IL1, IL2) |
| `PE_Vs` | Switching node voltage |
| `il1`, `il2` | Individual boost inductor currents |
| `llm1` | LLC resonant inductor current |

---

## Tools Used

- **MATLAB Simulink** — System simulation (`.slx` model)
- **Microsoft Visio** — Circuit diagram drafting (`.vsdx`)
- **Adobe Illustrator** — Waveform figure preparation (`.ai`)

---

## How to Run the Simulation

1. Open MATLAB (R2021a or later recommended).
2. Navigate to the `simulation/` folder.
3. Open `EV_Charger_Simulink_Model.slx`.
4. Run the simulation (Ctrl+T or the Run button).
5. Observe waveforms on the Scope blocks.

---

## Reference

> *Interleaved Boost PFC with Half Bridge LLC Resonant Converter based EV Battery Charger* — see `references/` folder for the source paper.

---

## Authors

- Group 05, EECE 474 — Power Electronics, MIST
