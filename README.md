# fraud_detection_analysis-
This is a comprehensive machine learning project, detecting fraud
# Fraud Detection Analysis

A machine learning pipeline designed to identify fraudulent financial transactions using a highly imbalanced dataset. This project performs comprehensive Exploratory Data Analysis (EDA), engineering domain-specific features, and trains a balanced classification model to flag suspicious activity.

---

## 📌 Project Overview
Financial fraud costs organizations billions of dollars annually. This repository contains an end-to-end data science solution to detect fraudulent activities from synthetic financial transaction logs. 

The primary challenge of this project is addressing extreme class imbalance, as fraudulent transactions account for only **0.13%** of the dataset (~8,213 fraud cases out of 6.36 million rows).

## 📊 Dataset Detail
The analysis uses the **Fraud Detection Dataset** (`AIML Dataset.csv`). It contains 11 core features representing transaction logs:
*   `type`: CASH-IN, CASH-OUT, DEBIT, PAYMENT and TRANSFER.
*   `amount`: Amount of the transaction in local currency.
*   `oldbalanceOrg` / `newbalanceOrig`: Initial and new balances of the sender.
*   `oldbalanceDest` / `newbalanceDest`: Initial and new balances of the recipient.
*   `isFraud`: The target variable (1 for fraudulent, 0 for legitimate).

## 🚀 Key Insights & Features
*   **Fraud Distribution:** Fraudulent behavior is strictly confined to `TRANSFER` and `CASH_OUT` transaction types.
*   **Feature Engineering:** Derived localized balance differentials (`balanceDiffOrig` and `balanceDiffDest`) to better capture anomalous cash-draining behaviors.
*   **High Recall Strategy:** Because failing to catch fraud is incredibly costly, the model is tuned to prioritize **Recall** over standard accuracy.

---

## 🛠️ Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/YOUR_USERNAME/fraud-detection-analysis.git](https://github.com/YOUR_USERNAME/fraud-detection-analysis.git)
   cd fraud-detection-analysis
