# Customer Churn Prediction in Telecom

## Overview
Customer churn is a critical problem in the telecom industry, where retaining existing customers is often more cost-effective than acquiring new ones. This project formulates churn prediction as a binary classification problem, aiming to identify customers who are likely to leave the service based on historical usage, service, and demographic data.

## Problem Statement
Telecom churn datasets are typically highly imbalanced, with churned customers forming a small fraction of the total population. Traditional classifiers tend to perform poorly under this setting, often missing churn cases (false negatives). The objective of this project is to build a machine learning pipeline that improves churn detection while explicitly addressing class imbalance.

## Dataset
- Structured telecom customer data containing usage patterns, service details, and customer attributes  
- Target variable: **Churn (Yes / No)**  
- Significant class imbalance between churned and non-churned customers  

## Methodology

### Data Analysis and Preprocessing
- Performed exploratory data analysis (EDA) to understand feature distributions and churn-related patterns  
- Handled missing values and encoded categorical variables  
- Applied feature engineering to improve model interpretability and predictive performance  

### Class Imbalance Handling
- Implemented resampling techniques such as **SMOTE** and **SMOTEENN**  
- Compared model behavior before and after resampling to evaluate improvements in minority-class detection  

### Modeling
- Trained and evaluated multiple supervised learning models, including:
  - Logistic Regression  
  - Random Forest  
  - XGBoost  
- Used **Scikit-learn** for model training and evaluation  

### Evaluation Metrics
- Accuracy (used cautiously due to class imbalance)  
- F1-score  
- Precision and Recall  
- Confusion Matrix  
- ROC-AUC  

Special emphasis was placed on reducing **false negatives**, as missed churn cases are costly in real-world scenarios.

## Results
Resampling techniques significantly improved recall and F1-score for the churn class. Ensemble-based models demonstrated better robustness compared to linear models. The final model achieved improved churn detection without severely impacting overall performance.

## Tools and Technologies
- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib  

## Key Takeaways
- Class imbalance has a major impact on churn prediction performance  
- Resampling techniques are effective when combined with appropriate evaluation metrics  
- Model selection should be guided by business objectives, not accuracy alone  

## Future Improvements
- Incorporate cost-sensitive learning  
- Explore model explainability techniques (e.g., feature importance, SHAP)  
- Extend the pipeline to real-time or streaming data scenarios  
