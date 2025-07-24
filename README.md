# 📊 Telco Customer Churn Prediction using Deep Learning

This project uses a deep learning model built with TensorFlow and Keras to predict customer churn for a telecommunications company. The dataset is provided by IBM and contains customer usage patterns and service details.

## 🚀 Objective

To build a binary classification model that predicts whether a customer will **churn (leave)** or **stay**, based on demographic and service-related features.

---

## 📁 Dataset

**Source:** [Telco Customer Churn - IBM Sample Data](https://www.ibm.com/communities/analytics/watson-analytics-blog/guide-to-sample-datasets/)

**Columns include:**
- CustomerID
- Gender, SeniorCitizen, Partner, Dependents
- Tenure, PhoneService, InternetService, etc.
- `Churn` (Target variable)
- clone:https://github.com/HasinTaj/RUBBER-PROPERTIES-PREDICTION.git

---

## 🧼 Data Preprocessing

- Converted `TotalCharges` to numeric and handled non-numeric values.
- Dropped `customerID` column.
- Encoded categorical variables using `pd.get_dummies()`.
- Standardized numerical features with `StandardScaler`.
- Label encoded the target variable `Churn`.

---

## 🧠 Model Architecture

Built using `TensorFlow` / `Keras`:
- Input layer: 30+ features
- Hidden Layers:
  - Dense(64), activation='relu'
  - Dense(32), activation='relu'
- Output Layer: Dense(1), activation='sigmoid'
- Optimizer: Adam
- Loss: Binary Crossentropy
- Metrics: Accuracy

---

## 🧪 Evaluation Metrics

- Accuracy Score
- Classification Report:
  - Precision
  - Recall
  - F1-Score

---

## 📉 Results

| Metric         | Value    |
|----------------|----------|
| Accuracy       | ~80%     |
| Precision (Yes)| ~0.68    |
| Recall (Yes)   | ~0.49    |
| F1-Score (Yes) | ~0.57    |

---

## 🛠 Technologies Used

- Python 🐍
- Pandas & NumPy
- Scikit-learn
- TensorFlow & Keras
- Matplotlib / Seaborn 

---

## ⚠️ Common Issues

- Make sure to handle `NaN` values in `TotalCharges` after type conversion.
- Don’t forget to drop `customerID`.
- Apply `get_dummies()` to all object-type columns before training.
- Ensure the labels are encoded before fitting the model.

---

## 📂 How to Run

1. Clone this repo:
   ```bash
   git clone https://github.com/HasinTaj/RUBBER-PROPERTIES-PREDICTION.git

   cd telco-churn-predictor
