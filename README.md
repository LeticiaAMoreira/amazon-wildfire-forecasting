# Forecasting Wildfires in the Amazon: Integrating Lagged Dependence Analysis, Complex Networks, and Machine Learning

[![Conference](https://img.shields.io/badge/Accepted-BDCAT%202026-blue)](#)
[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](#)
[![License](https://img.shields.io/badge/License-MIT-green)](#)

Official repository for the paper **"Forecasting Wildfires in the Amazon: Integrating Lagged Dependence Analysis, Complex Networks, and Machine Learning"**, accepted at the IEEE/ACM BDCAT 2026 conference.

## 📌 Overview
The volume of spatiotemporal data has grown significantly, requiring advanced methods to support environmental monitoring. This repository contains the data processing pipeline, network extraction algorithms, causal discovery analysis, and machine learning models used to forecast the continuous magnitude of fire outbreaks in the Amazon basin (2003–2025).

The methodological pipeline integrates:
1. **Chronological Networks (Chronnets):** Modeling spatial fire propagation using MODIS satellite detections.
2. **Lagged Conditional Dependence (PCMCI):** Identifying statistically supported delayed associations between macroclimatic anomalies (e.g., ENSO), local weather, and anthropogenic exposure.
3. **Machine Learning Forecasting:** Multi-horizon magnitude prediction using Negative Binomial (NB2), Random Forest, XGBoost, Multilayer Perceptron (MLP), and SARIMAX models evaluated under a rolling chronological cross-validation design.

## 📂 Repository Structure
```text
├── datasets/
│   ├── fire_graph_metrics.csv       # NASA MODIS fire hotspots and Chronnet topological metrics
│   └── integrated_analysis.csv      # Single unified dataset used for correlation, PCMCI, and forecasting
├── scripts/
|   ├── 01_network_extraction.ipynb  # Fire graph metrics
│   ├── 02_correlation.ipynb         # Spearman correlation matrix generation
│   ├── 03_causality_pcmci.ipynb     # Lagged conditional dependence tests (ParCorr, GPDC, Spearman)
│   └── 04_prediction_models.ipynb   # Rolling-window validation for NB2, RF, XGBoost, MLP, SARIMAX
├── requirements.txt                 # Python dependencies
└── README.md
