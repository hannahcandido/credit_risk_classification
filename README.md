# credit_risk_classification

Overview of the Analysis
The purpose of this analysis was to evaluate machine learning models that can predict the likelihood of a loan defaulting. The goal was to use historical data on loans to predict whether a loan will be healthy (low risk of default) or high-risk (likely to default).
Financial Information and Prediction Goal:
The dataset provided information on a series of loans, with a focus on predicting whether each loan is:
•	Healthy (0) – meaning the loan is performing well with no sign of default.
•	High-risk (1) – meaning the loan is at high risk of defaulting.
The key variable to predict was the loan_status column, where:
•	0 denotes a healthy loan,
•	1 denotes a high-risk loan.
To achieve this, machine learning models were used to train on the features (such as borrower details, loan information, etc.) and predict the risk status of loans.
Stages of the Machine Learning Process:
1.	Data Preprocessing:
o	Split the data into features (X) and labels (y), where X contained all columns except for loan_status, and y was the loan_status column.
2.	Model Training and Testing:
o	Split the dataset into training (75%) and testing (25%) sets using train_test_split.
o	Trained a Logistic Regression model on the training data (X_train and y_train).
3.	Used the confusion matrix and classification report to evaluate the model's performance.
4.	Focused on accuracy, precision, recall, and F1-score metrics.
5.	Logistic Regression: The model used here was a Logistic Regression model, which is a statistical model commonly used for binary classification tasks. The logistic regression model was fitted to the data, and predictions were made on the test set to evaluate its performance.
6.	Also evaluated precision, recall, and F1-scores to understand the model's behavior with respect to both the healthy loans and the high-risk loans.
Results
Machine Learning Model 1: Logistic Regression
•	Accuracy:
o	0.99: The model achieved a high overall accuracy, indicating that it correctly predicted the loan status (healthy or high-risk) most of the time.
•	Precision (Class 0 - Healthy Loan):
o	1.00: The model was very precise in predicting healthy loans, meaning very few false positives were observed for class 0.
•	Recall (Class 0 - Healthy Loan):
o	0.99: The model was able to correctly identify 99% of the actual healthy loans, indicating good recall for this class.
•	Precision (Class 1 - High-Risk Loan):
o	0.84: The model was less precise in predicting high-risk loans, meaning there were more false positives compared to class 0.
•  Recall (Class 1 - High-Risk Loan):
•	0.94: The model had a relatively high recall for high-risk loans, correctly identifying 94% of actual high-risk loans.
•  F1-Score (Class 1 - High-Risk Loan):
•	0.89: The balance between precision and recall for high-risk loans was decent, though there is still some room for improvement.
Summary
Model Performance:
•	Logistic Regression performed very well for the majority class (healthy loans), but struggled with the minority class (high-risk loans).
o	The high precision for class 0 and high recall for class 1 indicate that the model is quite good at identifying healthy loans, but it may miss some high-risk loans due to lower precision.
o	The overall accuracy of 0.99 is very high, but given the class imbalance, the model could still be biased toward predicting the majority class (healthy loans).
Logistic Regression is a strong candidate for this problem due to its simplicity and solid performance in predicting the majority class.
