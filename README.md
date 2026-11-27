# Dhaka AQI Forecasting

## Project Overview

This repository contains the research code and dataset used in the study:

**Incremental Value of Meteorological Predictors for Next-Day Air Quality Index Forecasting in Dhaka Using Tree-Based Ensemble Models.**

The study evaluates whether meteorological predictors provide additional value beyond historical pollutant information for next-day daily Air Quality Index (AQI) forecasting in Dhaka, Bangladesh, using daily data from 2023 to 2025.

## Research Objectives

- Evaluate the incremental value of meteorological predictors.
- Compare pollutant-only and pollutant-plus-meteorological feature sets.
- Assess forecasting performance using chronological evaluation.
- Examine model robustness and seasonal variation.

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

## Data Source

The dataset was obtained from:

Karim, R. (2026). *Bangladesh 64 Districts Daily Climate and Air Quality (AQI) Dataset (2023–2025)*, Version 1. Mendeley Data. https://doi.org/10.17632/rd5cdx9shp.1

The original dataset contains daily climate and air quality observations for 64 districts in Bangladesh. This study uses the Dhaka district CSV file provided in the `data/` directory.

The dataset is distributed under the Creative Commons Attribution 4.0 International (CC BY 4.0) license.

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

- `Revision_Analysis_AQI_Dhaka.ipynb`: Research notebook containing the original analysis and subsequent revisions, model development, evaluation, robustness checks, and figure generation.
- `data/Dhaka_Climate_AQI_Data.csv`: Dhaka district dataset used in the analysis.
- `requirements.txt`: Python package dependencies and versions.
- `README.md`: Project documentation.

## Software Environment

The revised analysis was run using:

- Python 3.13.18
- pandas 2.2.3
- NumPy 2.4.6
- scikit-learn 1.6.1
- XGBoost 3.4.1
- LightGBM 4.6.0
- Matplotlib 3.10.0
- SciPy 1.16.3

## How to Run

1. Open `Dhaka_AQI_Forecasting_Revised.ipynb` using Google Colab.
2. Ensure the notebook has access to the internet.
3. Install the required dependencies using:

   `pip install -r requirements.txt`

4. Run the notebook cells sequentially.

The notebook retrieves the dataset directly from this GitHub repository, so manual dataset uploading is not required.

## Reproducibility

The repository provides the dataset, research notebook, and package dependency versions required to reproduce the analysis.

The notebook includes data preprocessing, feature engineering, model development, hyperparameter tuning, statistical evaluation, robustness checks, and figure generation.

The dataset is also available from its original Mendeley Data source.

## Code Availability

The research code and dataset used in this study are publicly available at:

https://github.com/putriikrima2/Dhaka-AQI-Forecasting
