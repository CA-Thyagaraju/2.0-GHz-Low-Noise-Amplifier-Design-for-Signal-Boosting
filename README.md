# Optimal 2 GHz Low Noise Amplifier (LNA) Design

This repository presents the complete design and simulation workflow of a **single-stage Low Noise Amplifier (LNA)** developed to amplify weak RF signals in the **1.8–2.6 GHz band**. The amplifier was designed using standard microwave design methodology and simulated using **Keysight Advanced Design System (ADS)**.

The objective of the design was to achieve **high gain, low noise figure, and unconditional stability** while maintaining practical biasing and matching networks suitable for hardware implementation.

---

# 📡 Project Overview

The LNA was designed to:

- Amplify low-power RF signals with minimal added noise  
- Maintain **unconditional stability across the operating band**  
- Achieve an optimal trade-off between **gain, noise figure, and stability**

### Key Performance Metrics

| Parameter | Value |
|-----------|------|
| Center Frequency | **2.0 GHz** |
| Small Signal Gain (S21) | **≈ 14 dB** |
| Minimum Noise Figure | **≈ 0.83–0.93 dB** |
| Input Return Loss (S11) | **≈ −14 dB** |
| Output Return Loss (S22) | **≈ −22 dB** |
| Stability Factor (μ, μ′) | **> 1 across band** |

---

# ⚙️ Design Features

### Transistor Selection

The amplifier uses the **ATF-21170 GaAs FET**, chosen for its:

- Low intrinsic noise
- High gain at microwave frequencies
- Accurate S-parameter models available for simulation

---

### Stability Network

A stabilization network consisting of:

- Gate damping resistor  
- Source inductive degeneration  

was implemented to ensure **unconditional stability**, verified using **Mu (μ) and Mu-prime (μ′) stability factors**.

---

### Biasing Network

The transistor was biased at:

Vds = 3 V

Ids ≈ 20 mA


RF chokes and DC blocking capacitors were used to isolate the RF and DC paths while maintaining proper biasing conditions.

---

### Matching Networks

Both **Input Matching Network (IMN)** and **Output Matching Network (OMN)** were designed using the **Smith Chart Utility in ADS**.

The matching networks were implemented using lumped elements:

- Inductors for impedance transformation
- Capacitors for DC blocking and reactive tuning

This ensured the source and load impedances were transformed close to their **optimal reflection coefficients (Γs and ΓL)**.

---

# 🧪 Design Methodology

The LNA was developed using the following RF design workflow:

### 1. S-Parameter Validation

The ATF-21170 transistor model in ADS was verified against the datasheet to ensure accurate simulation behavior.

### 2. Bias Point Selection

A bias point of **Vds = 3 V and Ids ≈ 20 mA** was selected to balance gain and noise performance.

### 3. Stability Analysis

Stability was analyzed using:

- **Mu (μ) factor**
- **Mu-prime (μ′) factor**

A stabilization network was introduced until **μ > 1 across the frequency band**, ensuring unconditional stability.

### 4. Impedance Matching

Input and output matching networks were synthesized using the **Smith Chart utility**, aligning the circuit with:
Γs ≈ Γopt (for low noise operation)
ΓL optimized for power gain


### 5. Iterative Optimization

Multiple simulation passes were performed to optimize:

- Gain (S21)
- Noise Figure (NF)
- Input/Output Return Loss
- Stability

---

# 📊 Final Performance

The final LNA achieved:

- **~14 dB small-signal gain at 2 GHz**
- **Noise figure below 1 dB**
- **Good input and output impedance matching**
- **Unconditional stability across the band**

This demonstrates an effective balance between **low noise performance, gain, and stable operation**.

---

# 📖 References

- Gonzalez, G. *Microwave Transistor Amplifiers: Analysis and Design*  
- Keysight **Advanced Design System (ADS) Documentation**  
- **ATF-21170 Datasheet**  
- IEEE **ICMRSISIT 2019 Conference Paper**

---

# 📬 Contact

**Achutha Thyagaraju**  
Electrical Engineering  
NIT Rourkela  

📧 achuthathyagaraju@gmail.com
