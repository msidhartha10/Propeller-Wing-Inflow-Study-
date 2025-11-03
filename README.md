# Propeller–Wing Inflow Study

## 🧩 Overview

This repository contains code, CFD setups, data, and analysis scripts for investigating the **aerodynamic interaction between a propeller and a wing**, commonly known as *propeller–wing inflow interaction*.  
The study aims to quantify how the propeller wake and induced inflow modify local flow structures, lift and drag characteristics, and pressure distributions across a range of operating conditions.

This project supports:
- High-fidelity **CFD simulations** (ANSYS Fluent / OpenFOAM / Star-CCM+)
- **Analytical and reduced-order models** for propeller inflow
- **MATLAB-based slipstream computation** and visualization
- Reproducible case setups for **parametric and validation studies**

---

## 🚀 Motivation

Propeller–wing interaction is critical in modern aircraft configurations such as:
- **VTOL and eVTOL platforms**, where propellers are placed in front of or over wings
- **Distributed electric propulsion (DEP)** systems
- **STOL aircraft**, where inflow effects alter lift and stability  
Understanding these effects is essential for accurate aerodynamic modeling, improved performance, and noise mitigation.

---

## ⚙️ Key Features

- Structured repository layout for **2D and 3D CFD case setups**
- **MATLAB slipstream model** for analytical inflow prediction and visualization
- Scripts for **pre-processing and post-processing** (Python / MATLAB)
- Example **CFD case files** with journal scripts for Fluent
- **Jupyter notebooks** for post-processing, data fitting, and plotting
- Reference papers and validation datasets for reproducibility

---

## 🧪 Methodology

### 1. 2D Airfoil Validation (NACA 0012)
- Performed steady and unsteady CFD simulations at **Re ≈ 2×10⁵**
- Structured **C-type mesh** with wall-resolved inflation layers ($y^+ < 1$)
- Compared **k–ω SST** and **Transition SST (γ–θ)** models
- Validated against:
  - *Michna & Rogowski (2022)* — *Effect of Reynolds Number and Turbulence Intensity on NACA 0018 Performance*
  - *Choudhry et al. (2015)* — *Long Separation Bubble on Thick Airfoils and Its Effects*
- Found that **transition modeling** is essential to capture laminar separation bubbles and match experimental trends.

### 2. MATLAB Slipstream Modeling
- Computed **induced velocity (Vᵢ)** and **advance ratio (J)** for propeller inflow.  
- Modeled **slipstream contraction radius (Rₛ(x))**, wake shape, and induced velocity profiles.
- Generated inflow velocity components (u, v, w) for different AoAs.  
- Produced **3D visualizations of the slipstream tube** and **tabulated velocity distributions** for CFD boundary setup.

### 3. 3D Unsteady CFD of Propeller–Wing Configuration
- Simulated a **finite wing with a rotating propeller** in front.
- Approach: **URANS (k–ω SST)** using **MRF/sliding mesh** framework.
- Extracted **lift, drag, and moment coefficients** ($C_L$, $C_D$, $C_m$) under propeller-induced inflow.
- Analyzed **wake–wing interaction**, pressure field distortion, and induced flow gradients.

---

## 🧰 Tools & Software

- **ANSYS Fluent** — 2D and 3D CFD simulation (steady + unsteady, MRF/sliding mesh)
- **MATLAB** — Slipstream modeling, induced velocity analysis, and visualization
- **Python** — Data parsing, plotting, and regression
- **Tecplot / ParaView** — Post-processing and field visualization

---

## 📊 Key Results

- Transition SST captured laminar separation bubbles accurately, improving $C_L$ prediction by ~8% over k–ω SST.
- MATLAB inflow model provided accurate **induced velocity and slipstream geometry** for CFD coupling.
- 3D unsteady CFD quantified **propeller-induced lift enhancement** and **wake–wing aerodynamic interference**.
- Framework enables **hybrid analytical + CFD modeling** for distributed-propulsion and VTOL applications.


---

## 📈 Future Work

- Extend to **multi-propeller configurations** and **non-uniform inflow fields**
- Couple with **aero-structural solvers** for flexible wing deflection studies
- Include **experimental validation** for slipstream and pressure distribution mapping


