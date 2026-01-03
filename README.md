Transaction Fraud Detection (F4)

Problem:

In digital payment systems, there are few cases of fraudulent transactions relative to normal transactions, resulting in an extremely imbalanced dataset.
Conventional models are not capable of identifying fraud cases correctly because they are biased towards non-fraud cases. The goal is to differentiate fraudulent transactions and generate few false alarms.

Data Link:
PaySim – Synthetic Financial Fraud Dataset  
http://www.kaggle.com/datasets/ealaxi/paysim1
->Simulated mobile money transactions
->Highly imbalanced dataset
->Target column: 'isFraud'

Design:

The system follows a machine learning pipeline:
1.Data loading and preprocessing
2.Feature engineering from transaction balances and amounts
3.Stratified train-test split
4.Imbalance handling using:
    -Class weighting
    -SMOTE
5.Model training using ML classifiers
6.Threshold tuning for fraud detection
7.Evaluation using precision and recall
8.Export fraud probability scores

Assumptions:

-> The PaySim dataset is a synthetic dataset, simulating real-world transaction data
-> "Patterns found in historical data may indicate fraud in the future as well."
-> A better fraud case recall is valued more than accuracy.
-> Model output is probabilistic and needs threshold parameter tuning

Outcome:

A trained fraud detection model
Evaluation using precision and recall metrics
fraud_score.csv containing fraud risk scores for transactions

Real-Time Use Case:

-> The trained model can be integrated into payment systems to:
-> Score transactions in real time
-> Flag high-risk transactions
-> Assist fraud prevention teams
