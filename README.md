# Dhaka AQI Forecasting

## Project Overview

This repository contains the original and revised research code for the study:

**Incremental Value of Meteorological Predictors for Next-Day Air Quality Index Forecasting in Dhaka Using Tree-Based Ensemble Models.**
The study evaluates whether meteorological predictors provide additional value beyond historical pollutant information for next-day daily Air Quality Index (AQI) forecasting in Dhaka, Bangladesh, using daily data from 2023 to 2025.

## Research Objectives

- Evaluate the incremental value of meteorological predictors.
- Compare pollutant-only and pollutant-plus-meteorological feature sets.
- Assess forecasting performance using chronological evaluation.
- Examine the robustness and seasonal variation of model performance.

## Feature Scenarios

- **S1:** Historical pollutant features (AQI, PM2.5, and PM10) with lags 0, 1, and 2.
- **S2:** S1 features plus meteorological variables (temperature, rainfall, and wind speed) with lags 0, 1, and 2.

## Models

The study evaluates:

- Random Forest
- XGBoost
- LightGBM
- Linear Autoregressive Model (ARX)

Baseline methods include persistence, seasonal naive-7, and climatology.

## Data and Evaluation

The study uses daily observations covering 1 January 2023 to 31 December 2025.

Chronological data splitting:
- Training: 4 January 2023 – 30 June 2024 (544 samples)
- Validation: 1 July 2024 – 31 December 2024 (184 samples)
- Testing: 1 January 2025 – 31 December 2025 (365 samples)

Additional analyses include:
- Diebold–Mariano tests
- Paired block bootstrap
- Random seed stability
- Fixed-configuration ablation
- Rolling-origin evaluation
- Seasonal performance analysis
- Meteorological and pollutant lag sensitivity
- Grouped permutation importance
- AQI reconstruction diagnostics

## Repository Contents

- `Dhaka_AQI_Forecasting_Revised.ipynb`: Original and revised research code, including model development, evaluation, robustness checks, and figure generation.

## Software Environment

The revised analysis was run using:

- Python 3.13.18
- pandas 2.2.3
- NumPy 2.4.6
- scikit-learn 1.6.1
- XGBoost 3.4.1
- LightGBM 4.6.0

## How to Run

1. Open the notebook using Google Colab.
2. Obtain the dataset from its original source.
3. Upload the dataset and configure the CSV file path.
4. Install the required Python packages if they are not already available.
5. Run the notebook cells sequentially.

## Reproducibility

The notebook includes the original analysis and subsequent revisions, together with model evaluation, statistical tests, robustness checks, and visualization procedures.

The dataset is not redistributed in this repository. Users should obtain it from its original source.

## Code Availability

The complete research code is publicly available in this GitHub repository:

https://github.com/putriikrima2/Dhaka-AQI-Forecasting
