---
title: 📄 Draft – Pb-free ScAlN MEMS Array × 65 nm SiGe CMOS × SiP for Medical Ultrasonic Sensors
---

# Introduction

Medical ultrasonic imaging is widely used in **ophthalmology, vascular diagnosis, dermatology, and implantable monitoring**.  
Traditional devices have been dominated by **PZT (Pb(Zr,Ti)O₃)** because of its superior piezoelectric properties.  
However, the **toxicity of Pb** has become a serious limitation for **in-body medical applications**, as regulated by **EU RoHS, REACH, and FDA**.  

As a result, there is an urgent demand for **Pb-free alternatives** that can provide comparable performance while ensuring **biocompatibility and regulatory compliance**.  
Several materials have been investigated, including KNN, BNT, ZnO, and PVDF.  
Among these, **Scandium-doped Aluminum Nitride (ScAlN)** has emerged as the **most promising candidate** due to its:  

- Compatibility with **CMOS processes** (low deposition temperature, sputtering)  
- **High Q** and suitable piezoelectric properties for **RF and ultrasonic frequencies**  
- Demonstrated industrial adoption in **RF BAW/XBAR filters**  

This work proposes a **Pb-free ScAlN MEMS ultrasonic array**, co-integrated with a **65 nm SiGe CMOS front-end** via **System-in-Package (SiP)** technology, as a practical solution for next-generation medical ultrasound sensors.  

---

# System Concept

## ScAlN MEMS Array
- Frequency range: **10–50 MHz** (targeting high-resolution medical imaging).  
- Array size: **64–256 channels**, designed with **λ/2 pitch rule**.  
- Structures: **PMUT-like thin-film stack** or **BAW/XBAR resonant cavity** for improved Q.  

## SiGe CMOS Front-end
- Technology: **65 nm SiGe BiCMOS**, offering **low noise figure (< 2 dB)** and wideband operation.  
- Blocks: **LNA, VGA, ADC, T/R switch**, optimized for microvolt-level signal detection.  
- Integration: Analog front-end placed **directly adjacent to MEMS array** to minimize interconnect losses.  

## System-in-Package (SiP) Integration
- Assembly: **Flip-chip bonding** of MEMS and CMOS dies, with underfill and redistribution if needed.  
- Benefits:  
  - **Yield separation** (independent MEMS and CMOS fabrication)  
  - **Short interconnects** → improved SNR  
  - **Hermetic sealing** for medical-grade reliability  

---

# Simulation Results

## Finite Element Method (FEM) Analysis
- Modeled **ScAlN MEMS cells** with λ/2 pitch at 20, 30, and 40 MHz.  
- Results show:  
  - **Resonant frequencies** aligned with design target.  
  - **Effective electromechanical coupling (k²_eff)** in the range of 2–4%.  
  - **Acoustic beam patterns** demonstrating expected directivity for 64- and 128-channel arrays.  

## Circuit Simulation
- Modeled **LNA with input-referred noise < 2 nV/√Hz**.  
- System-level SPICE simulation including MEMS capacitance, interconnect parasitics, and ADC quantization.  
- Achieved **SNR > 60 dB** for 20–40 MHz operation with 64-channel beamforming.  

---

# Application Scenarios

## Ophthalmology
- **20–40 MHz ScAlN MEMS array** provides high-resolution imaging of the anterior eye.  
- Potential replacement for PZT-based **Ultrasound Biomicroscopy (UBM)** with Pb-free compliance.  

## Vascular Imaging (IVUS)
- **Catheter-integrated arrays** at 30–40 MHz for intravascular ultrasound.  
- Pb-free approach reduces toxicity concerns for long-term implantable devices.  

## Dermatology and Oncology
- **10–20 MHz wide-aperture arrays** for non-invasive imaging of skin layers and tumor boundaries.  
- Portable, battery-powered devices enabled by low-power SiGe CMOS.  

## Implantable Monitoring
- Miniaturized **SiP package** with wireless telemetry.  
- Continuous monitoring of blood flow or tissue elasticity in chronic disease management.  

---

# Expected Contributions
1. Demonstration of a **Pb-free ultrasonic array technology** for medical applications.  
2. A practical **co-integration scheme** of MEMS and SiGe CMOS using SiP.  
3. Establishing **design guidelines** for pitch, frequency, and front-end electronics for high-resolution imaging.  
4. Application scenarios in **ophthalmology, vascular imaging, dermatology, and implantable monitoring**.  

---
