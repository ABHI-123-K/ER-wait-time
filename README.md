# ER-wait-time
# Machine Learning Model Training for Emergency Department Triage Prediction

## Overview

This module focuses on building and evaluating machine learning models to predict a patient's **Urgency Level** based on hospital visit and operational data. The objective is to compare multiple classification algorithms and identify the model that provides the best predictive performance.

---

## Dataset

The dataset contains emergency department visit records with features such as:

- Region
- Day of Week
- Season
- Time of Day
- Nurse-to-Patient Ratio
- Specialist Availability
- Facility Size (Beds)
- Time to Registration
- Time to Triage
- Time to Medical Professional
- Total Wait Time
- Patient Outcome
- Patient Satisfaction

**Target Variable**

- Urgency Level

The following identifier columns were removed before training as they do not contribute to prediction:

- Visit ID
- Patient ID
- Hospital ID
- Hospital Name
- Visit Date

---

## Data Preprocessing

The preprocessing pipeline included:

- Handling categorical variables using Label Encoding
- Removing identifier columns
- Separating features and target variable
- Stratified Train-Test Split (80:20)
- Feature scaling using StandardScaler for Logistic Regression

---

## Machine Learning Models

Three supervised learning algorithms were trained and compared.

### 1. Logistic Regression

- Baseline linear classification model
- Standardized input features
- Used for comparison against ensemble methods

### 2. Random Forest Classifier

- Ensemble learning using multiple decision trees
- Handles nonlinear relationships
- Provides feature importance

### 3. XGBoost Classifier

- Gradient Boosting based ensemble model
- Optimized for high predictive performance
- Selected as the final model based on evaluation metrics

---

## Model Evaluation

Each model was evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

The best-performing model was selected after comparing these metrics.

---

## Libraries Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn
- Joblib

---

## Project Workflow

1. Load Dataset
2. Clean and preprocess data
3. Encode categorical features
4. Remove unnecessary identifier columns
5. Split dataset into training and testing sets
6. Scale features for Logistic Regression
7. Train Logistic Regression
8. Train Random Forest
9. Train XGBoost
10. Compare model performance
11. Save the best trained model

---

## Output

The training process generates:

- Performance comparison of all models
- Confusion matrices
- Classification reports
- Best trained model (`best_model.pkl`)

---

## Future Improvements

- Hyperparameter tuning using GridSearchCV
- Explainable AI using SHAP
- Real-time prediction integration
- Deployment using Streamlit
- Cross-validation for improved generalization

---

## Authors

Developed as part of the **HackWithIndia Machine Learning Track**.
