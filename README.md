# Telco Customer Churn Prediction

## 📚 Context
Customer churn prediction is a critical use case for businesses looking to retain their customers. The goal is to predict whether a customer will leave (churn) or stay, based on their demographic information, account details, and the services they have subscribed to. This project uses a dataset provided by IBM Sample Data Sets.

---

## 📋 Project Description
This project analyzes customer data to predict churn behavior and provides insights for customer retention programs. Machine learning models are used to predict churn with high accuracy, enabling businesses to take preventive actions.

---

## 📂 Dataset Overview
The dataset contains the following information:

### Columns:
- **Demographic Info:** `gender`, `Partner`, `Dependents`
- **Services Signed Up For:** `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`
- **Account Info:** `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges`
- **Target Variable:** `Churn` (Indicates whether a customer has churned)

Each row represents a customer, and the columns describe the customer’s attributes.

---

## 🎯 Project Goals
1. Predict customer churn using machine learning models.
2. Compare various models to determine the best-performing one.
3. Develop actionable insights to aid customer retention strategies.

---

## ⚙️ Models Used
The following machine learning models were trained and evaluated:

| Model                     | Accuracy | F1 Score | ROC AUC | Cross-Val Score |
|---------------------------|----------|----------|---------|-----------------|
| Hist Gradient Boosting    | 83.77%   | 83.76%   | 91.88%  | 91.25%          |
| Cat Boosting              | 84.35%   | 84.35%   | 92.58%  | 91.58%          |
| XG Boost Classifier       | 84.30%   | 84.30%   | 92.47%  | 91.88%          |
| Random Forest Classifier  | 83.67%   | 83.66%   | 91.12%  | 90.21%          |

The **Cat Boosting model** performed the best across all metrics.

We can also Focus on recall because the cost of losing a customer in telecom industry is high, that means missing a churning customer (False Negative) can result in lost revenue and customer lifetime value (CLV). Also A telecom company wants to identify all customers likely to churn so it can target them with retention offers. Even if some customers are wrongly flagged as churning (False Positives), they can still receive offers, which may strengthen loyalty. So, Prioritize recall to ensure no potential churners are missed.

---

## 🛠️ Tools and Libraries
- **Programming Language:** Python
- **Libraries Used:** 
  - Machine Learning: `scikit-learn`, `xgboost`, `catboost`
  - Visualization: `seaborn`, `matplotlib`
  - Data Manipulation: `pandas`, `numpy`

---

## 📊 Insights
- Customers with short-term contracts and higher monthly charges are more likely to churn.
- Providing online security and technical support services significantly reduces churn rates.
- Payment methods like automatic payments improve customer retention.

---

## 📝 Future Work
- Explore more complex ensemble methods for further accuracy improvements.
- Perform hyperparameter optimization for additional performance gains.
- Visualize feature importance and decision boundaries for better interpretability.

---

## 🚀 How to Run the Project
1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/telco-churn-prediction.git
