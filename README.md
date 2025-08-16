# Telecom Customer Churn Prediction

## Project Overview
This project, completed as part of the **Estarta Internship**, focuses on predicting **customer churn** for a telecom company using machine learning. The goal is to help telecom providers identify customers at risk of leaving and improve service retention.

## Dataset
The dataset is publicly available from the **CrowdAnalytix Community** churn prediction competition. It contains **3333 customer records** with 20 features, including usage patterns, service plans, and customer support interactions. The target variable is `Churn`.

## Data Quality and Preparation
- Checked for **missing values** and **duplicates** (none found).  
- Outliers in numerical features were retained as they represent valid customer behavior.  
- Numerical features were analyzed for **correlation** to reduce redundancy.  
- Categorical features (`International plan`, `Voice mail plan`, `State`) were **encoded**, and the target variable `Churn` was converted to numeric.  
- Data was split into **training (80%)** and **testing (20%)** sets.  
- **Standard scaling** was applied to numerical features.

## Feature Analysis
- **Chi-square test** was performed for categorical features (e.g., `State`).  
- **Information gain** was calculated for numerical features to identify important predictors.  
- Feature importance was later evaluated using **XGBoost**.

## Modeling
Three models were trained and evaluated:  
1. **Logistic Regression**  
2. **Decision Tree**  
3. **XGBoost**  

Model performance was assessed using the **confusion matrix**, **precision**, **recall**, **F1-score**, and **ROC-AUC**, considering the imbalanced nature of the dataset.

## Key Findings
- **XGBoost** achieved the highest performance with an accuracy of ~95.5% and ROC-AUC of 0.9146.  
- Most important features included customer service calls, total day charge, and service plan indicators.  

## Files in the Repository
- **`churn_prediction.ipynb`** – Jupyter Notebook containing data preprocessing, feature analysis, modeling, and results.  
- **`Customer Churn Prediction in the Telecom Industry - Report.pdf`** – Project report summarizing the methodology, findings, and conclusions.  
