# Retail Sales Prediction

A Python machine learning project analyzing retail sales patterns and predicting the number of units sold (`unit_sales`). The notebook combines exploratory data analysis, feature engineering, model comparison, and regression evaluation.

## Dataset Overview

- **Dataset:** `retail_sales_data.csv` — 633 records and 13 columns.
- **Target:** `unit_sales` (number of units sold).
- **Coverage:** 46 stores, 23 items, and four distinct dates from January to February 2013.
- **Attributes:** Store and item identifiers, location, product family, store type, cluster, perishability, and sales data.

Because the dataset covers only four distinct dates, this project is an exploratory regression analysis rather than a validated long-term forecasting system.

## Technologies Used

Python, Google Colab, pandas, NumPy, Matplotlib, Seaborn, SciPy, and scikit-learn.

## Methodology

1. **Exploratory analysis:** Examine sales distributions, store and product patterns, and potential outliers without removing outlier records.
2. **Data split:** Use earlier dates for training (419 records) and the final date for testing (214 records).
3. **Feature engineering:** Create calendar features and group-average sales features for items, stores, product families, and clusters.
4. **Preprocessing:** Encode relevant categorical variables and scale model features.
5. **Model training:** Compare Support Vector Regression (SVR), Decision Tree Regression, Linear Regression, and Random Forest.
6. **Evaluation:** Use RMSE, MAE, and R² alongside saved charts and model comparison results.

## Recorded Model Results

The original notebook's saved execution reports these held-out test results:

| Model | RMSE | MAE | R² |
|---|---:|---:|---:|
| Linear Regression | 8.061 | 3.122 | 0.297 |
| SVR (selected by cross-validation) | **6.108** | **2.494** | **0.596** |
| Decision Tree (comparison baseline) | 7.473 | 2.663 | 0.396 |
| Random Forest | 6.246 | 2.496 | 0.578 |

SVR has the lowest test RMSE in this recorded model-comparison step. These results are taken from saved notebook output, not an independently reproduced run.

**Limitations:** The dataset contains only four distinct dates. Group-average features use training labels and include each training row's own target; using them before cross-validation can introduce target leakage. These results should not be treated as evidence of production forecasting performance.

## How to Run

The original notebook uses Google Colab and a fixed Google Drive path. To keep the notebook code unchanged:

1. Open [Google Colab](https://colab.research.google.com/) and upload `retail_sales_prediction.ipynb`.
2. In Google Drive, create `MACHINE LEARNING/Data` under **My Drive**.
3. Upload a copy of `retail_sales_data.csv` to that Google Drive folder and **name the copy `K234131595.csv`**. The file in this GitHub repository keeps its descriptive name.
4. Open the notebook in Colab, mount Google Drive when prompted, and run cells in order.
5. Review the saved and regenerated plots and regression metrics in the notebook.

The notebook expects the dataset at:

```text
/content/drive/MyDrive/MACHINE LEARNING/Data/K234131595.csv
```

Running outside Google Colab requires changing the notebook's Drive-mount and input-path code; this repository intentionally preserves the original code.

## Notes

The notebook retains its original code and saved results. The PDF course report is not included in this repository. Before reusing the dataset elsewhere, confirm that its original source and sharing terms permit redistribution.
