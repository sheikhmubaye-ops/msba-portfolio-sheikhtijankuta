# MSBA Portfolio – Customer Churn Prediction
Author: Sheikh Tijan Kuta  
Course: Predictive Analytics – Spring 2026  

## Business Problem

This project predicts customer churn for TruSource, a subscription-based service provider.  
The goal is to identify customers likely to leave and provide actionable recommendations to improve retention and long-term profitability.

## Key Results

- XGBoost model achieved **ROC-AUC = 0.8937**, outperforming logistic regression and random forest.
- Month-to-month contracts and early tenure customers were the strongest predictors of churn.
- Customers with 3+ referrals and multiple services were significantly less likely to churn.

## How to Run This Project

1. Clone this repository  
2. Open the notebook or Python script in Jupyter/VS Code  
3. Install required libraries (pandas, sklearn, xgboost, shap)  
4. Run preprocessing section  
5. Run model training section  
6. Review evaluation metrics and SHAP plots  

## Limitation / Risk

The dataset is imbalanced (more non-churn than churn), which may bias predictions.  
Although scale_pos_weight was used in XGBoost, real-world deployment would require continuous monitoring and recalibration.
