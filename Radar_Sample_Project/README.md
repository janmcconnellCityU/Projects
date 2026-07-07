# 📡 Synthetic Radar Signal Analysis

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)

A synthetic data analysis project exploring whether unusually weak radar signals can be identified relative to the expected relationship between signal strength and target distance.

## 🔍 Analytical Question

**Can unusually weak radar signals be identified relative to the expected relationship between signal strength and target distance?**

Radar signal strength naturally decreases as target distance increases. As a result, a weak signal is not necessarily abnormal simply because its measured strength is low.

This project compares observed signal strength with the signal strength expected for a target's distance from the radar. The goal is to distinguish normal distance-related attenuation from observations that may warrant further investigation.

## 📊 Project Overview

The project generates 500 synthetic radar observations containing:

- Timestamp
- Three-dimensional target coordinates (`x`, `y`, and `z`)
- Target velocity
- Calculated distance from the radar origin
- Simulated signal strength

A simplified distance-based signal attenuation model is used to generate expected signal strength. Random measurement noise is added to represent normal variation.

Fifteen known weak-signal anomalies are intentionally injected into the dataset. These known anomalies provide ground truth for evaluating the detection method.

> **Note:** The simulated signal model is intentionally simplified for data analysis and demonstration purposes. It is not intended to represent a complete physical radar model.

## ⚙️ Anomaly Detection Method

Expected signal strength is calculated as a decreasing function of target distance.

For each observation, a signal residual is calculated as the difference between observed and expected signal strength:

`Signal Residual = Observed Signal Strength - Expected Signal Strength`

An observation is flagged as anomalous when its signal residual is more than three standard deviations below the mean residual.

This approach accounts for the expected effect of distance rather than relying on a fixed signal-strength threshold.

## 📈 Results

The anomaly detection method:

- Detected **14 of 15** intentionally injected anomalies
- Identified approximately **93.3%** of the known anomalies
- Produced **0 false positives**
- Missed **1 injected anomaly**

Normal observations generally followed the expected decrease in signal strength as target distance increased. Detected anomalies fell substantially below the expected signal curve.

The results demonstrate why a fixed signal-strength threshold can be misleading. A low signal strength may be normal for a distant target, while the same signal strength may be unexpectedly weak for a closer target.

## 🛠 Tools and Libraries

- Python
- pandas
- NumPy
- Matplotlib
- Jupyter Notebook

## 📁 Repository Contents

```text
Radar_Sample_Project/
├── 00_generate_sample_data.ipynb
└── README.md