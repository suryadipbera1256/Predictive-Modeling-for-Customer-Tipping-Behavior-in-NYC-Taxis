# 🚕 NYC Taxi Tipping Behavior Prediction  
A Machine Learning Project to Predict Customer Tipping Decisions Using NYC TLC Trip Data

---

## 📖 Project Overview  
This project analyzes the **New York City Taxi & Limousine Commission (TLC)** dataset to understand and predict **customer tipping behavior** using machine learning.

Using more than **50,000+ taxi trip records**, the project identifies key factors influencing tips and builds high-performing classification models to assist taxi businesses with decision-making and pricing strategies.

---

## 🎯 Objectives
- Predict whether a customer will tip or not  
- Perform exploratory data analysis (EDA) to understand tipping trends  
- Build ML models such as Logistic Regression, Random Forest, and XGBoost  
- Improve accuracy using feature engineering  
- Evaluate models using F1-score, accuracy, recall, precision, AUC  
- Analyze overfitting using train–test metrics and learning curves  

---

## 📊 Model Performance (WITH METRICS)

### **Baseline Models**
| Model | Accuracy | Precision | Recall | F1-score | AUC |
|--------|----------|------------|---------|-----------|-------|
| Logistic Regression | 85% | 0.83 | 0.81 | 0.82 | 0.87 |
| Random Forest | 89% | 0.88 | 0.87 | 0.88 | 0.91 |

---

### **Final Model – XGBoost (Best Model)**
✔ **Accuracy:** 92%  
✔ **Precision:** 0.92  
✔ **Recall:** 0.90  
✔ **F1-score:** 0.91  
✔ **AUC:** 0.95  

XGBoost gave the best balance between predictive power and generalization.

---

## 🔎 Overfitting Analysis  
To ensure the model generalizes well:

### **Training vs Testing Metrics**
- Training Accuracy: **93.8%**  
- Testing Accuracy: **92.1%**  
- Training F1-score: **0.93**  
- Testing F1-score: **0.91**

✔ Overfitting kept under control (Gap < 3%)  
✔ Achieved by:
- Using L2 regularization  
- Limiting tree depth  
- Applying early stopping  
- Feature noise reduction  
- Stratified train–test split  

---

## 🧠 Feature Engineering (Improved Accuracy by +14%)
Key engineered features:
- Trip duration  
- Average speed  
- Tip percentage  
- Fare-to-distance ratio  
- Time-of-day categories  
- Payment type one-hot encoding  
- Vendor ID & passenger count signals  

---

## 🗂 Dataset  
- **Source:** NYC Taxi & Limousine Commission (NYC TLC)  
- Records: **50,000+**  
- Target Variable: `TipGiven` (1 if tip given, 0 otherwise)

Important fields used:
- trip_distance  
- fare_amount  
- tip_amount  
- passenger_count  
- trip_datetime  
- payment_type  

---

## 🧪 Exploratory Data Analysis (Highlights)
- Credit card payments have **3× higher tipping probability**  
- Evening trips show maximum tip percentages  
- Short trips (<2 miles) have the lowest tips  
- Strong correlation between **fare amount** and **tip decision**  

---

## 🔧 Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-Learn  
- XGBoost  
- Matplotlib, Seaborn  
- Jupyter Notebook  

---

## 🚀 How to Run the Project

### **1. Clone repository**
```bash
git clone https://github.com/suryadipbera1256/NYC-Taxi-Tip-Prediction.git
cd NYC-Taxi-Tip-Prediction
