# Detection-of-a-Fraud.CSV-file

Project Overview

Financial fraud poses a significant risk to digital payment systems. This project focuses on building a machine learning–based fraud detection system that identifies fraudulent transactions from highly imbalanced financial data.

A Random Forest Classifier is trained using engineered transaction-level features, and performance is evaluated using metrics suitable for imbalanced datasets such as Precision, Recall, F1-score, and ROC-AUC.

Dataset Description

The dataset contains transaction-level records with the following characteristics:

Transaction type (e.g., transfer, payment)

Origin and destination balances

Transaction amount

Fraud labels (isFraud)

Highly imbalanced target variable (fraud cases are rare)

Feature Engineering

To improve fraud detection, domain-specific features were created:

Encoded transaction type using Label Encoding

Original balance change

oldbalanceOrg - newbalanceOrig


Destination balance change

newbalanceDest - oldbalanceDest


Irrelevant or identifier columns were removed:

nameOrig

nameDest

isFlaggedFraud

Model Used

Random Forest Classifier

Handles non-linear relationships

Robust to noise

Supports feature importance analysis

Class imbalance handled using class_weight='balanced'

Train–Test Strategy

80/20 split

Stratified sampling to preserve fraud ratio

Random seed fixed for reproducibility

Model Evaluation

Due to the imbalanced nature of the dataset, accuracy was avoided as a primary metric.

The model was evaluated using:

Precision

Recall

F1-score

ROC-AUC score

These metrics provide a more realistic view of fraud detection performance.

Feature Importance

Random Forest feature importance was used to identify the most influential predictors of fraudulent behavior.

Top contributing features typically included:

Transaction amount

Balance change patterns

Transaction type

This improves model interpretability and supports explainable AI practices.

Technologies Used

Python

Pandas

NumPy

Scikit-learn

Matplotlib

Jupyter Notebook

How to Run the Project

Clone the repository:

git clone <repository-url>


Install dependencies:

pip install -r requirements.txt


Run the notebook:

jupyter notebook


Execute cells in order to:

Preprocess data

Train the model

Evaluate performance

Analyze feature importance
