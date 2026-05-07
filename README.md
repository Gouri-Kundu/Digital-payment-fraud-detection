# Digital Payment Fraud Detection

A Machine Learning project focused on detecting fraudulent digital payment transactions using classification models and threshold tuning techniques.

---

## Project Overview

With the rapid growth of online transactions, fraud detection has become a critical challenge in the financial industry.  
This project aims to build a fraud detection system capable of identifying fraudulent transactions while handling highly imbalanced data.

The project was built completely from scratch using separate train and test datasets downloaded from Kaggle.

---

## Problem Statement

Predict whether a transaction is fraudulent at the time of authorization.

Target column: `is_fraud`
  - `1` → Fraudulent Transaction
  - `0` → Legitimate Transaction
    
---

### Dataset Details

- ~400,000 transactions
- ~40,000 customers
- ~8,000 merchants
- Transaction records across 12 months (2023)
- Highly imbalanced fraud distribution
- Separate train and test datasets with time-based split

---

## Objective

The primary goal of this project is to:

- Detect fraudulent transactions accurately
- Minimize missed fraud cases (False Negatives)
- Handle class imbalance effectively
- Compare multiple machine learning models

---

## Dataset

- Source: [Kaggle Dataset](https://www.kaggle.com/datasets/rohit8527kmr7518/digital-payment-fraud-detection-benchmark)
- Dataset Type: Separate Train and Test datasets
- Problem Type: Binary Classification

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib

---

## Workflow

1. Data Loading
2. Exploratory Data Analysis (EDA)  
3. Data Cleaning & Preprocessing  
4. Feature Engineering  
5. Handling Class Imbalance  
6. Model Training  
7. Hyperparameter Tuning  
8. Threshold Tuning  
9. Model Evaluation on Validation & Test Data

---

## Models Used

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier

---

## Evaluation Metrics

Since fraud detection is an imbalanced classification problem, the focus was placed on:

- Recall
- ROC-AUC Score
- Confusion Matrix
- Classification Report

---

### Why Recall?

Fraud detection is a highly imbalanced classification problem where fraudulent transactions are very rare compared to genuine transactions.

In such cases, Recall becomes one of the most important evaluation metrics because missing a fraudulent transaction (False Negative) can lead to financial loss and security risks.

A higher Recall ensures that the model is able to identify and capture a larger number of fraud cases, even if it increases some false alarms (False Positives).

---

## Key Highlights

- Performed hyperparameter tuning using `RandomizedSearchCV` and `GridSearchCV`
- Applied threshold tuning to improve fraud detection performance
- Handled class imbalance using:
  - `class_weight='balanced'`
  - `scale_pos_weight`
- Compared multiple ML models to identify the best-performing approach

---

## Results

- Logistic Regression was used as a baseline model but showed lower fraud detection capability compared to ensemble models.

- XGBoost achieved very high Recall, meaning it was able to detect most fraudulent transactions successfully. However, increasing Recall also increased False Positives, causing many genuine transactions to be flagged as fraud.

- Random Forest provided a more balanced performance between Recall and Precision after threshold tuning. It was able to detect a large number of fraud cases while reducing unnecessary false alarms compared to XGBoost.

- Threshold tuning played an important role in improving fraud detection performance. Lowering the classification threshold increased Recall by helping the model capture more fraud cases.

- The project demonstrates the real-world tradeoff between Recall and Precision in fraud detection systems:
  - Higher Recall → Fewer frauds missed
  - Lower Precision → More genuine transactions flagged as fraud

- Final model evaluation was performed on unseen test data to check the model’s generalization capability.
  
---

## Conclusion

This project demonstrates an end-to-end machine learning workflow for fraud detection, including preprocessing, imbalance handling, model tuning, and evaluation on validation set and unseen test data.

It also highlights the importance of balancing Recall and Precision in real-world fraud detection systems.

---

## Contact

Feel free to connect for discussions, suggestions, or collaboration.

Email: gourikundu1808@gmail.com
LinkedIn: www.linkedin.com/in/gouri-kundu
