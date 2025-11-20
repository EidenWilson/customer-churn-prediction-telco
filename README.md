# 🚀 Customer Churn Prediction & Retention Dashboard

## Executive Summary
This project delivers an end-to-end Applied Data Science solution focused on maximizing customer retention for a telecommunications company. By leveraging Machine Learning, the solution predicts customer attrition and translates these predictions into a high-utility, actionable business intelligence dashboard (Power BI).

---

## 🎯 Key Results & Business Insights

### 1. Overall Risk Profile
The baseline **Overall Churn Risk** for the customer population is **35.70%** (KPI Card). This establishes the scale of the retention problem.

### 2. Primary Churn Driver (Tenure)
The **Churn Risk vs. Customer Tenure** chart visually proves that the highest probability of churn (up to 70%+) occurs at the **lowest tenure scores** (left side of the chart), confirming that customer onboarding and first-year experience are critical failure points.

### 3. Actionable Deliverable (The Call List)
The **High-Risk Customer Call List** table is the core tool for the Retention Team.

* The table is filtered to show **only** customers predicted to churn.
* The **Heat Map** (gradient coloring on Churn Probability) immediately prioritizes the most urgent calls (rows in deep red).

---
## 📈 Final Dashboard Visualization

This visualization was created using Power BI to ensure maximum usability by non-technical stakeholders.

<p align="center">
  <img src=""C:\Users\EIDEN W\OneDrive\Pictures\Screenshots\Screenshot 2025-11-20 213035.png"" alt="Customer Retention Dashboard" width="100%">
</p>

---

## 🛠️ Technical Workflow

### Data Science Pipeline
1.  **Data Acquisition:** Loaded Telco Customer Churn dataset.
2.  **Preprocessing:** Handled missing values (`TotalCharges`), one-hot encoded all categorical features, and performed **Standard Scaling** on numerical features (`Tenure`, `MonthlyCharges`) to optimize model training.
3.  **Imbalance Handling:** Utilized **SMOTE** (Synthetic Minority Over-sampling Technique) on the training data to ensure the model was not biased toward the "Non-Churn" class.
4.  **Modeling:** Trained and evaluated **Random Forest** and Logistic Regression classifiers. Selected the model with the best combined **Recall** (to minimize missed opportunities) and **AUC-ROC** score.

### Business Intelligence Stack
* **Modeling & Export:** Python (Pandas, Scikit-learn, Imbalanced-learn)
* **Visualization:** Power BI Desktop

---

## 📝 Business Recommendations

Based on the quantitative analysis, the primary focus for the retention strategy should be:

1.  **Targeted Intervention:** Retention agents should exclusively use the **High-Risk Customer Call List**, prioritizing customers by the deepest red **Churn Probability** score.
2.  **Onboarding Focus:** Develop specialized interventions (e.g., proactive calls, loyalty incentives) for customers in the lowest **Tenure** quartile, as demonstrated by the steepest drop-off in the risk chart.

***
**Note:** The `Tenure` and `Monthly Charges` columns are displayed as standardized Z-scores, consistent with the model's training data.
