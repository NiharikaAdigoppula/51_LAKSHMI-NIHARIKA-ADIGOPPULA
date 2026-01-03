# Transaction Fraud Detection (F4)

## Problem

In digital payment systems, fraudulent transactions occur far less frequently than normal transactions, resulting in a highly imbalanced dataset.  
Conventional machine learning models become biased toward non-fraud cases and fail to detect fraud effectively.

The goal of this project is to accurately identify fraudulent transactions while minimizing false alarms.

---

## Data Link

PaySim – Synthetic Financial Fraud Dataset  
https://www.kaggle.com/datasets/ealaxi/paysim1

- Simulated mobile money transactions  
- Highly imbalanced dataset  
- Target column: `isFraud`

---

## Design

The system follows a standard machine learning pipeline:

1. Data loading and preprocessing  
2. Feature engineering using transaction balances and amounts  
3. Stratified train-test split  
4. Imbalance handling using:
   - Class weighting  
   - SMOTE  
5. Model training using machine learning classifiers  
6. Threshold tuning for fraud detection  
7. Evaluation using precision and recall  
8. Exporting fraud probability scores  

---

## Assumptions

- The PaySim dataset simulates real-world financial transactions  
- Patterns in historical data may indicate future fraud  
- Recall for fraud cases is prioritized over overall accuracy  
- Model outputs probabilities and requires threshold tuning  

---

## Outcome

- A trained fraud detection model  
- Evaluation using precision and recall metrics  
- `fraud_score.csv` containing fraud risk scores  

---

## Real-Time Use Case

The trained model can be integrated into payment systems to:

- Score transactions in real time  
- Flag high-risk transactions  
- Assist fraud prevention teams
