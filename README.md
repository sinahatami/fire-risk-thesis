# Wildfire Risk Prediction & Analysis

![Project Status](https://img.shields.io/badge/status-active-brightgreen.svg)
![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)
![License](https://img.shields.io/badge/license-MIT-blue.svg)

## 📌 Overview

This repository contains the research and implementation for predicting and analyzing wildfire risks using geospatial data and machine learning algorithms. **This project is conducted as part of a final dissertation at the University of Geneva.** The thesis explores the synergy between climate reanalysis data (ERA5), vegetation indices (NDVI), and advanced predictive modeling to create robust fire risk assessment systems.

## 🗂️ Project Structure

The repository is structured to adhere to industry best practices for data science projects, separating data acquisition, processing, and modeling phases.

```text
fire-risk-thesis/
├── notebooks/
│   ├── data_collection/
│   │   ├── ERA5.ipynb             # Extraction and processing of ECMWF ERA5 climate data
│   │   └── NDVI.ipynb             # Calculation and integration of Normalized Difference Vegetation Index
│   ├── preprocessing/
│   │   └── pre-train.ipynb        # Data cleaning, feature engineering, and dataset preparation
│   └── modeling/
│       ├── model_training.ipynb   # Comprehensive model training (Random Forest, XGBoost, Deep Learning)
│       └── train.ipynb            # Lightweight/experimental training script
├── .gitignore                     # Git tracking exclusions
├── requirements.txt               # Project dependencies
└── README.md                      # Project documentation
```

## 🛠️ Technologies & Libraries

- **Geospatial Analysis:** `rasterio`, `xarray`
- **Data Manipulation:** `pandas`, `numpy`
- **Machine Learning:** `scikit-learn`, `xgboost`
- **Deep Learning:** `tensorflow` (with specialized loss functions like `focal-loss` for class imbalance)
- **Visualization:** `matplotlib`, `seaborn`

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/sinahatami/fire-risk-thesis.git
cd fire-risk-thesis
```

### 2. Set up the environment

It is recommended to use a virtual environment to manage dependencies.

```bash
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run Notebooks

Start Jupyter Notebook or Jupyter Lab to explore the project.

```bash
jupyter notebook
```
Navigate to the `notebooks/` directory and execute the notebooks in the following order:
1. `data_collection/`
2. `preprocessing/`
3. `modeling/`

## 📊 Methodology

1. **Data Collection:** Integrating meteorological variables (temperature, precipitation, wind) from ERA5 and vegetation health (NDVI) from satellite imagery.
2. **Preprocessing:** Handling missing values, aligning spatial resolutions, and engineering predictive features.
3. **Modeling:** Training various models including tree-based ensembles (Random Forest, XGBoost) and neural networks. Focal loss is employed to address the inherent class imbalance in fire occurrence data.
4. **Evaluation:** Assessing models using relevant metrics like Precision, Recall, F1-Score, and ROC-AUC.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.
