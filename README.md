# 🏡 Riyadh Real Estate Price Prediction

## 📌 Project Overview
This project aims to build a **machine learning model** to predict **real estate prices in Riyadh** based on property features such as type, location, area, number of rooms, and price per square meter.  
By analyzing these features, the model provides accurate price estimations that can be useful for real estate agents, investors, and buyers.

---

## ⚙️ Steps and Workflow

### 1. Data Preprocessing
- Dataset: `Riyadh_RealEstate.csv`
- Renamed columns for better readability (Arabic → English mapping).
- Converted categorical features (`City`, `District`, `Front`) into numerical format using **One-Hot Encoding**.
- Handled missing values:
  - Numerical columns → filled with **median**.
  - Categorical columns → filled with **mode**.
- Applied **StandardScaler** to normalize numerical features.
- Removed duplicate records.

---

### 2. Model Training (Full Dataset)
- Algorithm: **RandomForestRegressor**
- Split dataset into training and testing sets.
- Performance:
  - **Mean Squared Error (MSE)**: `0.0031`
  - **R² Score**: `0.926` → Explains ~92% of price variance.

---

### 3. Feature Importance and Selection
- Extracted the **Top 10 Features** influencing price:
  - `Price_per_Meter`
  - `Area`
  - Certain districts and cities (e.g., Riyadh, Mulham, etc.)
- Built a second model using only these top 10 features.
- Performance:
  - **MSE**: `0.0028`
  - **R² Score**: `0.933` → Higher accuracy with fewer features.
- Saved reduced dataset as `newRealEstate.csv`.

---

### 4. Price Analysis
- Descriptive statistics for `Total_Price`:
  - **Mean**: ~4.25M SAR
  - **Min**: 1.4K SAR
  - **Max**: 893M SAR (outliers exist)
- Calculated **Relative MSE** and **Percentage RMSE**, both extremely low → confirms model reliability.

---

## 🎯 Goal
The project demonstrates how **machine learning** can be applied to **real estate valuation** in Riyadh.  
It provides:
- Data preprocessing pipeline
- Feature importance insights
- A predictive model with strong performance  
This solution could be extended into a **real-world application** for property price estimation.

---

## 🚀 Technologies Used
- Python (Pandas, NumPy)
- Scikit-learn (RandomForest, Linear Regression, Preprocessing, Metrics)
- Matplotlib & Seaborn (Visualization)
- Google Colab (Development environment)

---
