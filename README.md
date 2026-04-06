📌 Diabetes Classification Analysis
📖 Project Overview
This project applies data science and machine learning techniques to analyze the Pima Indians Diabetes Dataset and build predictive models for diabetes classification. The workflow includes data cleaning, exploratory data analysis (EDA), model development, performance evaluation, and model improvement using multiple strategies.
The goal is to develop a model that not only performs well overall but is also effective at identifying diabetic cases. This is especially important in medical screening, where failing to detect true cases can have serious consequences.
🎯 Objectives
Perform data quality assessment and preprocessing
Conduct exploratory data analysis (EDA) with meaningful visualizations
Train a baseline classification model
Evaluate model performance using multiple metrics
Improve model performance using:
Feature selection
Class balancing
Hyperparameter tuning
Implement an alternative model (Random Forest)
Compare all models and select the best-performing one
📊 Dataset
Name: Pima Indians Diabetes Dataset
Source:
https://github.com/npradaschnor/Pima-Indians-Diabetes-Dataset
Description:
The dataset contains medical diagnostic measurements used to predict whether a patient has diabetes.
Features:
Pregnancies
Glucose
BloodPressure
SkinThickness
Insulin
BMI
DiabetesPedigreeFunction
Age
Target:
Outcome (0 = Non-diabetic, 1 = Diabetic)
🧹 Data Preprocessing
Identified invalid zero values in key medical features:
Glucose, BloodPressure, SkinThickness, Insulin, BMI
Removed rows containing these values
Dataset reduced from 768 → 392 samples
👉 This improves data reliability but introduces a trade-off between data quality and dataset size.
📈 Exploratory Data Analysis (EDA)
The following visualizations were used:
Count Plot: Revealed class imbalance
Histograms: Showed feature distributions and skewness
Correlation Heatmap: Identified key predictors (Glucose, BMI, Age, Pregnancies)
Boxplot (Glucose vs Outcome): Showed higher glucose levels in diabetic individuals
👉 EDA helped guide feature selection and modeling decisions.
🤖 Models Implemented
1. Baseline Logistic Regression
Trained using all features
Provided a benchmark for comparison
2. Logistic Regression with Feature Selection
Used key features:
Glucose, BMI, Age, Pregnancies
Reduced noise and improved interpretability
3. Balanced Logistic Regression
Applied class_weight='balanced'
Addressed class imbalance
Improved recall significantly
4. Tuned Logistic Regression
Used GridSearchCV
Tuned regularization parameter (C)
Did not significantly improve performance
5. Random Forest (Alternative Model)
Tree-based ensemble model
Captures non-linear relationships
Compared with Logistic Regression models
📊 Model Performance Summary
Model	Accuracy	Precision	Recall	F1 Score	ROC-AUC
Baseline Logistic Regression	0.835	0.783	0.692	0.735	0.888
Feature Selection LR	0.835	0.760	0.731	0.745	0.876
Balanced Logistic Regression	0.810	0.677	0.808	0.737	0.877
Tuned Logistic Regression	0.797	0.656	0.808	0.724	0.878
Random Forest	0.810	0.720	0.692	0.706	0.862
📌 Key Insights
Glucose is the strongest predictor of diabetes
Removing invalid values significantly improved data quality
Feature selection improved model simplicity and performance
Class imbalance handling was critical for improving recall
Hyperparameter tuning did not always improve performance
Random Forest did not outperform Logistic Regression
🏆 Final Model Selection
👉 Balanced Logistic Regression was selected as the best model because:
Highest recall (0.81)
Lowest false negatives
Most suitable for medical screening
In healthcare applications, recall is more important than precision, as missing true diabetic cases can have serious consequences.
📉 Evaluation Metrics Used
Accuracy
Precision
Recall
F1 Score
ROC-AUC
Confusion Matrix
📊 Visualizations
Feature distributions
Correlation heatmap
Confusion matrices for all models
ROC curve comparison
🧠 Conclusion
This project demonstrates the importance of proper data preprocessing, feature selection, and model evaluation in building reliable classification models. While multiple models performed well, Balanced Logistic Regression provided the best balance between predictive performance and practical usability.
The study highlights that simpler models can often outperform more complex ones when the data relationships are well-structured.
🛠️ Technologies Used
Python
Pandas
NumPy
Matplotlib
Seaborn
Scikit-learn
🚀 How to Run the Project
Clone the repository:
git clone https://github.com/jasneetsingh1141/diabetes-classification-project.git
Open the notebook:
cd diabetes-classification-project
Run the notebook in:
Jupyter Notebook OR
Google Colab
📁 Repository Structure
diabetes-classification-project/
│
├── diabetes_classification.ipynb
├── README.md
└── requirements.txt (optional)
📌 Author
Jasneet Singh
PhD Student
Department of Agricultural, Food & Nutritional Sciences
University of Alberta
