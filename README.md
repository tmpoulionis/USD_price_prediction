# 💵 USD Value Prediction Project

✨ **A machine learning project to forecast the US Dollar's value using historical data and ensemble methods.**

---

## 📌 Overview

A brokerage firm wanted to predict the US Dollar's value to aid financial decisions. This project uses **5 years of historical data** (fetched via `yfinance`) to build forecasting models. The focus was on experimenting with **linear regression, ensemble methods, and log returns** for interpretable predictions.

---

## 🚀 Approach
1. Exploratory Data Analysis (EDA)
    - Visualized the Dollar's price trends over 5 years using matplotlib and plotly.
    - Identified patterns and cleaned missing data.

2. Feature Engineering
    - Created a 5-day sliding window to use past values for forecasting.
    - Transformed raw prices into log returns for percentage-based predictions (easier interpretation).

3. Testing Multiple Models:
   - Linear Regression
   - Random Forest
   - Bagging/Stacking with Linear Regression
   - XGBoost 
   - Lasso Regression (for regularization)

## 📊 Results

### Absolute Price Predictions
| Model                      | Training MAE | Test MAE    |
|----------------------------|--------------|-------------|
| Linear Regression          | 0.3393       | 0.2719      |
| Random Forest           | 0.2694       | 0.2863      |
| XGBoost                 | 0.2775       | 0.3093      |
| Linear Regression + Bagging | 0.3403      | 0.2735      |
| Linear Regression + Stacking | 0.3380 | **0.2709**  |

### Log Returns Predictions (Interpretable % Changes)
| Model                      | Training MAE | Test MAE    |
|----------------------------|--------------|-------------|
| Linear Regression          | 0.00336      | 0.00272     |
| Random Forest           | 0.00281  | 0.00264     |
| XGBoost                 | 0.00341      | **0.00260** |
| Lasso Regression  + Bagging     | 0.00337  | 0.00271     |
| Linear Regression + Stacking | 0.00344 | 0.00262    |

## 🛠️ Technologies Used  
yfinance · NumPy · Pandas · Matplotlib · Plotly · Scikit-learn  
  
