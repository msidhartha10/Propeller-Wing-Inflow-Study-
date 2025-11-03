# Propeller-Wing Inflow Study

## Overview

This repository contains code, case setups, data, and analysis scripts for studying the aerodynamic interaction between a propeller (rotor) and a wing — commonly referred to as propeller-wing inflow interaction. The goal is to analyze how the propeller wake and inflow affect wing loading, lift/drag characteristics, and local flow features (velocity, vorticity, pressure) across a range of operating conditions.

This project is intended to support:
- CFD simulations (e.g., OpenFOAM / other solvers)
- Reduced-order / analytic models of propeller inflow
- Post-processing and visualization of the wake and wing aerodynamic response
- Reproducible case setups for parametric studies

---

## Key features

- Structured repository layout for simulation cases and scripts
- Scripts for pre-processing and post-processing (Python / MATLAB placeholders)
- Sample case(s) demonstrating propeller–wing interactions
- Jupyter notebooks for data analysis and plotting (if present)
- Guidance and templates to reproduce results and extend studies

---

## Motivation

Propeller-wing interaction is important in:
- Small unmanned aircraft and VTOL concepts where propellers are placed near or in front of lifting surfaces
- Propeller installation effects on wing aerodynamics and noise
- Design optimization for performance and stability

This repository centralizes the tools and case configurations needed to investigate and reproduce physical and numerical phenomena associated with propeller inflow.

---

## Requirements

The exact requirements depend on the solver and scripts used in your cases. Typical dependencies:

- CFD solver (one or more; install and configure separately)
- Ansys Fluent / Star CCM +
- MATLAB 

