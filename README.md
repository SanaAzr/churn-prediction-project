# Churn Prediction Project

This project is a solution to a Data Science challenge from Coursera focused on predicting customer churn for a video streaming service. The goal is to predict whether a subscription will be continued for another month, utilizing a dataset of customer information and usage patterns.

## Project Overview

- **Objective:**  
  Predict the probability that a customer will churn (i.e., cancel or not renew their subscription).

- **Dataset:**  
  The data consists of customer subscription records with features such as account age, monthly charges, total charges, subscription type, payment method, usage metrics, and more.

- **Methodology:**
  - **Data Preprocessing:**
    - Separated numerical and categorical features.
    - Standardized numerical features using `StandardScaler`.
    - Encoded categorical features using `OneHotEncoder`.
    - Utilized a `ColumnTransformer` for unified preprocessing.
  - **Modeling:**  
    A Random Forest Classifier was used within a scikit-learn Pipeline to predict churn. Key parameters include:
    - `n_estimators=500` (number of trees in the forest)
    - `random_state=42` for reproducibility.
  - **Prediction:**  
    The model was trained on historical data (train.csv) and used to predict churn probabilities for the test dataset. The predictions (probabilities between 0 and 1) are output in a DataFrame along with the `CustomerID`.

## Model Performance

- **Evaluation Metric:**
  The model is evaluated using the ROC AUC (Receiver Operating Characteristic Area Under the Curve) metric.

- **Final Score:**
  The final ROC AUC score achieved by the model is 0.74.
