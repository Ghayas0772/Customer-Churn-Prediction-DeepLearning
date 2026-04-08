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

##  Dataset

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

##  Data Preprocessing

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

## Model Architecture (ANN)

- Input Layer: based on features  
- Hidden Layer 1: 6 neurons (ReLU)  
- Hidden Layer 2: 6 neurons (ReLU)  
- Output Layer: 1 neuron (Sigmoid)  

### Compilation:
- Optimizer: Adam  
- Loss Function: Binary Crossentropy  
- Metric: Accuracy  

---

##  Model Training

- Epochs: 100  
- Batch Size: 10  
- Validation Split: 33%  

---

##  Model Performance

###  Test Accuracy:
**86%**

###  Confusion Matrix:
[[1513 94]
[ 186 207]]



### Key Metrics:

| Metric        | Stayed (0) | Exited (1) |
|--------------|-----------|-----------|
| Precision    | 0.89      | 0.69      |
| Recall       | 0.94      | 0.53      |
| F1-score     | 0.92      | 0.60      |

---

##  Key Insights

- Model performs **very well on non-churn customers (Stayed)**
- Struggles with detecting churn customers (Exited)
- Recall for churn = **53%** → needs improvement

###  Business Insight:
Missing churn customers can impact retention strategies.

---

##  Improvements

- Handle class imbalance:
  - SMOTE (Oversampling)
  - Class weights

- Try advanced models:
  - Random Forest
  - XGBoost
  - Gradient Boosting

---

##  Model Saving

- ANN Model:
  - `ann_model.keras`

- Scaler:
  - `scaler.pkl`

---

## Model Loading

```
python
from tensorflow.keras.models import load_model
import pickle

model = load_model('ann_model.keras')

with open('scaler.pkl', 'rb') as f:
    scaler = pickle.load(f) ```


### Project Structure

Customer-Churn-Prediction/

- model/
- ann_model.keras
- scaler.pkl
- notebook/
- churn_model.ipynb
- data/
Churn_Modelling.csv
README.md

### Technologies Used
Python
Pandas & NumPy
Scikit-learn
TensorFlow / Keras
Matplotlib & Seaborn
### Conclusion
ANN achieved good accuracy (86%)
Model is biased toward majority class
Further tuning required for real-world deployment
### Note

This project was developed for academic purposes and enhanced with AI-assisted explanations.
