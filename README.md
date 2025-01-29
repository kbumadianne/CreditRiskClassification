# CreditRiskClassification
code file: Credit_Risk / credit_risk_classification.ipynb
report file: Credit_Risk / credit_risk_report.md


Overview
This analysis aims to build a model that can predict the creditworthiness of loan borrowers based on historical lending data. The dataset comes from a peer-to-peer lending services company and includes various features such as loan size, interest rate, borrower income, debt-to-income ratio, and more. The target variable is loan_status, which indicates whether a loan is healthy (0) or high-risk (1).

Key Variables
The dataset includes the following features:

Loan Size
Interest Rate
Borrower Income
Debt-to-Income Ratio
Number of Accounts
Derogatory Marks
Total Debt
The target variable is loan_status:

0: Healthy loan
1: High-risk loan
There is a class imbalance, as there are far more healthy loans (0) than high-risk loans (1).

Machine Learning Process
1. Data Preparation
The dataset was split into features (X) and labels (y).
loan_status was the target variable.
2. Data Splitting
The dataset was divided into training and testing sets using train_test_split(), ensuring the model was trained on one portion and evaluated on another.
3. Model Selection
Logistic Regression was chosen as the initial machine learning model.
4. Model Evaluation
The model was evaluated using:
Confusion Matrix
Classification Report (Precision, Recall, F1-score)
Accuracy Score

Results
Logistic Regression Model
Accuracy: 93.5% – The model correctly predicted whether a loan was healthy or high-risk 93.5% of the time.

Precision & Recall for Class 0 (Healthy Loans):

Precision: 1.00
Recall: 0.99
Precision & Recall for Class 1 (High-Risk Loans):

Precision: 0.85
Recall: 0.95
Key Insights:
The Logistic Regression model performs well with high accuracy (93.5%) and solid recall for high-risk loans (95%).
However, precision for high-risk loans (85%) could be improved.
Summary:
Performance: The Logistic Regression model balances accuracy and recall for high-risk loans well but can be further optimized for precision.
Recommendations: Improving precision can be achieved through hyperparameter tuning, adjusting class weights, or using different models such as Random Forest or XGBoost.
