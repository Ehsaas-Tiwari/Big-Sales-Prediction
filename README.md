# **Big Sale Prediction using Random Forest Regressor**

## Project Overview

This project aims to predict the sales of products at various outlets of a retail store chain using machine learning techniques. We have used a **Random Forest Regressor (RFR)** model to forecast the `Item_Outlet_Sales` based on various product and outlet features. The model helps retailers in demand forecasting, inventory management, and strategic planning.

---

## Dataset Description

The dataset consists of historical sales data for various products across different outlet locations. The target variable is:

- `Item_Outlet_Sales` — sales of a particular product at a particular outlet.

### Features used:

| Feature | Description |
|---------|-------------|
| `Item_Identifier` | Unique ID for each product |
| `Item_Weight` | Weight of the product |
| `Item_Fat_Content` | Whether the product is low fat or regular |
| `Item_Visibility` | % of total display area allocated to this product in the store |
| `Item_Type` | Category to which the product belongs |
| `Item_MRP` | Maximum Retail Price of the product |
| `Outlet_Identifier` | Unique ID of the outlet |
| `Outlet_Establishment_Year` | Year when the outlet was established |
| `Outlet_Size` | Size of the outlet (Small, Medium, High) |
| `Outlet_Location_Type` | Tier of the city where the outlet is located |
| `Outlet_Type` | Type of outlet (Grocery Store, Supermarket Type1/2/3) |

---

## Problem Statement

Predict `Item_Outlet_Sales` for each product at a particular outlet using the provided features. This is a **regression problem**.

---

## Project Pipeline

1. **Data Loading & Exploration**
   - Loaded dataset using pandas
   - Checked for missing values and basic statistics

2. **Data Preprocessing**
   - Handled missing values
   - Encoded categorical variables using One-Hot Encoding
   - Normalized/Standardized numerical features

3. **Hyperparameter Tuning**
   - Performed hyperparameter tuning using RandomizedSearchCV
   - Got the best estimator

4. **Model Selection**
   - Trained a `RandomForestRegressor` using scikit-learn
   - Evaluated model on train/test set using R², MAE, MSE

5. **Results & Evaluation**
   - Compared actual vs predicted sales
   - Visualized feature importance
   - Final model performance metrics

---

## Model Performance

| Metric | Train Set | Test Set |
|--------|-----------|----------|
| R² Score | 0.69 | 0.53 |
| MAE | 653.99 | 804.71 |
| MSE | 998802.13| 1579228.60 |


---

## Key Insights

- Item MRP was the most influential feature in predicting sales.
- Outlet type and size significantly affect the sales.
- RFR performed well with minimal overfitting after tuning.

---
