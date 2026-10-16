# 📉 Customer Churn Prediction Project

An end-to-end Machine Learning project designed to predict customer churn in the telecommunications industry. This project covers data preprocessing, handling class imbalance, training multiple classification models, extracting key churn drivers, and performing customer risk segmentation.

---

## 🚀 Project Overview
Customer churn is a critical metric for subscription-based businesses. Identifying customers who are likely to cancel their service allows companies to take proactive retention measures. 
- **Dataset:** Telco Customer Churn (Kaggle)
- **Goal:** Predict whether a customer will churn and identify the primary factors driving their decision.

---

## 🛠️ Tech Stack & Libraries
- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Machine Learning:** Scikit-Learn, XGBoost
- **Class Imbalance Handling:** Imbalanced-Learn (SMOTE)
- **Data Visualization:** Matplotlib, Seaborn

---

## 📊 Project Workflow
1. **Data Cleaning & Preprocessing:** 
   - Handled missing values in `TotalCharges` and encoded categorical variables using One-Hot Encoding.
   - Dropped irrelevant identifiers (`customerID`).
2. **Handling Class Imbalance:** 
   - Used **SMOTE** (Synthetic Minority Over-sampling Technique) on the training set to prevent model bias towards loyal customers.
3. **Model Training & Evaluation:** 
   - Trained and compared three classification algorithms:
     - Logistic Regression
     - Random Forest Classifier
     - XGBoost Classifier
   - Evaluated models using **Accuracy, Precision, Recall, F1-Score, and ROC-AUC Score**.
4. **Feature Importance Analysis:** 
   - Extracted top features driving churn using the XGBoost model.
5. **Customer Risk Segmentation:** 
   - Segmented customers into **High Risk, Medium Risk, and Low Risk** categories based on their predicted churn probabilities.

---

## 🔑 Key Insights & Top Churn Drivers
According to the feature importance analysis, the top factors driving customer churn are:
1. **Payment Method:** Customers using *Electronic check* show the highest propensity to churn.
2. **Internet Service Type:** Users with *Fiber optic* connections experience higher churn rates.
3. **Contract Type:** Short-term / Month-to-month contracts lead to quicker service cancellation compared to two-year contracts.
4. **Paperless Billing:** Strongly correlates with churn behavior.

---

## 💡 Business Recommendations (Retention Strategies)
- **Promote Auto-Pay:** Incentivize customers using electronic checks to switch to automated credit card or digital wallet payments with small discounts.
- **Improve Fiber Optic Experience:** Investigate pricing or technical bottlenecks in high-tier fiber optic plans to retain high-value users.
- **Long-term Contract Incentives:** Offer attractive renewal discounts or loyalty perks to convert month-to-month subscribers into 1-year or 2-year contracts.
- **Targeted Retention Campaigns:** Focus the customer success/retention team directly on the **High-Risk** customer segment with personalized offers.

---

## 📂 Repository Structure
```text
customer-churn-prediction/
│
├── churn.csv                # Dataset file
├── churn_prediction.ipynb   # Jupyter Notebook with full implementation
└── README.md                # Project documentation