# Predicting-Credit-Card-Approval

## Project Description
Commercial banks receive a lot of applications for credit cards. Many of them get rejected for many reasons, like high loan balances, low income levels, or too many inquiries on an individual's credit report, for example. Manually analyzing these applications is mundane, error-prone, and time-consuming (and time is money!). Luckily, this task can be automated with the power of machine learning and pretty much every commercial bank does so nowadays. In this project, you will build an automatic credit card approval predictor using machine learning techniques, just like the real banks do.

The dataset used in this project is the Credit Card Approval dataset from the UCI Machine Learning Repository.

## Topics
- Data Manipulation
- Machine Learning
- Importing and Cleaning data
- Applied Finance

## Dependencies 
- `Pandas`
- `Sklearn`
- `Numpy`

## The structure of this notebook is as follows: 
1. Load and inspect data with `.describe()` and `info()`
2. Handle missing value with `.isnull()`, `.replace('?', np.nan)`, `.fillna()`
    - For numerical data: impute missing values with mean imputation
    - For categorical data: impute missing values with most frequent value 
3. Preprocess data
    - Convert non-numeric data to numeric data `sklearn.preprocessing.LabelEncoder`
    - Split the data into test and train set `sklearn.model_selection.train_test_split`
    - Scale the features to a uniform range (Normalization) `MinMaxScaler`
 4. Fit a logistic regression model to the train set and evaluate its performance on the test set.
    - Find the accuracy of the model `logreg.score=0.8377`
    - Also take a look at the confusion matrix `sklearn.metrics.confusion_matrix` `confusion_matrix(y_test, y_pred)`
 5. Hyperparameter Tuning
    - `sklearn.model_selection.GridSearchCV`
    - `tol` , `max_iter`
    - The best model achieved an accuracy of 0.8507.
