# Optimal 2.0 GHz Low Noise Amplifier (LNA) Design

This repository contains the complete design workflow and simulation results of a single-stage Low Noise Amplifier (LNA) targeted at boosting weak RF signals in the 1.8–2.6 GHz band. The design was developed using industry-standard RF design methodologies and simulated using Keysight Advanced Design System (ADS).

## 📡 Project Overview

The LNA was designed to:
- Amplify low-level RF signals with minimal added noise
- Maintain unconditional stability across the operational band
- Achieve optimal tradeoff between gain, noise figure, and stability

**Key Specs:**
- Center Frequency: 2.0 GHz  
- Achieved Gain: 14.02 dB  
- Minimum Noise Figure (NFmin): 0.83 dB  
- Stability (Mu > 1): Achieved via custom stabilization network

## ⚙️ Features

- **Transistor Selection:** ATF-21170 GaAs FET (modeled using S-parameters)
- **Stability Analysis:** Mu and Mu’ factors simulated in ADS
- **Biasing:** Active biasing network for thermal and electrical stability
- **Matching Networks:** Lumped-element IMN & OMN designed using Smith Chart
- **Simulation Tools:** Keysight ADS 2020 with gain & NF circles, load-pull analysis

## 🧪 Design Methodology

1. **S-Parameter Verification** — Confirmed ADS model fidelity with datasheet  
2. **Biasing & Stability** — Engineered for Vds = 3 V, Ids = 20 mA; achieved unconditional stability  
3. **Impedance Matching** — Designed with Smith Chart utility to align Γs & ΓL  
4. **Simulation Passes** — 10 iterations optimizing gain, NF, and Mu simultaneously  
5. **Final Result** — Stable and high-gain performance verified at 2.0 GHz

## 📖 References

- Gonzalez, G. *Microwave Transistor Amplifiers: Analysis and Design*
- Keysight ADS Documentation  
- ATF-21170 Datasheet  
- IEEE ICMRSISIT 2019 Conference Paper

## 📬 Contact

For any queries, feel free to reach out:
- Achutha Thyagaraju  
- 📧 achuthathyagaraju@gmail.com  
