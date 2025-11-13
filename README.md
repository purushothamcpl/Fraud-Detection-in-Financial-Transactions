Fraud Detection in Financial Transactions
Overview
This project analyzes a large dataset of financial transactions and aims to detect fraudulent activities using various data science techniques and machine learning models.

Dataset
Source: Dataset.csv (loaded inside the notebook)

Rows: More than 6 million transaction records

Columns:

step, type, amount, nameOrig, oldbalanceOrg, newbalanceOrig, nameDest, oldbalanceDest, newbalanceDest, isFraud, isFlaggedFraud

Project Steps
Data Exploration and Visualization

Analyzes transaction types and balances

Visualizes fraud occurrence over time

Feature Engineering

Adds balance difference columns, encodes categorical variables

Model Building

Uses a pipeline with preprocessing:

Numerical: StandardScaler

Categorical: OneHotEncoder

Combines using ColumnTransformer

Classifier: Logistic Regression (class_weight=balanced, max_iter=1000)

Evaluation

Confusion matrix, classification report (Precision, Recall, F1 score)

Achieves test accuracy of around 94.55%

Model Save

Trained pipeline saved as frauddetectionpipeline.pkl for future use

How to Run
Install Dependencies:

Python 3.x

pandas, numpy, matplotlib, seaborn, scikit-learn, joblib

bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
Open project.ipynb in Jupyter Notebook:

Run all cells

Ensure Dataset.csv is in the same directory

Output:

Classification metrics displayed

Trained model file: frauddetectionpipeline.pkl

Results
Precision/Recall for Fraud Class:

Precision: 0.02

Recall: 0.93

Accuracy:

94.55%

Most frauds are detected in ‘TRANSFER’ and ‘CASHOUT’ transaction types.

Files
project.ipynb – Main Jupyter notebook

Dataset.csv – Transaction data

frauddetectionpipeline.pkl – Saved model
