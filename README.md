# Retail Sales Prediction

## Project Overview

A machine learning project that explores retail sales patterns and predicts product sales quantities (`unit_sales`). The dataset contains **633 records across four dates in 2013**, making this an exploratory regression study rather than a long-term time-series forecasting system.

## Methodology & Implementation

- Analyzed sales distributions and differences across stores and product categories.
- Prepared numerical and categorical features, including calendar-based and group-level sales features.
- Compared **Linear Regression**, **Support Vector Regression (SVR)**, **Decision Tree**, and **Random Forest** models.
- Evaluated regression performance using RMSE, MAE, and R² on a held-out test set.

## Results & Key Findings

**SVR** achieved the lowest recorded test RMSE among the compared models:

- **RMSE:** 6.108
- **MAE:** 2.494
- **R²:** 0.596

These are results from the original notebook run. The limited date coverage and use of target-derived group features constrain how broadly the predictive performance can be interpreted.

## Technologies

Python, Google Colab, pandas, NumPy, SciPy, scikit-learn, Matplotlib, Seaborn.
