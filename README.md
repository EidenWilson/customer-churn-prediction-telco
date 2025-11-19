## 🌟 Business Interpretation & Recommendations

This project provides a predictive tool and actionable insights to reduce customer churn, focusing on high-risk segments for targeted intervention.

### 🎯 Business Goal
To build a highly predictive classification model (Random Forest) that flags customers likely to churn, improving resource allocation for retention campaigns.

### 💡 Key Findings (The 'Why' Customers Leave)
The analysis reveals the three dominant factors driving customer attrition:

1.  **Contract Type (Month-to-Month):** This feature is the single largest predictor of churn risk, emphasizing a lack of commitment.
2.  **Low Tenure:** Newer customers are significantly more likely to churn, indicating issues with early customer experience and onboarding.
3.  **Lack of Online Security:** Customers who declined or do not use the Online Security feature show a higher propensity to leave, suggesting security concerns may be a driver.

### 📊 Model Performance Summary (Random Forest)
Our final model achieved an **AUC-ROC Score of 0.8316** on the test set, demonstrating strong discriminatory power.

| Metric | Score | Business Impact |
| :--- | :--- | :--- |
| **Churn Recall (1)** | **68%** | The model correctly identifies **68%** of all customers who will actually leave, allowing the retention team to focus efforts where they matter most. |
| **Churn Precision (1)** | **55%** | When the model flags a customer as high-risk, it is correct 55% of the time, leading to efficient targeting. |

### ✅ Actionable Recommendations

Based on the model's insights, we recommend the following retention strategies:

1.  **Contract Conversion Campaign:** Prioritize offering subsidized 1-Year or 2-Year contracts to customers currently on the **Month-to-Month** plan.
2.  **Onboarding Experience:** Implement a **90-day retention campaign** focused on customers with **low tenure** (< 12 months), offering proactive technical support checks or introductory benefits.
3.  **Service Upsell & Education:** Target customers flagged with **OnlineSecurity\_No** with a free 3-month trial of the service, positioning it as a mandatory security update rather than an optional add-on.

### 🛠️ Technical Stack
* **Language:** Python
* **Core Libraries:** Pandas, NumPy, Scikit-learn
* **Modeling:** Logistic Regression, Random Forest Classifier
* **Balancing:** SMOTE (Synthetic Minority Over-sampling Technique)
* **Visualization:** Matplotlib, Seaborn
