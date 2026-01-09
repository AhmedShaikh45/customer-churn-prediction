# 📊 Customer Churn Prediction | End-to-End Machine Learning Project

## 📌 Project Overview
Customer churn prediction helps businesses identify customers who are likely to stop using their services.  
In this project, I built an **end-to-end churn prediction system** using machine learning, with a strong focus on **business impact rather than just accuracy**.

The final model prioritizes **recall for churn customers**, ensuring that most at-risk customers are identified for retention efforts.

---

## 🎯 Business Problem
- Predict whether a customer will churn
- Reduce the number of missed churners
- Provide interpretable insights for business teams

**Key Challenge:**  
The dataset is **imbalanced**, with fewer churn customers than non-churn customers, making accuracy a misleading metric.

---

## 🧠 Workflow & Methodology

### 1️⃣ Data Understanding
- Analyzed customer demographics, services, and billing behavior
- Identified class imbalance in the target variable (`Churn`)

### 2️⃣ Data Preprocessing
- Dropped non-informative identifier columns (e.g., `customerID`)
- Converted categorical variables using **one-hot encoding**
- Handled missing values using **median imputation**
- Scaled numeric features with **StandardScaler**
- Prevented data leakage by applying preprocessing after train-test split

### 3️⃣ Feature Engineering
- Encoded service-related features such as:
  - InternetService
  - OnlineSecurity
  - TechSupport
  - OnlineBackup
- Analyzed feature importance using Logistic Regression coefficients

### 4️⃣ Model Development
Models trained and compared:
- Logistic Regression (Baseline)
- Logistic Regression with `class_weight='balanced'`
- Random Forest Classifier
- Threshold-tuned Logistic Regression

### 5️⃣ Hyperparameter Tuning
- Used **GridSearchCV** with 5-fold cross-validation
- Optimized based on **ROC-AUC**
- Tuned regularization parameters (`C`, `L1/L2 penalty`)

---

## 🏆 Final Model Selection

### ✅ Final Model: **Balanced Logistic Regression (Threshold Tuned)**

**Why this model?**
- Achieved the **highest recall for churn customers**
- Interpretable and business-friendly
- Stable and easy to deploy
- Better aligned with real-world churn costs

---

## 📈 Final Model Performance

### Classification Report
