# EPFL ME-428 Fall 2024 Final Project: Strength‑to‑Weight Optimization of Spider‑Web Structures


## 📋 Project Overview

This repository hosts the final project for **ME‑428: Advanced Structural Optimization** at EPFL, supervised by Prof. Josie Hughes. Inspired by the efficiency of natural spider webs, we developed a data‑driven workflow to **maximize the strength‑to‑weight ratio** of bioinspired web geometries.
In simple terms, we taught MATLAB and Python to weave the perfect digital "web" that holds the most weight while using the least material—much like choosing the fewest silk threads to build the strongest net.

## 🚀 Core Workflow

1. **Design Parameter Sampling**: MATLAB draws four discrete variables—radial/spiral thread counts and radii—using Latin Hypercube Sampling (LHS).
2. **CAD Automation**: A Python script drives SolidWorks to generate 2D sketches and export STEP geometries for each design.
3. **Finite‑Element Analysis**: ANSYS Mechanical applies boundary conditions and central loading to compute maximum load capacity for TPU webs.
4. **Bayesian Optimization Loop**: MATLAB’s Gaussian Process surrogate and an Expected Improvement + acquisition function balance exploration/exploitation over 20 costly FEA runs.
5. **Convergence**: The pipeline identifies the optimal web: 5 radial, 5 spiral threads, 2.5 mm radial radius, 0.5 mm spiral radius—yielding an S/W ratio of **13 225**.


## 📈 Key Results

* **Optimal Design**: 5 radial & 5 spiral threads, radii 2.5 mm & 0.5 mm
* **Strength‑to‑Weight**: **13 225** (N/kg)
* **FEA Precision**: Load capacity converges within ±0.1 MPa over 20 runs
* **Design Trend**: Minimal thread counts and radii yield highest efficiency, mirroring how spiders often use few, thick strands for structural support.

## 👤 Authors & Acknowledgments

* **Wieland M. Apel**, **Yo‑Shiun Cheng**, **Tassilo Friberg**
* **Supervisor:** Prof. Josie Hughes, EPFL

Thanks to the SolidWorks and ANSYS API teams for automation guidance.
