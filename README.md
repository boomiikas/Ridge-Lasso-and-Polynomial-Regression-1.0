# 🔍 Ridge, Lasso & Polynomial Regression

This repository showcases different **regression experiments** that highlight how **regularization** and **polynomial features** influence model performance.  
The focus is on:
- Improving prediction accuracy  
- Handling high-dimensional or correlated data  
- Understanding feature selection behavior  

---

## 📌 What’s Inside?
We experiment with **four regression setups**:

### 🔹 Ridge Regression
- **Dataset:** `ridge_10feat_150.csv`  
- Method: `RidgeCV` (with built-in cross-validation)  
- **Findings:**  
  - Selects the optimal α (regularization strength)  
  - Produces stable coefficients by shrinking large weights  
  - Outputs: coefficients, intercept, R² score, RMSE  

---

### 🔹 Lasso Regression on Sparse Data
- **Dataset:** `lasso_sparse_150.csv`  
- Method: `LassoCV` (5-fold CV)  
- **Highlights:**  
  - Identifies the best α  
  - Performs **automatic feature selection** (some coefficients shrink to zero)  
  - Reports R² and RMSE  

---

### 🔹 Lasso Regression on Correlated Features
- **Dataset:** `lasso_groups_150.csv`  
- Aim: See how Lasso handles **correlated pairs** (xA/xB, xC/xD).  
- **Key Takeaways:**  
  - Best α selected via cross-validation  
  - In correlated groups, Lasso usually keeps **one variable** and discards the other  
  - Outputs coefficients, intercept, R², RMSE  

---

### 🔹 Polynomial vs Linear Regression
- **Dataset:** `poly_quadratic_150.csv`  
- **Comparison:**  
  - Linear Regression (y ~ x)  
  - Polynomial Regression (y ~ x + x²)  
- **Results:**  
  - Polynomial model fits non-linear trends better  
  - Reports coefficients, intercept, R², RMSE  
  - Predicts y at x = 1.5 for quadratic model  

---

## 📊 Metrics Used
- **R² Score:** Higher = better fit  
- **RMSE:** Lower = better accuracy  

---

## 💡 Insights
- Ridge prevents **overfitting** by penalizing large coefficients.  
- Lasso is great for **feature selection**, especially with many variables.  
- With correlated inputs, Lasso tends to keep just one.  
- Polynomial regression captures **curvature** that linear models miss.  

---

## ⚙️ Tech Stack
- **Language:** Python 3  
- **Libraries:**  
  - `numpy`, `pandas` → data handling  
  - `scikit-learn` → regression models & cross-validation  
  - `matplotlib`, `seaborn` → visualizations

---
