# Credit_Card_Approval_Prediction
Project Overview
This project focuses on developing a predictive model to determine whether a credit card application will be approved or rejected. Using demographic and financial data, the model classifies applications based on a target variable created from historical credit records. The application has been deployed using Flask with a simple HTML/CSS interface for predictions.

Problem Statement
Credit card approval is a crucial task for financial institutions, requiring accurate predictions based on an applicant's personal and financial data. This project aims to automate this process by building a machine learning model to predict approval outcomes.

Datasets
Two datasets were used in this project:

Application Record: Contains personal and financial data of applicants.
Credit Record: Contains historical credit status data.
These datasets were merged based on a common ID column, and a new TARGET variable was created using the STATUS column from the credit record dataset. The merged data was saved for further processing.

Data Preprocessing
Steps Included:
Handling Missing Values: Applied techniques to handle missing values across features.
Feature Engineering: Created new features and handled outliers (e.g., outliers in CNT_CHILDREN and placeholder values like DAYS_EMPLOYED with 365243 days).
Encoding: Applied various encoding techniques including one-hot encoding, label encoding, binary encoding, and frequency encoding depending on the nature of the columns.
Balancing the Dataset: The dataset was imbalanced, with significantly fewer rejected applications. SMOTENC (Synthetic Minority Over-sampling Technique for Nominal and Continuous data) was used to balance the dataset for better model performance.
Modeling
Several models were built and combined to improve prediction accuracy. The models used include:

Base Models:

Random Forest
EasyEnsemble Classifier
RUSBoost Classifier
Ensemble Approach: The outputs of the base models were combined using Logistic Regression as a meta-classifier to improve robustness and generalizability.

Evaluation Metrics:
Accuracy
Precision
Recall
F1 Score
ROC-AUC
Deployment
The final model was deployed using a Flask web application, with a user-friendly interface built using HTML and CSS. The application allows users to input new applicant data and receive an instant prediction on whether the credit card will be approved or rejected.
