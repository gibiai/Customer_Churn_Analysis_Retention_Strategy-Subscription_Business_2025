<div align="center">
  <img src="assets/logo00.png" alt="AI Jobs Market Analysis" width="55%"/>
</div>

# 📊 SaaS Customer Churn Analysis & Retention Strategy (2025)

## 📌 Project Overview
An end-to-end SaaS churn analytics project designed to uncover behavioral churn drivers, segment customer risk, and support retention-focused business strategy.

This project simulates the work of a Junior Data Analyst operating across:
- Data Cleaning & Transformation
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Churn Prediction
- Customer Segmentation
- Power BI Dashboard Development

### Behavioral Churn Prediction · Customer Segmentation · CLV Estimation

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-red.svg)](https://scikit-learn.org)
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi)](https://app.powerbi.com/view?r=eyJrIjoiZWU3MTRiOTYtZjk2OS00NDAwLThmYTctNzgzNWY0MjI5Zjc0IiwidCI6IjFmNTRhMThlLTg0MjUtNDdiYi1hMDk3LTczODg2ZTM1MTE4YSIsImMiOjh9&pageName=c954228bb7088ab4c0e0)
[![Status](https://img.shields.io/badge/Status-Complete-success.svg)]()

---

## Description

End-to-end SaaS churn analytics project built to uncover behavioral churn drivers, segment customer risk, and support data-driven retention strategy. The pipeline merges 5 relational datasets, engineers business features, builds a Random Forest classifier, estimates Customer Lifetime Value, and exports a prioritized retention targeting matrix for Power BI. Key finding: customer satisfaction and product inactivity are stronger churn predictors than account size or plan tier.

---

## Project Structure

```
Customer_Churn_Analysis/
│
├── dataset/
│   ├── accounts.csv                    # customer profiles (500 accounts)
│   ├── subscriptions.csv               # subscription lifecycle (5,000 rows)
│   ├── feature_usage.csv               # product engagement logs (25,000 rows)
│   ├── support_tickets.csv             # support history (2,000 rows)
│   ├── churn_events.csv                # churn timing and reasons (600 rows)
│   ├── final_dataset.csv               # merged & cleaned (Notebook 1 output)
│   ├── final_dataset_segmented.csv     # with risk segments (Notebook 2 output)
│   └── final_dataset_advanced.csv      # with CLV & churn probability (Notebook 3 output)
│
├── notebooks/
│   ├── 01_EDA_and_Data_Cleaning.ipynb          # data prep, feature engineering, EDA
│   ├── 02_Churn_Prediction_and_Strategy.ipynb  # Logistic Regression, segmentation
│   └── 03_Advanced_Models.ipynb                # Random Forest, CLV, targeting matrix
│
├── assets/
├── requirements.txt
└── .gitignore
```

---

## Quick Setup

```bash
git clone https://github.com/gibiai/Customer_Churn_Analysis_Retention_Strategy-Subscription_Business_2025.git
cd Customer_Churn_Analysis_Retention_Strategy-Subscription_Business_2025
```

```bash
pip install -r requirements.txt
```

```bash
jupyter notebook
```

Run notebooks in order: `01` → `02` → `03`

---

## Dependencies

```
pandas>=2.0
numpy>=1.24
matplotlib>=3.7
seaborn>=0.12
scikit-learn>=1.3
jupyter>=1.0
```

---

## Dataset Structure

5 relational tables merged on `account_id`:

| Table | Rows | Description |
|-------|------|-------------|
| `accounts.csv` | 500 | Customer profiles, plan tier, seats, churn flag |
| `subscriptions.csv` | 5,000 | Subscription lifecycle, billing, upgrades |
| `feature_usage.csv` | 25,000 | Product engagement and activity logs |
| `support_tickets.csv` | 2,000 | Support burden, satisfaction, escalations |
| `churn_events.csv` | 600 | Churn timing, reasons, reactivation |

---

## Notebooks

| Notebook | Description | |
|----------|-------------|---|
| 01 — EDA & Data Cleaning | Multi-table merge, feature engineering, exploratory analysis | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1GmSHNLALewnE6MDaAGtfdJXQsNMelqoS#scrollTo=7cd949da) |
| 02 — Churn Prediction & Strategy | Logistic Regression, risk segmentation, KPI framework | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/15BXD4qItIidzYHXTXGKSj_1kO2XhIWv5) |
| 03 — Advanced Models & CLV | Random Forest, churn probability scores, CLV, retention targeting matrix | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1b-Uufo_CzdIVmY0rxd4-BWkPc9J3oEDF) |

---

## Key Findings

| Finding | Value |
|---------|-------|
| **Churn rate** | 70% — high, driven by behavioral decline |
| **Top churn driver** | `avg_satisfaction` — strongest predictor |
| **Second driver** | `total_usage` — low engagement = high risk |
| **High value at risk** | High-CLV accounts with churn probability > 0.7 |
| **Random Forest vs LR** | RF outperforms on all metrics, especially recall |
| **Key insight** | Behavioral signals outperform static account size |

---

## Techniques Used

| Area | Techniques |
|------|-----------|
| **Python** | Pandas, NumPy, multi-table merge, feature engineering |
| **Machine Learning** | Logistic Regression, Random Forest, predict_proba, feature importance |
| **Metrics** | Accuracy, Precision, Recall, F1, ROC-AUC, Confusion Matrix |
| **Business Analytics** | CLV estimation, retention targeting matrix, risk segmentation |
| **Visualization** | Matplotlib, Seaborn, scatter matrix, heatmap |

---

## 📊 Power BI Dashboard

Interactive dashboard across 3 pages: Churn Overview · Behavioral Risk Analysis · Retention Targeting

**Interactive Dashboard:** [![Power BI](https://img.shields.io/badge/Power%20BI-View%20Dashboard-yellow?logo=powerbi)](https://app.powerbi.com/view?r=eyJrIjoiZWU3MTRiOTYtZjk2OS00NDAwLThmYTctNzgzNWY0MjI5Zjc0IiwidCI6IjFmNTRhMThlLTg0MjUtNDdiYi1hMDk3LTczODg2ZTM1MTE4YSIsImMiOjh9&pageName=c954228bb7088ab4c0e0) ↗️ *Ctrl+click to open in a new tab*

---

## Future Improvements

- XGBoost / LightGBM for improved prediction accuracy
- Cohort retention analysis over time
- Automated churn alert system
- Revenue-at-risk modeling with real billing data

---

## Author

**Gabriele De Carlo** — Data Analyst Portfolio Project, 2025

