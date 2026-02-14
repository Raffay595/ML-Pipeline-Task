# Customer Churn Prediction – End-to-End ML Pipeline

## Project Overview

This project builds a production-ready machine learning pipeline to predict customer churn using the Telco Customer Churn dataset.

The solution uses Scikit-learn’s Pipeline and ColumnTransformer APIs to ensure clean preprocessing, prevent data leakage, and enable reusability. Multiple models are trained and optimized using GridSearchCV, and the final pipeline is exported using joblib for deployment or future use.

---

## Objective

The main objectives of this project are:

- Build an end-to-end ML pipeline using Scikit-learn
- Implement preprocessing (scaling and encoding) inside a Pipeline
- Train Logistic Regression and Random Forest models
- Perform hyperparameter tuning using GridSearchCV
- Export the final trained pipeline for reuse
- Follow production-ready ML practices

---

## Dataset

- **Dataset:** Telco Customer Churn
- **Source:** IBM Sample Dataset
- **Target Variable:** Churn (Yes / No)
- **Task Type:** Binary Classification

The dataset includes customer demographic information, account details, services subscribed, and billing information.

---

## Machine Learning Approach

### 1. Data Preprocessing
- Dropped irrelevant columns (customerID)
- Converted `TotalCharges` to numeric
- Handled missing values
- Encoded target variable to binary (0/1)

### 2. Feature Engineering
- Numerical features scaled using StandardScaler
- Categorical features encoded using OneHotEncoder
- Combined preprocessing using ColumnTransformer

### 3. Model Training
Two models were implemented:

- Logistic Regression
- Random Forest Classifier

### 4. Hyperparameter Tuning
- GridSearchCV with 5-fold cross-validation
- Optimization metric: F1-score

---

## Model Evaluation Metrics

Models were evaluated using:

- Accuracy
- F1-score
- Classification Report

F1-score was prioritized due to class imbalance considerations in churn prediction.

---

## Model Export

The final selected pipeline is exported using:

joblib.dump(final_model, "churn_pipeline.pkl")


This allows:

- Reusing the trained model
- Deploying in production
- Loading without retraining

---

## Skills Demonstrated

- End-to-end ML pipeline construction
- ColumnTransformer for structured preprocessing
- Hyperparameter tuning with GridSearchCV
- Cross-validation techniques
- Model serialization with joblib
- Production-ready ML workflow design

---

Key Takeaways

- Pipelines prevent data leakage and ensure reproducibility.
- Hyperparameter tuning significantly improves model performance.
- Exporting the full pipeline makes the solution deployment-ready.
- Clean structure and modular code are critical for production ML systems.

---
