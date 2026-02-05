# 🏠 House Price Prediction – Comparative Study of Regression Models

This project implements and evaluates multiple regression algorithms to predict house prices using a unified preprocessing pipeline. The notebook is structured as a **narrative-driven machine learning workflow** that demonstrates model development, evaluation, and selection using quantitative performance metrics.

The goal is to compare linear, tree-based, and ensemble regressors and select the model that delivers the strongest generalization performance.

---

## 📌 Models Implemented

The following regression models are trained and evaluated under identical preprocessing and data splits:

* **Simple Linear Regression (SLR)** – Single-feature baseline
* **Multiple Linear Regression (MLR)** – Multivariate linear baseline
* **Decision Tree Regressor** – Non-linear single-model learner
* **Random Forest Regressor** – Ensemble model for variance reduction

---

## 📊 Evaluation Metrics

All models are evaluated using:

* **R² Score** – Measures explained variance
* **Root Mean Squared Error (RMSE)** – Measures prediction error

### Final Results

| Model                      | R² Score | RMSE     |
| -------------------------- | -------- | -------- |
| Simple Linear Regression   | 0.35     | 0.31     |
| Multiple Linear Regression | 0.77     | 0.18     |
| Decision Tree Regressor    | 0.55     | 0.26     |
| Random Forest Regressor    | **0.82** | **0.16** |

**Key Gains:**

* Gained a **~134% relative increase in explained variance** from baseline (SLR → Random Forest).
* Gained a **~48% reduction in RMSE** from baseline to final model.
* Gained improved generalization by transitioning from single-model learners to ensemble methods.

---
## 🗂️ Project Structure

```
.
├── Predict_house_prices.ipynb     # Main notebook with full ML workflow
├── regression_data_using_scikit_learn.ipynb (optional reference)
└── README.md
```

---

## ▶️ How to Run

1. Open the notebook in **Google Colab** or Jupyter Notebook
2. Run all cells sequentially
3. Review:

   * Data preprocessing
   * Model training
   * Metric comparison
   * Final model selection

---

## 🏁 Final Model Selection

The **Random Forest Regressor** is selected as the final model due to:

* Highest explained variance (**R² = 0.82**)
* Lowest prediction error (**RMSE = 0.16**)
* Strong bias–variance tradeoff compared to linear and single-tree models

---

## 🚀 Skills Demonstrated

* End-to-end regression pipeline design
* Feature preprocessing & scaling
* Model benchmarking under identical conditions
* Bias–variance tradeoff analysis
* Quantitative performance reporting
* Recruiter-friendly ML documentation

---
