# Customer Churn Prediction (ANN + Machine Learning)

Predict whether a bank customer will churn (leave the bank) using Deep Learning (ANN) and Machine Learning techniques.

---

##  Project Overview

This project uses the **Churn_Modelling dataset** to predict whether a customer will exit the bank.

- Binary Classification Problem:
  - 0 → Customer Stayed
  - 1 → Customer Exited (Churn)

The project includes:
- Data preprocessing & feature engineering
- Artificial Neural Network (ANN)
- Model evaluation (Confusion Matrix & Metrics)
- Model saving & loading

---

## 📊 Dataset

- File: `Churn_Modelling.csv`
- Total Records: 10,000 customers
- Features include:
  - Credit Score
  - Geography
  - Gender
  - Age
  - Balance
  - Number of Products
  - IsActiveMember
  - Estimated Salary
  - Target: `Exited`

---

## ⚙️ Data Preprocessing

✔ Removed unnecessary columns (RowNumber, CustomerId, Surname)  
✔ One-hot encoding:
- Geography → France, Germany, Spain  
- Gender → Male  

✔ Feature Scaling:
- StandardScaler applied  

✔ Train-Test Split:
- 80% Training
- 20% Testing  

---

## 🧠 Model Architecture (ANN)

- Input Layer: based on features  
- Hidden Layer 1: 6 neurons (ReLU)  
- Hidden Layer 2: 6 neurons (ReLU)  
- Output Layer: 1 neuron (Sigmoid)  

### Compilation:
- Optimizer: Adam  
- Loss Function: Binary Crossentropy  
- Metric: Accuracy  

---

## 🚀 Model Training

- Epochs: 100  
- Batch Size: 10  
- Validation Split: 33%  

---

## 📈 Model Performance

### ✅ Test Accuracy:
**86%**

### 📊 Confusion Matrix:
