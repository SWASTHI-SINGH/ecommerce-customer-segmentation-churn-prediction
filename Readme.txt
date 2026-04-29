# 🛒 E-Commerce Customer Segmentation & Churn Prediction

## 📌 Overview

This project analyzes e-commerce transaction data to:

* Segment customers based on behavior (RFM analysis)
* Predict customer churn using machine learning

---

## 🎯 Objectives

* Identify high-value customer segments
* Predict customers likely to churn
* Enable targeted retention strategies

---

## 📊 Dataset

* UCI Online Retail Dataset (~541K transactions)
* Features: CustomerID, InvoiceDate, Quantity, Price, Country

---

## ⚙️ Approach

### 🔹 Data Processing

* Removed missing CustomerID (~25%)
* Filtered cancellations & invalid transactions
* Created revenue feature

### 🔹 Feature Engineering

* RFM (Recency, Frequency, Monetary)
* Additional behavioral features
* Log transformation + scaling

---

## 👥 Segmentation

* Model: K-Means (k=4)
* Segments:

  * Champions
  * Loyal Customers
  * Occasional Buyers
  * At-Risk / Dormant

---

## 🔮 Churn Prediction

* Models: Logistic Regression, Random Forest, Gradient Boosting
* Final Model: **Gradient Boosting**
* Performance:

  * ROC-AUC: ~0.72
  * F1 Score: ~0.67

---

## 📦 Models Included

* `gb_churn_model.pkl` → Churn prediction
* `scaler_churn.pkl` → Preprocessing
* `rf_segment_classifier.pkl` → Segment prediction
* `label_encoder.pkl` → Segment decoding

---

## 🚀 Usage

```python
import joblib

model = joblib.load('Model/gb_churn_model.pkl')
scaler = joblib.load('Model/scaler_churn.pkl')
```

---

## 💡 Key Insights

* ~18% customers generate ~64% revenue
* Early churn detection enables revenue recovery
* Segmentation supports targeted marketing

---

## 🛠 Tools

Python · Scikit-learn · Pandas · Power BI

---

## 👤 Author

Swasthi Singh
