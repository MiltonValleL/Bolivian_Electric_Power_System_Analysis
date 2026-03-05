# 🧠 BOL-SIN: Predictive Analytics for Grid Stability & Inertia Forecasting

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.7%20Nightly-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-Winner_Model-008080?style=for-the-badge&logo=xgboost&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-12.4-76B900?style=for-the-badge&logo=nvidia&logoColor=white)

<br>

## 📌 Project Executive Overview
As the **Bolivian National Interconnected System (SIN)** integrates more Variable Renewable Energy (VRE), the reduction of **Equivalent System Inertia ($H_{sys}$)** poses a significant threat to grid stability. 

This project delivers an advanced predictive framework to forecast $H_{sys}$ margins with high precision. Using 16 years of operational data (2010-2026), I developed a multi-stage pipeline that balances computational efficiency with industrial-grade accuracy.

<br>

## 🚀 Key Performance Indicators (KPIs)
| Metric | Linear Regression | **XGBoost (Champion)** | LSTM (Deep Learning) |
| :--- | :---: | :---: | :---: |
| **MAE (Seconds)** | 0.0554 | **0.0483** | 0.0675 |
| **RMSE (Seconds)** | 0.0809 | **0.0668** | 0.0887 |
| **R² Score** | 0.8494 | **0.8976** | 0.8194 |

**Strategic Outcome:** The XGBoost model provides a **12.73% improvement** in error reduction over the baseline, ensuring a robust safety buffer for the **3.5s stability limit**.

<br>

## 🏗️ High-Performance Computing (HPC) Stack
To handle over **140,000 hourly records** and train deep architectures, I utilized a high-end workstation:
* **CPU:** AMD Ryzen 7 9800X3D (8C/16T).
* **RAM:** 96GB DDR5.
* **GPU:** **NVIDIA GeForce RTX 5070 Ti (16GB)**.
* **MLOps:** PyTorch Nightly with **SM_120 (Blackwell)** architecture support.

<br>

## 📊 Strategic Visualizations & Technical Insights

### 1. Model Tracking Fidelity
The visualization below confirms the model's exceptional ability to "track" the daily inertia valleys caused by solar displacement during the **2026 validation period**.

![System Inertia Tracking](./images/22.System_Inertia_Tracking(winner_model).jpg)

> **Finding:** The model exhibits high stability during transient morning ramps (06:00-09:00), where VRE penetration typically compromises synchronous mass.

### 2. Feature Attribution (Interpretability)
We moved beyond "black-box" modeling by analyzing the gain-based importance of each variable.

![XGBoost Feature Importance](./images/image_9fb82a.png)

> **Finding:** **h_sys_equivalent_lag_1** accounts for **70.01%** of the predictive weight. This statistically validates the "Temporal Momentum" of the power grid.

### 3. Global Benchmarking
A comparative analysis of the three architectures explored during the project.

![Final Model Benchmarking](./images/23.Final_Model_Benchmarking(predictive_accuracy).png)

> **Finding:** Despite the complexity of the LSTM, **XGBoost** emerged as the superior choice due to its ability to exploit high-autocorrelation features in tabular time-series data.

<br>

## 🛠️ Advanced Methodology
To ensure world-class standards, I implemented:
* **Cyclical Time Encoding:** Sine/Cosine transformations for hours and months to preserve periodic continuity.
* **StandardScaler Calibration:** Scaling fitted *only* on training data (2010-2024) to eliminate **Data Leakage** in the 2025-2026 test set.
* **Recursive Lag Engineering:** Integration of $t-24$ and $t-168$ features to capture circadian and weekly seasonality.

<br>

## 🤝 Professional Contact
Specialized in **Data Science & Machine Learning** for critical infrastructure and power systems.

**LinkedIn:** [Milton Rodolfo Valle Lora](https://www.linkedin.com/in/miltonvallelora/)  
**YouTube:** [DataScienceByDoing](https://www.youtube.com/@DataScienceByDoing)

---
**Analyzed by: Milton R. Valle Lora** *March 2026*

---
