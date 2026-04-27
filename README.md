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

---

# 🎯 Business Objective
Subscription businesses often lose revenue through preventable churn.  
The goal of this project was to identify:

✔ Which customers are most likely to churn  
✔ Which operational factors drive churn  
✔ Which high-value accounts require proactive retention  
✔ How data can support strategic intervention

---

# ⚙️ Quick Setup
To run this project, simply create an environment and install the requirements. All dependencies, including **Jupyter**, are listed in the `requirements.txt` file.

1. **Create and activate your environment:**
   ```bash
   python -m venv venv
   # Windows:
   venv\Scripts\activate
   # Mac/Linux:
   source venv/bin/activate
2. **install everything necessary:**
    ```bash
    pip install -r requirements.txt
   
---

# 🗂 Dataset Structure
The project integrates multiple relational SaaS datasets:

### Core Tables:
- **accounts.csv** → Customer profile, seats, plan tier, churn flag  
- **subscriptions.csv** → Subscription lifecycle, billing, upgrades/downgrades  
- **feature_usage.csv** → Product engagement and behavioral activity  
- **support_tickets.csv** → Support burden, satisfaction, escalation  
- **churn_events.csv** → Churn timing, reactivation, cancellation reasons  

### Scale:
- Multi-table relational schema  
- Account-level aggregation  
- Behavioral + operational + retention features  

---

# 💾 Project Workflow

## 📓 Notebook 1 — Data Preparation & EDA
### Key Tasks:
- Merged multi-source SaaS datasets  
- Resolved schema granularity issues (subscription → account level)  
- Cleaned missing values and inconsistencies  
- Engineered business features:
  - `inactive`
  - `high_value`
  - `low_satisfaction`
  - `support_heavy`
- Conducted exploratory analysis:
  - Churn distribution
  - Usage vs churn
  - Satisfaction vs churn
  - Correlation heatmap

### Key Findings:
- Low product engagement strongly correlates with churn  
- Inactive customers churn significantly more  
- Support-heavy customers show elevated churn risk  
- Customer satisfaction outperforms account size as a churn indicator  

---

## 📓 Notebook 2 — Churn Prediction & Retention Strategy
### Key Tasks:
- Built churn KPI framework  
- Created `risk_segment` (High Risk / Low Risk)  
- Logistic Regression model for churn prediction  
- Feature importance analysis  
- Strategic segmentation for business action  

### Model Focus:
**Behavior > Static Profile**

Primary churn drivers:
- Inactivity  
- Satisfaction decline  
- Support escalation  
- Usage reduction  

---

# 📊 Power BI Dashboard (!WIP!)

## Dashboard Pages:
### 1️⃣ Executive Overview
- Churn Rate
- Avg Usage
- Avg Satisfaction
- Churn by Plan Tier
- Geographic distribution

### 2️⃣ Behavioral Risk Analysis
- Usage vs Satisfaction Scatter
- Support Load
- Escalation Impact
- High-Risk Segments

### 3️⃣ Retention Opportunities
- High-Value Accounts at Risk
- Segment Prioritization
- Account-level intervention targeting

---

# 🧠 Strategic Insights
## Core Business Conclusion:
**Behavioral decline is a stronger churn predictor than customer size alone.**

### Practical Implications:
- Prioritize inactive high-value accounts  
- Reduce churn through customer success intervention  
- Monitor support burden as an early warning signal  
- Use segmentation for retention campaigns  

---

# 🛠 Tech Stack
### Data Analysis:
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

### BI & Reporting:
- Power BI
- DAX
- Power Query

### Workflow:
- Jupyter Notebook
- GitHub

---

# 🚀 Future Improvements
- Random Forest / XGBoost churn prediction  
- Cohort retention analysis  
- Customer Lifetime Value (CLV) forecasting  
- Revenue-at-risk modeling  
- Automated retention scoring  

---

# 👤 Author
**Gabriele De Carlo**  
Junior Data Analyst | Python | SQL | Power BI | Predictive Analytics

---
