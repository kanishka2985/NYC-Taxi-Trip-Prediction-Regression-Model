# NYC Taxi Trip Duration Prediction Model🚖📊

## 📌 Project Overview

This project aims to predict the **trip duration of New York City taxi rides** using machine learning techniques. Accurate trip duration estimates can significantly improve user experience, fleet management, and route planning in urban transportation systems.

---

# 🔍 Problem Statement

In a city as fast-paced as NYC, knowing how long a taxi trip will take is crucial for both drivers and passengers. This project aims to build a predictive model that can accurately estimate trip duration using historical data.

---

## 📂 Dataset

- **Source**: [Kaggle - NYC Taxi Trip Duration](https://www.kaggle.com/c/nyc-taxi-trip-duration)
- **Size**: ~55 million rows (subset used for modeling)
- **Key Features**:
  - `pickup_datetime`
  - `dropoff_datetime`
  - `pickup_longitude` & `latitude`
  - `dropoff_longitude` & `latitude`
  - `passenger_count`
  - `store_and_fwd_flag`
  - `trip_duration` (target variable, in seconds)

---

## ⚙️ Technologies Used

- Python 🐍
- Pandas & NumPy
- Scikit-learn
- XGBoost
- Matplotlib & Seaborn
- Jupyter Notebook

---

## 🧪 Methodology

### 🔹 Data Preprocessing
- Converted datetime fields to extract features like **hour**, **weekday**, **month**, etc.
- Removed obvious outliers and invalid entries (e.g., zero-duration trips).
- Visualized and cleaned geographic coordinates.

### 🔹 Exploratory Data Analysis (EDA)
- Found patterns in trip duration by:
  - Day of the week
  - Time of day
  - Pickup vs. dropoff zones
- Identified strong correlation between pickup/dropoff time and trip duration.

### 🔹 Modeling Techniques
Applied and compared multiple regression models:
- Linear Regression
- Ridge Regression
- Lasso Regression (with feature selection)
- K-Nearest Neighbors
- XGBoost Regressor

Each model was evaluated using appropriate metrics such as **R² score** and **RMSE** to check performance.

---

## 🧠 Models Trained

| Model               | Description                         |
|--------------------|-------------------------------------|
| Linear Regression  | Baseline model                      |
| Ridge Regression   | L2 regularization                   |
| Lasso Regression   | L1 regularization + feature selection |
| K-Nearest Neighbors| Non-linear model                    |
| XGBoost Regressor  | Advanced boosting model             |

---

## 📈 Results

- **Best Performing Model**: Lasso and XGBoost (based on accuracy and generalization)
- **R² Score**: High (above 0.982 on training, above 0.928 on validation)
- **Key Insight**: Trip duration is heavily influenced by pickup time and location, as well as traffic patterns on different days.

---
## ▶️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/kanishka2985/nyc-taxi-trip-duration
   cd nyc-taxi-trip-duration
