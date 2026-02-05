# 🚗 Car Price Prediction

This project implements a **production-oriented machine learning pipeline** to predict car prices using structured tabular data. The workflow covers **data preprocessing, baseline modeling, ensemble modeling, tuning, and metric-driven model selection**, with final deployment recommendations based on empirical performance.

---

## 📌 Project Highlights

* Built a **leakage-safe preprocessing pipeline** using `ColumnTransformer`
* Compared **Multiple Linear Regression** vs. **Random Forest Regressor**
* Selected the final model using **R² and RMSE on held-out test data**
* Prioritized **interpretability, generalization, and operational simplicity**

---

## 🧠 Final Model Performance (Test Set)

| Model                      | R² Score | RMSE           |
| -------------------------- | -------- | -------------- |
| Multiple Linear Regression | **0.91** | **302,448.62** |
| Random Forest Regressor    | 0.88     | 343,558.43     |

### ✅ Final Recommendation

**Multiple Linear Regression** outperformed Random Forest on this dataset:

* Gained **+3 percentage points in R²** (0.91 vs. 0.88)
* Gained **~12% lower RMSE**, reducing prediction error
* Gained **higher interpretability** and **lower operational complexity**

---

## ⚙️ Technical Architecture

**Preprocessing**

* Dropped non-predictive identifiers
* `OneHotEncoder` for categorical features
* `StandardScaler` for numerical features
* Unified pipeline to prevent data leakage

**Models**

* Baseline: `LinearRegression()`
* Ensemble: `RandomForestRegressor(n_estimators=100, max_depth=10, random_state=1)`

**Evaluation**

* Metrics: R², RMSE
* Controlled comparison using identical train/test splits

---

## 📂 Repository Structure

```
.
├── Car_Price_Prediction.ipynb   # End-to-end ML workflow and results
├── README.md                   # Project overview and final metrics
```

## 🚀 How to Run

```bash
pip install -r requirements.txt
jupyter notebook Car_Price_Prediction.ipynb
```

Or open directly in JupyterLab:

```bash
jupyter lab
```

---

## 🔍 Key Engineering Decisions

* Used **pipelines** to guarantee reproducibility and leakage safety
* Benchmarked a **simple linear model** before introducing higher-capacity ensembles
* Selected the final model based on **generalization performance, not complexity**
* Ensured **deterministic results** with fixed random seeds

---
