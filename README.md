# 🏠 House Price Prediction

## 📌 Overview
An end-to-end machine learning project that predicts California house prices 
using the classic California Housing dataset. The project covers data 
preprocessing, feature engineering, model training, hyperparameter tuning, 
and evaluation.

---

## 📊 Dataset
- **Source:** California Housing Dataset
- **Rows:** 20,640
- **Features:** 10 (longitude, latitude, housing age, rooms, bedrooms, 
  population, households, income, ocean proximity)
- **Target:** Median House Value

---

## 🛠 Tech Stack
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn (Pipeline, ColumnTransformer, RandomizedSearchCV)

---

## 🔄 Project Workflow

1. **EDA** — Heatmap, histograms, geo scatter plot
2. **Data Cleaning** — Filled missing values in `total_bedrooms` with median
3. **Feature Engineering** — Created 3 new features:
   - `room_per_house`
   - `bedroom_per_house`
   - `population_per_house`
4. **Preprocessing** — OneHotEncoding for `ocean_proximity`, StandardScaler for numeric features
5. **Model Training** — 3 models trained using sklearn Pipelines:
   - Linear Regression
   - Decision Tree Regressor
   - Random Forest Regressor
6. **Hyperparameter Tuning** — RandomizedSearchCV (20 iterations, 5-fold CV)
7. **Evaluation** — R2 Score, RMSE, Actual vs Predicted plot

---

## 📈 Model Results

| Model | Train R2 | Test R2 | RMSE |
|---|---|---|---|
| Linear Regression | 0.658 | 0.597 | 72668.54 |
| Decision Tree | 1.000 | 0.589 | 73362.52 |
| Random Forest (Tuned) | 0.975 | 0.812 | 49669.29 |

---

## 🔍 Key Findings
- `median_income` is the most important feature by far
- Engineered features (`bedroom_per_house`, `population_per_house`) 
  ranked higher than raw features like `total_rooms` and `population`
- Random Forest significantly outperformed Linear Regression
