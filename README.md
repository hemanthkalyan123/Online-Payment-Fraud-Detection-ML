# 💳 Online Payment Fraud Detection using Machine Learning

A Machine Learning project that detects **fraudulent online payment transactions** using classification algorithms. The project performs data analysis, preprocessing, visualization, model training, and evaluation to identify potentially fraudulent transactions.

---

## 📌 Project Overview

Online payments have become an important part of modern financial transactions. With the growth of digital payments, detecting fraudulent transactions has also become increasingly important.

This project uses Machine Learning techniques to analyze online payment transactions and predict whether a transaction is:

* **0 → Normal Transaction**
* **1 → Fraudulent Transaction**

---

## 🎯 Objectives

* Analyze online payment transaction data
* Perform Exploratory Data Analysis (EDA)
* Understand transaction patterns
* Analyze fraudulent and normal transactions
* Preprocess categorical and numerical features
* Train multiple Machine Learning models
* Compare model performance
* Evaluate the selected model using a confusion matrix

---

## 🗂️ Dataset

The dataset contains information about online financial transactions.

### Dataset Features

| Feature          | Description                           |
| ---------------- | ------------------------------------- |
| `step`           | Unit of time for the transaction      |
| `type`           | Type of transaction                   |
| `amount`         | Total transaction amount              |
| `nameOrig`       | Account initiating the transaction    |
| `oldbalanceOrg`  | Sender's balance before transaction   |
| `newbalanceOrg`  | Sender's balance after transaction    |
| `nameDest`       | Account receiving the transaction     |
| `oldbalanceDest` | Receiver's balance before transaction |
| `newbalanceDest` | Receiver's balance after transaction  |
| `isFraud`        | Target variable: 0 or 1               |

---

## 📊 Dataset Information

| Category                           |     Count |
| ---------------------------------- | --------: |
| Total Transactions                 | 6,362,620 |
| Normal Transactions                | 6,354,407 |
| Fraudulent Transactions            |     8,213 |
| Input Features After Preprocessing |        10 |
| Target Variable                    | `isFraud` |

The dataset contains a large number of normal transactions compared with fraudulent transactions, making fraud detection an imbalanced classification problem.

---

## 🛠️ Technologies Used

* **Python**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **XGBoost**
* **Jupyter Notebook**

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Data Exploration
   ↓
Data Visualization
   ↓
Fraud Distribution Analysis
   ↓
Correlation Analysis
   ↓
Data Preprocessing
   ↓
Feature Encoding
   ↓
Train-Test Split
   ↓
Model Training
   ↓
Model Comparison
   ↓
Model Evaluation
```

---

## 🔍 Exploratory Data Analysis

The project performs Exploratory Data Analysis to understand the transaction dataset.

The analysis includes:

* Dataset information
* Statistical summary
* Data type analysis
* Transaction type distribution
* Transaction amount analysis
* Fraud transaction distribution
* Step distribution
* Feature correlation analysis

### Transaction Analysis

The project analyzes different payment types, including:

* CASH_OUT
* TRANSFER
* PAYMENT
* DEBIT
* CASH_IN

The analysis helps identify transaction patterns and differences between normal and fraudulent transactions.

---

## 🔧 Data Preprocessing

The following preprocessing steps are performed:

### Categorical Feature Encoding

The `type` column is converted into numerical features using one-hot encoding.

### Irrelevant Feature Removal

The following account-identification columns are removed before model training:

* `nameOrig`
* `nameDest`

The original `type` column is also removed after encoding.

### Feature and Target Separation

* **Features:** Transaction-related attributes used for prediction
* **Target:** `isFraud`

### Train-Test Split

The dataset is divided into:

* **70% Training Data**
* **30% Testing Data**

A fixed random state is used to maintain reproducibility.

---

## 🤖 Machine Learning Models

Three classification algorithms are used in this project:

### Logistic Regression

A classification algorithm used to estimate the probability of a transaction belonging to a particular class.

### XGBoost Classifier

A gradient boosting algorithm based on decision trees. It builds models sequentially and combines them to improve prediction performance.

### Random Forest Classifier

An ensemble learning algorithm that combines multiple decision trees and uses their combined predictions for classification.

---

## 📈 Model Performance

The models are evaluated using **ROC-AUC**.

| Model               | Training ROC-AUC | Validation ROC-AUC |
| ------------------- | ---------------: | -----------------: |
| Logistic Regression |           0.8874 |             0.8850 |
| XGBoost Classifier  |          0.99998 |            0.99921 |
| Random Forest       |           1.0000 |             0.9650 |

The reported results are based on the project implementation and may vary depending on the dataset, environment, library versions, and model configuration.

---

## 📊 Model Evaluation

Based on the reported validation ROC-AUC results, **XGBoost Classifier** is selected for further evaluation.

A **confusion matrix** is used to analyze the classification results.

The confusion matrix represents:

* **True Positive:** Fraud correctly identified as fraud
* **True Negative:** Normal transaction correctly identified as normal
* **False Positive:** Normal transaction incorrectly identified as fraud
* **False Negative:** Fraud incorrectly identified as normal

---

## ⚠️ Class Imbalance

Fraudulent transactions represent a small portion of the complete dataset.

This makes fraud detection a challenging classification problem.

Therefore, evaluating the model using only accuracy may not provide a complete picture of its performance.

Important evaluation metrics for this type of problem include:

* Precision
* Recall
* F1-Score
* ROC-AUC
* PR-AUC
* Confusion Matrix

---

## 🚀 How to Run

### 1. Clone the Repository

```text
git clone https://github.com/yourusername/online-payment-fraud-detection.git
```

### 2. Install Required Libraries

Install the required Python libraries used in the project.

### 3. Open the Jupyter Notebook

Launch Jupyter Notebook and open the project notebook.

### 4. Run the Notebook

Execute the notebook cells sequentially to perform:

**Data Analysis → Preprocessing → Model Training → Evaluation**

---

## 💼 Real-World Applications

This project can be used as a foundation for:

* Online payment fraud detection
* Banking transaction monitoring
* Digital wallet security
* Payment gateway monitoring
* E-commerce fraud detection
* Financial transaction analysis

---

## 🎓 Key Concepts

* Python
* Data Analysis
* Exploratory Data Analysis
* Data Visualization
* Feature Engineering
* One-Hot Encoding
* Binary Classification
* Logistic Regression
* XGBoost
* Random Forest
* ROC-AUC
* Confusion Matrix
* Class Imbalance
* Machine Learning

---

## 👨‍💻 Author

**Kalyan**

B.Tech | Electrical & Electronics Engineering

**Interests:** Machine Learning • Python • Data Science • Artificial Intelligence

---

⭐ **If you found this project useful, consider giving the repository a star!**
