# Week 2 – Data Preparation for Machine Learning

**Dataset:** Loan Prediction (`loan_prediction.csv`, 614 rows × 13 columns)
**Source:** Kaggle / Analytics Vidhya "Loan Prediction Problem" training data
(CSV copy used from https://github.com/shrikant-temburwar/Loan-Prediction-Dataset)

## Summary
This project takes the raw loan data and prepares it for a machine learning model that predicts whether a loan
will be approved (`Loan_Status`). I explored the data with charts, removed useless columns, handled missing values,
and created new features (`TotalIncome`, `EMI`, `LoanToIncome`). Then I split the data 80/20 with stratification
and used a `ColumnTransformer` (median + StandardScaler for numbers, most-frequent + OneHotEncoder for text).
All preprocessing is fitted on the training data only, so there is no data leakage.
The final output is `X_train`, `X_test`, `y_train`, `y_test`.