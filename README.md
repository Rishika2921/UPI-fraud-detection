# UPI Fraud Detection Using Machine Learning

## Overview

This project focuses on detecting fraudulent UPI (Unified Payments Interface) transactions using Machine Learning techniques. The model is trained on the **PaySim financial transaction dataset** and aims to classify transactions as **Fraudulent** or **Legitimate**.

The project includes **data preprocessing, feature engineering, exploratory data analysis (EDA), model training, evaluation, and comparison of multiple machine learning algorithms**.

---

## Problem Statement

Digital payment systems are growing rapidly, and fraudulent transactions have become a major concern. The objective of this project is to build a machine learning model that can identify suspicious UPI transactions and help financial institutions reduce fraud-related losses.

---

## Dataset

* **Dataset:** PaySim Financial Transactions Dataset
* **Source:** Kaggle / PaySim Simulation Dataset
* **Target Variable:** `isFraud`

### Features Used

* Transaction type
* Transaction amount
* Account balances before and after transaction
* Time step of transaction
* Engineered features such as:

  * `hour`
  * `is_night`

---

## Project Workflow

### 1. Data Loading

* Loaded the transaction dataset using **Pandas**.

### 2. Data Cleaning

* Removed unnecessary columns.
* Checked for null values.
* Identified duplicate records.

### 3. Feature Engineering

Created additional features to improve model performance:

* **hour** = step % 24
* **is_night** = 1 if transaction occurs between 12 AM – 6 AM

### 4. Encoding

* Applied **One-Hot Encoding** to the `type` column.

### 5. Train-Test Split

* **75%** Training Data
* **25%** Testing Data

### 6. Feature Scaling

* Used **StandardScaler** for numerical feature normalization.

### 7. Model Training

Trained multiple machine learning models:

* Logistic Regression
* Decision Tree Classifier
* Random Forest Classifier

### 8. Evaluation Metrics

Models were evaluated using:

* Accuracy Score
* Confusion Matrix
* Classification Report

  * Precision
  * Recall
  * F1-Score

---

## Technologies Used

| Technology   | Purpose                   |
| ------------ | ------------------------- |
| Python       | Programming Language      |
| Pandas       | Data Manipulation         |
| NumPy        | Numerical Computing       |
| Matplotlib   | Data Visualization        |
| Seaborn      | Statistical Visualization |
| Scikit-learn | Machine Learning          |

---

## Installation

Clone the repository:

```bash
git clone https://github.com/https://github.com/Rishika2921/upi-fraud-detection.git
cd upi-fraud-detection
```

Install required libraries:

```bash
pip install -r requirements.txt
```

---

## Run the Project

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Run:

```bash
UPI Fraud Detection.ipynb
```

---

## Model Comparison

| Model               | Purpose                                     |
| ------------------- | ------------------------------------------- |
| Logistic Regression | Baseline linear model                       |
| Decision Tree       | Rule-based classification                   |
| Random Forest       | Ensemble model for improved fraud detection |

The **Random Forest Classifier** provided the best overall performance for detecting fraudulent transactions.

---

## Project Structure

```text
upi-fraud-detection/
│
├── UPI Fraud Detection.ipynb
├── README.md
├── requirements.txt
└── dataset/
    └── PS_20174392719_1491204439457_log.csv.zip
```

---

## Key Learnings

* Handling highly imbalanced fraud datasets
* Feature engineering for transaction data
* Applying multiple classification algorithms
* Evaluating models using precision, recall, and F1-score
* Understanding the importance of recall in fraud detection problems

---

## Future Improvements

* Apply **SMOTE** for imbalance handling
* Use **XGBoost / LightGBM**
* Deploy the model using **Flask or Streamlit**
* Create a real-time fraud detection dashboard

---

## Author

**Rishika Sangwan**

* Data Analytics & Machine Learning Enthusiast
* Skilled in Python, SQL, Power BI, and Machine Learning

If you found this project useful, please **⭐ star the repository** and connect with me on LinkedIn!
