# 📘 Estimating Anthropogenic Heat Flux Using Kalman Filter (KF-SEB)

This repository contains the Python implementation of a **Kalman Filter–Surface Energy Balance (KF-SEB)** framework to estimate **urban anthropogenic heat (AH) flux** by assimilating building surface and air temperature observations.

This model was developed as part of the study:

> **Cui, Y., et al. (2025)** – *Estimating anthropogenic heat flux by assimilating meteorological observations with Kalman filter approach* (under review, *Philosophical Transactions A*, Royal Society Publishing)

---

## 🧠 Motivation

Anthropogenic heat is a critical but uncertain component of urban climate systems. Traditional inventory or empirical models suffer from coarse resolution and large uncertainties. This KF-SEB approach aims to reduce estimation uncertainty by incorporating high-resolution meteorological data using a sequential data assimilation scheme.

---

## ⚙️ Model Overview

- **Forward model**: Generates synthetic "observations" (Ts, Tcan) using a simplified urban canopy model with *pre-defined* AH.
- **KF-SEB model**: Solves 1D heat conduction through wall and applies Kalman Filter to assimilate surface and indoor temperatures.
- **AH Estimation**: Reconstructs AH flux via energy balance:  
  \[ AH = H + G - R_n \]

Key Features:
- Discretized heat conduction equation with finite volume method
- Time-varying observational uncertainty (bias & std)
- Supports idealized evaluation with "known truth" for AH

---

## 📁 File Structure

```
KF_augmented_insulated_one_sensor_Yuanfeng_SEB4_UCM250725.ipynb  # Main notebook

```

---

## 🚀 Getting Started

### 1. Clone repository


### 2. Set up environment 


### 3. Run the notebook

Open the notebook in Jupyter or VSCode and run cells in order:

```bash
jupyter notebook KF_augmented_insulated_one_sensor_Yuanfeng_SEB4_UCM250725.ipynb
```

---

## 📊 Inputs & Outputs

- **Input**: Wall surface temperature (`Ts`), indoor temperature (`T_indoor`), net radiation (`Rn`), air temperature (`Tcan`)
- **Output**: Estimated AH flux with associated uncertainty, compared against known true AH

---

## 📎 Dependencies

- `numpy`
- `matplotlib`
- `scipy`
- `math`
- (optionally) `pandas`, `seaborn` for postprocessing

---

## 📌 Limitations

- Designed for synthetic experiments; observational integration (e.g., satellite Ts) not yet implemented
- Assumes access to wall-specific temperatures, which may not be feasible in many real-world datasets
- Neglects latent heat flux (LE) and assumes impervious surface

---

## 📄 Citation

If you use this code, please cite:

```bibtex
@article{Cui2025KFSEB,
  author = {Yuanfeng Cui and Qi Li and Minghan Chu and Zhejun He and John D. Albertson and Zhihua Wang},
  title = {Estimating anthropogenic heat flux by assimilating meteorological observations with Kalman filter approach},
  journal = {Philosophical Transactions A}, 
  year = {2025},
  note = {Under review}
}
```

---

## 👤 Contact

For questions or collaboration inquiries, contact:

**Yuanfeng Cui**  
Cornell University  
Email: yc2554@cornell.edu
