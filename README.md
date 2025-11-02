# 🚗 Car Price Prediction using Machine Learning

## 📘 Project Overview
This project applies **machine learning regression techniques** to predict the **selling price of used cars** based on factors such as brand value, manufacturing year, kilometers driven, fuel type, transmission, and ownership history.  

The goal is to build a predictive model that helps estimate a fair resale price, assisting **buyers**, **dealers**, and **auto marketplaces** in data-driven decision-making.

---

## 🎯 Objectives
- Perform **data analysis and visualization** to understand factors affecting car prices.  
- Apply **data preprocessing and feature engineering** to prepare the dataset.  
- Train multiple regression models and evaluate their performance.  
- Identify the most accurate and reliable model for price prediction.  
- Extract key insights into which car attributes influence price the most.

---

## 📂 Dataset
**Dataset Name:** Car Details Dataset  
**Source:** [Kaggle - Car Price Prediction Dataset](https://www.kaggle.com/datasets) *(or similar)*  

### Features:
| Feature | Description |
|----------|-------------|
| `Car_Name` | Model name of the car |
| `Year` | Year of manufacture |
| `Selling_Price` | Price of the car (target variable, in lakhs ₹) |
| `Present_Price` | Current ex-showroom price (in lakhs ₹) |
| `Driven_kms` | Kilometers driven |
| `Fuel_Type` | Fuel category (Petrol, Diesel, CNG) |
| `Selling_type` | Whether sold by dealer or individual |
| `Transmission` | Manual or Automatic |
| `Owner` | Number of previous owners |

---

## 🧠 Methodology

### 1️⃣ Data Exploration
- Checked for missing values, duplicates, and data inconsistencies.  
- Visualized distributions of numerical and categorical variables.  
- Identified strong correlations between **Present_Price**, **Year**, and **Selling_Price**.  
- Discovered non-linear relationships between price and mileage.

### 2️⃣ Feature Engineering
- Created **Car_Age = 2025 - Year** to better capture depreciation.  
- Removed irrelevant columns (`Car_Name`, `Year`).  
- One-hot encoded categorical features (`Fuel_Type`, `Selling_type`, `Transmission`).  
- Split data into **80% training** and **20% testing**.

### 3️⃣ Model Training
Trained and compared three regression algorithms:
- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**

### 4️⃣ Model Evaluation
Models were evaluated using:
- **R² (Coefficient of Determination)**
- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**

---

## 📊 Results

| Model | R² | MAE | RMSE |
|--------|-----|------|------|
| **Linear Regression** | 0.849 | 1.216 | 1.866 |
| **Decision Tree** | 0.945 | 0.733 | 1.121 |
| **Random Forest** | **0.959** | **0.637** | **0.966** |

✅ **Best Model:** Random Forest Regressor  

The **Random Forest model** outperformed others with an **R² score of 0.96**, meaning it explains 96% of the variance in car prices, while maintaining low prediction error.

---

## 🌟 Feature Importance (from Random Forest)
| Rank | Feature | Importance |
|------|----------|------------|
| 1️⃣ | **Present_Price** | Strongest predictor of resale price |
| 2️⃣ | **Car_Age** | Older cars sell for less |
| 3️⃣ | **Fuel_Type_Diesel** | Diesel cars retain higher value |
| 4️⃣ | **Driven_kms** | More distance → lower resale value |

📈 **Interpretation:**  
Car value depends most on its **initial price**, **age**, and **fuel type**, followed by **usage (Driven_kms)**.

---

## 🛠️ Technologies Used
- **Python** 🐍  
- **Pandas**, **NumPy** — Data cleaning and manipulation  
- **Matplotlib**, **Seaborn** — Exploratory data visualization  
- **Scikit-learn** — Machine learning algorithms and evaluation  

---
