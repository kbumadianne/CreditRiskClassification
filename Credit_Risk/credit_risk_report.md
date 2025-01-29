# Credit Risk Report

## Credit Risk Analysis

The below data and analysis was taken into consideration for the Credit Risk Report:

* The purpose of this analysis was to build a model that can determine the creditworthiness of loan borrowers.
* The dataset is historical lending activity from a peer-to-peer lending services company, inclusive of 
    * loan size
    * interest rate
    * borrower income
    * debt to income
    * number of accounts
    *  derogatory marks
    * total debt
    * loan status.
* Using the above data points from historical lending, this analysis is trying to make correlations and predictions on if a loan would be healthy or high-risk.
* The code trying to predict the loan_status variable, which indicates whether a loan is healthy (0) or high-risk (1). Here's a summary of the variable distribution:
    * Value 0 (healthy loan) : instances
    * Value 1 (high-risk loan) : instances
    * This shows that there is a large class imbalance as there are far more healthy loans (0) than high-risk loans(1), which is important to consider when evaluating model performance

* Stages of the machine learning process for the analysis:
* Data Splitting:
    * Split the dataset into training and testing sets using train_test_split(), ensuring the model is trained on one portion of the data and evaluated on a separate portion.
* Model Selection:
    * Chose Logistic Regression as the machine learning model.
* Model Fitting:
    * Instantiated a LogisticRegression model and trained it on the training dataset (X_train, y_train).
* Prediction:
    * Trained model to predict the loan status on the testing dataset (X_test).
* Model Evaluation:
* Evaluated the model using:
    * Confusion Matrix: Shows how well the model predicted each class (healthy vs. high-risk).
    * Classification Report: Provides precision, recall, and F1-score for both classes (0 and 1).
    * Accuracy Score: Gives a simple measure of overall correct predictions.


## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model:
  * Here are the performance metrics for the Logistic Regression model:

* Accuracy:
* Accuracy is 93.5%. This means that the model correctly predicts whether a loan is healthy or high-risk 93.5% of the time.

* Precision and Recall for Class 0 (Healthy Loans):
    * Precision: 1.00
    * Recall: 0.99
    * The model is very good at predicting healthy loans, with virtually no false positives (high precision) and missing only 1% of the actual healthy loans (slightly lower recall).

* Precision and Recall for Class 1 (High-Risk Loans):
    * Precision: 0.85
    * Recall: 0.95
    * The model is good at identifying high-risk loans, with a recall of 95%. However, its precision is lower at 85%, indicating that some of the loans predicted as high-risk are actually healthy (false positives).

## Summary

*  The Logistic Regression model seems to perform well with high accuracy (93.5%) and solid recall for high-risk loans (95%). However, its precision for high-risk loans (85%) could be improved

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
    * Yes, performance depends on the problem. If the goal is to avoid false negatives (missing high-risk loans), then recall (which is high for class 1) is very important. However, if the goal is to minimize false positives (predicting healthy loans as high-risk), then precision (which is lower for class 1) becomes more critical.
    * In this case, the imbalance in the dataset (many more healthy loans than high-risk loans) suggests that recall is important for capturing most of the high-risk loans. However, improving precision would be beneficial to avoid misclassifying healthy loans as high-risk.

* Overall the Logistic Regression model performs well for this problem, but improvements could be made by adjusting class weights, trying different algorithms (e.g., Random Forest or XGBoost), or performing hyperparameter tuning to address the imbalance and improve precision for the high-risk loans.


