# 📈 Economic Index Price Prediction

## Overview

This project predicts **Index Price** using economic indicators such as **Interest Rate** and **Unemployment Rate**. A linear regression model is built, evaluated, and validated using residual analysis to understand model performance and assumptions.

---

## Dataset

* Source: Economic Index CSV
* Target: `Index_Price`
* Features:

  * Interest Rate
  * Unemployment Rate
* Dropped columns: `year`, `month`, `Unnamed: 0`

---

## Tech Stack

* Python
* Pandas, NumPy
* Matplotlib, Seaborn
* Scikit-learn

---

📦 economic-index-price-prediction-multiple-linear-regression  
├── 📂 data  
│   └── economic_index.csv  
├── 📂 notebook  
│   └── economic_index_price_prediction.ipynb  
├── 📄 requirements.txt  
├── 📄 README.md  
└── 📄 .gitignore  

---

## Workflow

* Data cleaning (missing values check)
* Feature selection and column removal
* Exploratory Data Analysis (pairplot, correlation matrix)
* Regression visualization using `regplot`
* Train-test split
* Feature scaling using **StandardScaler**
* Linear Regression model training
* Prediction on test data
* Model evaluation (MAE, MSE, R²)

---

## Model Evaluation

* Performance metrics:

  * Mean Absolute Error (MAE)
  * Mean Squared Error (MSE)
  * R² Score

---

## Residual Analysis

* Residuals computed as:

  ```
  residuals = y_test - y_pred
  ```
* KDE plot used to analyze error distribution
* Scatter plot (`y_pred` vs residuals) used to check:

  * Bias
  * Linearity
  * Randomness of errors

---

## Key Findings

* Residuals are not centered around zero
* Model shows consistent under-prediction
* Residual patterns indicate non-linearity
* Linear regression underfits the data

---

## Conclusion

The model captures general trends but violates key linear regression assumptions due to biased and patterned residuals. This suggests the need for improved feature engineering or non-linear models to achieve better predictive performance.
