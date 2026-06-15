# 📊 Telecom Customer Churn Prediction

---

## 📌 Introduction

### What is Customer Churn?

Customer churn is defined as when customers or subscribers discontinue doing business with a firm or service.

In the telecom industry, customers can easily switch providers, leading to a high churn rate of **15–25% annually**. Since acquiring new customers is significantly more expensive than retaining existing ones, predicting churn is crucial for business growth.

By identifying customers who are likely to leave, companies can implement targeted retention strategies and improve overall profitability.

---

## 🎯 Objectives

- Finding the % of churn customers and active customers
- Analyzing features responsible for customer churn
- Building machine learning models for classification
- Selecting the best-performing model

---

## 📂 Dataset

**[Telco Customer Churn](https://www.kaggle.com/code/bhartiprasad17/customer-churn-prediction/data)**

### Includes:
- Customer churn status
- Services subscribed (Internet, Security, Streaming, etc.)
- Account details (tenure, contract, billing, charges)
- Demographics (gender, dependents, senior citizen)

---

## 🔍 Exploratory Data Analysis (EDA)

### Key Insights:

- **Churn Rate:** 26.6% customers left
- **Gender:** No major impact on churn
- **Contract Type:**
  - Month-to-Month → ~75% churn
  - One-Year → ~13% churn
  - Two-Year → ~3% churn
- **Payment Method:**
  - Electronic Check → High churn
  - Auto-payment → Lower churn
- **Internet Service:**
  - Fiber optic → High churn
  - DSL → Lower churn
- **Dependents:** Customers without dependents churn more
- **Online Security:** Lack of security increases churn
- **Senior Citizens:** Higher churn rate
- **Paperless Billing:** Higher churn
- **Tech Support:** Absence increases churn
- **Charges & Tenure:**
  - High monthly charges → High churn
  - New customers → High churn

---

## 🤖 Machine Learning Models

- Logistic Regression
- KNN
- Naive Bayes
- Decision Tree
- Random Forest
- AdaBoost
- Gradient Boosting
- Voting Classifier (Final Model)

---

## 🏆 Model Performance

| Model                  | Accuracy |
|-----------------------|---------|
| Logistic Regression   | 84.13%  |
| KNN                   | 79.13%  |
| Naive Bayes           | 82.32%  |
| Decision Tree         | 64.70%  |
| Random Forest         | 81.97%  |
| AdaBoost              | 84.45%  |
| Gradient Boosting     | 84.46%  |
| **Voting Classifier** | **84.68%** ✅ |

---

## ⚙️ Final Model: Voting Classifier

```python
from sklearn.ensemble import VotingClassifier

clf1 = GradientBoostingClassifier()
clf2 = LogisticRegression()
clf3 = AdaBoostClassifier()

eclf1 = VotingClassifier(
    estimators=[('gbc', clf1), ('lr', clf2), ('abc', clf3)],
    voting='soft'
)

eclf1.fit(X_train, y_train)
predictions = eclf1.predict(X_test)
```

---

## 📉 Confusion Matrix Insights

- Good prediction for non-churn customers
- Balanced churn classification
- Some misclassification exists → scope for improvement

---

## 🚀 Future Improvements

- Hyperparameter tuning
- Feature engineering
- Handling class imbalance
- Trying advanced models

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Jupyter Notebook

---

## 👨‍💻 About Me

Hi, I'm **J KARTHIK REDDY** 👋  
AI & Data Science enthusiast with strong expertise in Machine Learning, Data Analysis, and building real-world data-driven solutions.


