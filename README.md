<div align="center">
  <img src="assets/logo00.png" alt="AI Jobs Market Analysis" width="55%"/>
</div>

---

📊 SaaS Customer Churn Analysis & Retention Strategy

### Behavioral Churn Prediction · Customer Segmentation · CLV & Retention Targeting

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-red.svg)](https://scikit-learn.org)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi)]()

---

## 📌 Project Overview

An end-to-end SaaS churn analytics project: it integrates five relational tables, engineers behavioral features, predicts churn risk, estimates customer lifetime value, and turns the results into a retention-targeting strategy and an interactive Power BI dashboard.

The focus is the **full analytical cycle** — from messy multi-table data to a business-ready retention framework — rather than a single high-accuracy model.

---

## 🎯 Business Objective

Subscription businesses lose recurring revenue through preventable churn. The project answers:

- Which behavioral and operational factors are associated with churn?
- Can we score each account's churn risk?
- Which high-value accounts deserve proactive retention?
- How should a limited retention budget be prioritized for the best return?

---

## 🗂 Dataset

Five relational SaaS tables (synthetic, 500 accounts), merged to account level:

| Table | Description |
|-------|-------------|
| `accounts.csv` | Customer profile, seats, plan tier, churn flag |
| `subscriptions.csv` | Subscription lifecycle and billing |
| `feature_usage.csv` | Product engagement and activity |
| `support_tickets.csv` | Support burden, satisfaction, escalations |
| `churn_events.csv` | Churn timing and cancellation reasons |

> Note: synthetic dataset. The data is well-suited for demonstrating the full pipeline; as is common with synthetic data, the predictive signal is limited — discussed honestly in the results below.

---

## 💾 Workflow

| Notebook | Focus |
|----------|-------|
| `01_EDA_and_Data_Cleaning` | Multi-table merge, feature engineering, EDA |
| `02_Churn_Prediction_and_Strategy` | Logistic Regression baseline, risk segmentation |
| `03_Advanced_Models` | Random Forest, model comparison, churn probability, CLV, retention matrix |

### Notebook 1 — Data Preparation & EDA
- Merged five relational tables on `account_id`, resolving granularity (subscription → account level)
- Cleaned missing values; engineered behavioral features: `inactive`, `high_value`, `low_satisfaction`, `support_heavy`
- Explored churn patterns by inactivity, satisfaction, support load, and account value

### Notebook 2 — Prediction & Strategy
- Built a churn KPI framework and a behavioral `risk_segment`
- Logistic Regression as an interpretable baseline
- Strategic segmentation for retention action

### Notebook 3 — Advanced Models & CLV
- Random Forest, compared head-to-head with Logistic Regression on the same split
- Full metric comparison (accuracy, precision, recall, F1, ROC-AUC)
- Churn probability score per account
- Customer Lifetime Value (CLV) estimation and **revenue at risk** = churn probability × CLV
- 2×2 retention targeting matrix: Immediate Action / Monitor / Nurture / Standard

---

## 🤖 Model Results — an Honest Read

Two models were compared on the same 80/20 split:

| Metric | Logistic Regression | Random Forest |
|--------|--------------------:|--------------:|
| Accuracy | 0.67 | 0.63 |
| Precision | 0.67 | 0.68 |
| Recall | 1.00 | 0.85 |
| F1 | 0.80 | 0.76 |
| ROC-AUC | 0.51 | 0.42 |

**Honest interpretation:** the ROC-AUC values are close to 0.5, which means the models do **not** separate churners from non-churners much better than chance on this data. The high recall of the Logistic Regression is misleading — with a 70% churn base rate, predicting "churn" for almost everyone yields high recall but little real discrimination.

The most likely reason is the **synthetic nature of the dataset**: the engineered features don't carry a strong real signal for churn. This is itself a finding — it shows the importance of validating whether the data actually supports prediction, rather than trusting metrics at face value.

**What remains valuable** is the full pipeline: the five-table integration, the feature engineering, the CLV and revenue-at-risk framework, and the retention-targeting matrix — all of which would apply directly to a real dataset with genuine signal.

### Feature Importance (Random Forest)
| Feature | Importance |
|---------|-----------:|
| total_usage | 37.6% |
| seats | 28.4% |
| ticket_count | 15.2% |
| avg_satisfaction | 14.4% |
| total_escalations | 4.4% |

---

## 📊 Power BI Dashboard

Interactive dashboard across 3 pages: Churn Overview · Behavioral Risk Analysis · Retention Targeting

**Interactive Dashboard:** [![Power BI](https://img.shields.io/badge/Power%20BI-View%20Dashboard-yellow?logo=powerbi)](https://app.powerbi.com/view?r=eyJrIjoiMDg3NzA3NjUtNDMwMC00NjdlLWEwNWItOTNiNGQzNjZlYzA4IiwidCI6IjFmNTRhMThlLTg0MjUtNDdiYi1hMDk3LTczODg2ZTM1MTE4YSIsImMiOjh9&pageName=c7c98034ea1c684f28b1) ↗️ *Ctrl+click to open in a new tab*

---

## 🧠 Key Findings

- Behavioral features (usage, support burden) carry more weight than account size in the model
- Inactivity and low satisfaction are associated with higher churn in the EDA
- On this synthetic data the models show limited predictive power (AUC ≈ 0.5) — an honest result
- The CLV + churn-probability matrix provides an actionable retention framework regardless of model strength

---

## 🛠 Tech Stack

| Area | Tools |
|------|-------|
| **Data & Analysis** | Python, Pandas, NumPy, Matplotlib, Seaborn |
| **Machine Learning** | scikit-learn — Logistic Regression, Random Forest, predict_proba, feature importance |
| **Business Analytics** | CLV estimation, revenue-at-risk, 2×2 retention matrix |
| **BI & Reporting** | Power BI |
| **Workflow** | Jupyter Notebook, GitHub |

---

## 🚀 Future Improvements

- Validate the pipeline on a real dataset with genuine churn signal
- Add time-based cohort retention analysis
- Test gradient boosting once meaningful signal is present
- Integrate real billing data for accurate revenue-at-risk

---

## 👤 Author

**Gabriele De Carlo** — · Python · SQL · Power BI — Data Analyst Portfolio Project, 2025


