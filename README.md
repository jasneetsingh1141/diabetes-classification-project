# diabetes-classification-project
Binary classification of diabetes using Logistic Regression and Random Forest with data preprocessing and model evaluation.

This project applies machine learning techniques to predict diabetes using the Pima Indians Diabetes Dataset. It demonstrates a complete data science workflow including data preprocessing, exploratory data analysis (EDA), model training, evaluation, and performance improvement.

Project Overview
The objective of this project is to build and evaluate binary classification models that can accurately predict whether a patient is diabetic based on clinical and demographic features.

The workflow includes:
Data quality assessment
Handling invalid values (removal of zero-value records)
Exploratory Data Analysis (EDA)
Feature selection
Model training and evaluation
Model improvement and comparison

Data Preprocessing
Several features in the dataset contain zero values, which are not physiologically valid (e.g., Glucose, BMI, Insulin).
Instead of imputing, this project removes rows containing invalid values to ensure high data quality.

Original dataset size: 768 samples
Cleaned dataset size: 392 samples

This introduces a trade-off between:
Better data quality
Reduced dataset size (potential impact on generalizability)

Models Used
1. Logistic Regression (Baseline)
Simple and interpretable
Serves as a benchmark model
2. Balanced Logistic Regression
Uses class_weight='balanced'
Addresses class imbalance
Improves recall (important for medical tasks)
3. Random Forest
Captures non-linear relationships
Ensemble-based approach

Key Findings
Logistic Regression provided strong baseline performance
Balanced Logistic Regression significantly improved recall
Random Forest performed well but did not outperform balanced LR in detecting diabetic cases
Best Model: Balanced Logistic Regression
Reason: Higher recall → better identification of diabetic patients
