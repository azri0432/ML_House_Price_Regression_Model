# ML_House_Price_Regression_Model

## 📘 Overview
This project predicts home sale prices using various **machine learning regression algorithms**.  
It is derived from the [Housing Prices Competition for Kaggle Learn Users](https://www.kaggle.com/competitions/home-data-for-ml-course/overview) competition but restructured for educational use and portfolio demonstration.  

The notebook walks through a complete ML workflow, from data preprocessing and feature engineering to model comparison and hyperparameter tuning to showcase the development of a predictive regression model for real estate valuation.

---

## 🎯 Objectives
- Develop and evaluate multiple regression models to predict house prices.  
- Apply **feature engineering**, **data transformation**, and **cross-validation** to improve model accuracy.  
- Select and tune the best-performing algorithm (Gradient Boosting) based on RMSE performance.  
- Document the ML workflow in a reproducible and portfolio-ready format.

---

## 🧩 Project Workflow
1. **Exploratory Data Analysis (EDA)**  
   - Investigated feature correlations with `SalePrice`  
   - Log-transformed skewed target variable to stabilize variance  
2. **Feature Engineering**  
   - Created domain-relevant features:  
     `TotalSF`, `TotalBath`, `HouseAge`, `RemodAge`, `TotalPorchSF`, `OverallGrade`, and `GarageCars_x_Quality`  
3. **Model Comparison**  
   - Evaluated **7 regression algorithms** via 5-fold cross-validation  
   - Scoring metric: **Root Mean Squared Error (RMSE)** on log-transformed target  
4. **Model Selection & Tuning**  
   - Gradient Boosting Regressor emerged as the best performer  
   - Fine-tuned parameters to minimize validation error  
5. **Model Evaluation**  
   - Analyzed residual plots and prediction errors  
   - Noted stronger performance on lower- and mid-tier houses

---

## 📊 Results Summary

| Model | Mean RMSE (log) | Remarks |
|--------|------------------|----------|
| Linear Regression | ~0.151 | Baseline |
| Ridge Regression | ~0.147 | Improved generalization |
| Lasso Regression | ~0.399 | High RMSE; aggressive feature selection may have removed important predictors |
| Random Forest | ~0.141 | Good but prone to overfitting |
| **Gradient Boosting** | **~0.134** | ✅ Best performing |
| Support Vector Machine | ~0.143 | Performs well with proper scaling; moderately sensitive to hyperparameters |
| K-Neighbors Regressor | ~0.170 | Weak generalization |

**Validation RMSE (real prices):** ≈ **$30,052.62**

✅ *Gradient Boosting Regressor selected as final model.*

---

## 💡 Insights & Future Work
- Include Optuna/GridSearchCV for automated hyperparameter tuning.
- Investigate stacking ensemble to combine tree-based and linear models.
- Experiment with feature selection and log-based error metrics.

---

## 🧠 Author

Developed by Mohd Azri bin Mohd Ridzuan Nyanged
🎓 TalentLabs – MyMahir CADA Programme
💼 Data Analyst & Machine Learning Enthusiast
📫 [LinkedIn](https://www.linkedin.com/in/mohdazri4221)
