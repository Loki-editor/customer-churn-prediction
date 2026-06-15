# Customer Churn Prediction and Analysis Using Machine Learning

## Project Overview

Customer churn is one of the most important challenges faced by telecom companies. Churn occurs when customers stop using a company's services and switch to competitors. Predicting customer churn enables organizations to identify high-risk customers and implement retention strategies before customers leave.

This project applies machine learning techniques to analyze telecom customer data, predict customer churn, estimate monthly charges, and generate business insights through explainable AI methods. The project follows a complete machine learning pipeline, including exploratory data analysis, data preprocessing, model development, evaluation, and interpretation.

---

## Objectives

The main objectives of this project are:

- Analyze customer behavior and service usage patterns.
- Identify factors that contribute to customer churn.
- Build classification models to predict customer churn.
- Build regression models to predict monthly charges.
- Apply feature engineering and feature selection techniques.
- Handle class imbalance using SMOTE and class weighting.
- Interpret model predictions using SHAP explainability.
- Evaluate fairness and bias across customer groups.
- Provide actionable business recommendations to reduce churn.

---

## Dataset Information

The dataset contains telecom customer information, including:

- Customer demographics
- Service subscriptions
- Contract information
- Payment methods
- Monthly charges
- Total charges
- Churn status

Target Variable:

### Classification Target
- Churn
  - 1 = Customer leaves the company
  - 0 = Customer stays with the company

### Regression Target
- MonthlyCharges

---

## Project Workflow

### Task 1: Exploratory Data Analysis (EDA)

Performed comprehensive exploratory analysis to understand the dataset.

Activities:
- Dataset overview
- Missing value analysis
- Outlier detection using IQR
- Correlation analysis
- Univariate analysis
- Bivariate analysis
- Business insight generation

Tools Used:
- Pandas
- NumPy
- Matplotlib
- Seaborn

---

### Task 2: Data Preprocessing

Prepared the dataset for machine learning.

Techniques Applied:

#### Encoding
- Label Encoding
- One-Hot Encoding

#### Feature Scaling
- StandardScaler
- MinMaxScaler

#### Feature Engineering
Created new features:
- AvgMonthlySpend
- ServiceCount
- IsLongTermCustomer

#### Feature Selection
- Correlation Analysis
- Random Forest Feature Importance

#### Class Imbalance Handling
- SMOTE
- Class Weighting

#### Data Splitting
- Training Set (70%)
- Validation Set (15%)
- Test Set (15%)

---

### Task 3: Classification Models

Developed and compared multiple classification models for churn prediction.

Models Implemented:

1. Logistic Regression
2. Decision Tree Classifier
3. Random Forest Classifier
4. Support Vector Machine (SVM)
5. K-Nearest Neighbors (KNN)

Evaluation Metrics:
- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score
- Confusion Matrix

#### Best Classification Model

Logistic Regression

Performance:

- Accuracy: 74.34%
- Precision: 50.99%
- Recall: 82.14%
- F1 Score: 62.93%
- ROC-AUC: 84.99%

Logistic Regression was selected because it achieved the highest recall and F1 score, making it highly effective at identifying customers likely to churn.

---

### Task 4: Regression Models

Developed regression models to predict monthly customer charges.

Models Implemented:

1. Linear Regression
2. Ridge Regression
3. Lasso Regression
4. ElasticNet
5. Decision Tree Regressor
6. Random Forest Regressor
7. Support Vector Regressor (SVR)

Evaluation Metrics:
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

#### Best Regression Model

Linear Regression

Performance:

- MAE: 0.789
- RMSE: 1.049
- R² Score: 0.9988

Linear Regression achieved the highest R² score and lowest prediction error among all regression models.

---

### Task 5: Model Interpretation and Explainability

To improve transparency and trustworthiness, model interpretation techniques were applied.

#### SHAP Analysis

SHAP (SHapley Additive exPlanations) was used to identify the impact of individual features on churn predictions.

Most Influential Features:

- InternetService_Fiber optic
- tenure
- Contract_Two year
- TotalCharges
- PaymentMethod_Electronic check
- MonthlyCharges

#### Feature Importance

Random Forest feature importance analysis was performed to identify the most critical predictors.

#### Fairness Evaluation

Gender-based churn rates were analyzed.

Results showed similar churn rates across genders, indicating minimal gender bias.

#### Bias Detection

Senior citizens exhibited a significantly higher churn rate compared to non-senior citizens.

This suggests that targeted retention strategies should be developed for senior customers.

---

## Business Recommendations

Based on the analysis, the following recommendations are proposed:

1. Focus retention efforts on customers with short tenure.
2. Encourage customers to adopt long-term contracts.
3. Improve service quality for fiber optic internet users.
4. Provide loyalty rewards and discounts for high-value customers.
5. Develop targeted retention campaigns for senior citizens.
6. Monitor customers using electronic check payment methods.
7. Enhance customer support services to reduce dissatisfaction.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- Matplotlib
- Seaborn
- SHAP
- Google Colab
- GitHub

---

## Repository Structure

```
customer-churn-prediction/
│
├── 01_EDA.ipynb
├── 02_Preprocessing.ipynb
├── 03_Classification.ipynb
├── 04_Regression.ipynb
├── 05_Interpretation.ipynb
│
├── Telco_Customer_Churn.csv
├── processed_telco.csv
│
└── README.md
```

---

## Conclusion

This project successfully implemented a complete machine learning pipeline for customer churn prediction and analysis. Through extensive data preprocessing, classification, regression, and explainability techniques, valuable insights were generated regarding customer behavior and churn patterns.

The results demonstrate that machine learning can effectively identify customers at risk of churn and support data-driven business decisions aimed at improving customer retention and profitability.

---

## Author

Lokesh S

Bachelor of Technology (Artificial Intelligence and Machine Learning)

Saveetha Engineering College
