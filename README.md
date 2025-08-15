# AQI-Prediction-Seasonal-Analysis-for-Delhi
This repository contains a Jupyter Notebook that analyzes and predicts the **Air Quality Index (AQI)** for **Delhi, India** from **2015 to 2024**. It includes data preprocessing, exploratory data analysis (EDA), and machine learning models to forecast AQI and understand seasonal pollution patterns.

---
## 📊 Project Overview
- **Dataset:**  
  Combined from [Kaggle's Air Quality Data in India](https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india/data) and CPCB's official air quality portal.  
  The raw dataset contains **3,683 rows** of daily pollutant measurements.
- **Key Features:**  
  - PM2.5, PM10, NO, NO₂, NOx, NH₃, CO, SO₂, O₃, Benzene, Toluene
  - AQI value and AQI category (Good, Satisfactory, Moderate, Poor, Very Poor, Severe)
---
## ⚙️ Workflow

1. **Data Preprocessing**
   - Handling missing values via **linear interpolation**
   - Removal of outliers using **IQR method**
   - Feature scaling where necessary

2. **Exploratory Data Analysis**
   - Seasonal variation plots (winter, summer, monsoon)
   - Correlation matrix of pollutants
   - Trend analysis over years

3. **Modeling via both 5-fold CV and train-test split(70-30)**
   - Baseline: Linear/Lasso/Ridge Regression
   - Advanced: AdaBoost with RandomizedSearchCV (best performer in 70-30 split) and CatBoost (best performer in 5-fold CV)
   - Evaluation Metrics: R², MSE, MAE, MAPE, RMSE

4. **Results**
   - Seasonal AQI peaks in winters
   - AdaBoost with RandomizedSearchCV (best performer in 70-30 split) and CatBoost (best performer in 5-fold CV)

--
## 📚 Data Sources & Acknowledgements
- **Kaggle:** Air Quality Data in India — by Rohan Rao  
  https://www.kaggle.com/datasets/rohanrao/air-quality-data-in-india/data
- **CPCB:** Central Pollution Control Board, Government of India  
  https://cpcb.nic.in/
