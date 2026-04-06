# Solar Irradiance Prediction Using Machine Learning
**Bachelor's Thesis — Kaunas University of Technology, 2026**

## Research Question
Which machine learning approach best predicts solar irradiance from 
historical weather data, and what factors most influence prediction accuracy?

## Overview
This project investigates the use of machine learning and statistical 
time series methods to predict Global Horizontal Irradiance (GHI) 
using historical hourly weather data from the NSRDB dataset (2022).

The study follows a structured pipeline — from data preprocessing 
and feature engineering through to statistical time series models 
(ARIMA, SARIMA, SARIMAX), classical machine learning models 
(Random Forest, XGBoost), and deep learning (LSTM) — with a final 
comparison of all approaches using RMSE, MAE, and R².

## Dataset
- **Source:** NSRDB (National Solar Radiation Database)
- **Location:** Latitude 40.97, Longitude -4.54 (Spain)
- **Period:** Full year 2022 (8,760 hourly observations)
- **Target variable:** GHI — Global Horizontal Irradiance (W/m²)

## Project Structure
```
solar_thesis/
├── data/                             # Raw dataset (not tracked by Git)
├── notebooks/
│   ├── 01_data_preprocessing.ipynb   # Load, clean, EDA, visualisations
│   ├── 02_feature_engineering.ipynb  # Cyclic encoding, scaling, lag features
│   ├── 03_time_series_models.ipynb   # ARIMA, SARIMA, SARIMAX
│   ├── 04_ml_models.ipynb            # Random Forest, XGBoost
│   ├── 05_deep_learning.ipynb        # LSTM
│   └── 06_results.ipynb              # Final comparison & figures
├── outputs/
│   ├── figures/                      # Saved plots
│   ├── models/                       # Saved trained models
│   └── results/                      # Metrics & comparison tables
└── README.md
```

## Models Compared
| Model | Type |
|---|---|
| Clearsky GHI | Baseline |
| ARIMA | Statistical time series |
| SARIMA | Seasonal time series |
| SARIMAX | Seasonal time series with exogenous variables |
| Random Forest | Classical ML |
| XGBoost | Classical ML |
| LSTM | Deep Learning |

## Dependencies
Anaconda environment (Python 3.x) +
pip install xgboost pmdarima

## Evaluation Metrics
- **RMSE** — Root Mean Squared Error
- **MAE** — Mean Absolute Error
- **R²** — Coefficient of Determination

## Author
Sri Muthusivam Rethinasamy Resikesan Sathiya
BSc Informatics (Internet Informatics)
Kaunas University of Technology, 2026
