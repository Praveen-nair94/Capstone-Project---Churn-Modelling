# Capstone-Project---Churn-Modelling
Customer churn is a concerning problem for large companies (especially in the Telecom field) due to its direct effect on the revenues. Companies often seek to know which customers are likely to churn in the recent future so that a timely action could be taken to prevent it
# Customer Churn Prediction

Customer churn prediction is a common problem faced by businesses, especially in the telecom industry. This project focuses on building a machine learning model to predict customer churn and take proactive measures to retain customers.

## Table of Contents
- [About](#about)
- [Dataset](#dataset)
- [Features](#features)
- [Model Building](#model-building)
- [Model Evaluation](#model-evaluation)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## About

This project aims to develop a logistic regression machine learning model to predict customer churn for a telecom company. By identifying customers at risk of churning, the company can take targeted actions to retain them, thereby reducing revenue loss.

## Dataset

The dataset used for this project contains 11 features, including account duration, contract renewal status, data plan subscription, usage metrics, and customer service calls, among others. The target variable is 'Churn', indicating whether a customer has churned or not.

## Features

- Churn (Target variable)
- AccountWeeks: Number of weeks the customer has had an active account
- ContractRenewal: Whether the customer recently renewed their contract (1 if yes, 0 if no)
- DataPlan: Whether the customer has a data plan (1 if yes, 0 if no)
- DataUsage: Gigabytes of monthly data usage
- CustServCalls: Number of calls into customer service
- DayMins: Average daytime minutes per month
- DayCalls: Average number of daytime calls
- MonthlyCharge: Average monthly bill
- OverageFee: Largest overage fee in the last 12 months
- RoamMins: Average number of roaming minutes

## Model Building

The project involves the following steps in model building:
- Data preprocessing: Handling missing values, encoding categorical variables, and scaling numerical features.
- Model selection: Training logistic regression and random forest classifiers.
- Model evaluation: Assessing model performance using metrics such as accuracy, precision, recall, and F1-score.
- Hyperparameter tuning: Optimizing model parameters using techniques like grid search and cross-validation.

## Model Evaluation

### Logistic Regression
- Train Accuracy: 0.86
- Test Accuracy: 0.86
- Confusion Matrix:
  [[555  11]
   [ 83  18]]
- Classification Report:

          precision    recall  f1-score   support

       0       0.87      0.98      0.92       566
       1       0.62      0.18      0.28       101

accuracy                           0.86       667

macro avg 0.75 0.58 0.60 667
weighted avg 0.83 0.86 0.82 667


### Random Forest (with resampling)
- Test Accuracy: 0.91
- Confusion Matrix:
[[537  29]
 [ 30  71]]
- Classification Report:
          precision    recall  f1-score   support

       0       0.95      0.95      0.95       566
       1       0.71      0.70      0.71       101

accuracy                           0.91       667

macro avg 0.83 0.83 0.83 667
weighted avg 0.91 0.91 0.91 667


## Deployment

The model can be deployed for real-time predictions using a web application or API. Flask or FastAPI can be used to create a web service that takes input data and returns churn predictions.

## Contributing

Contributions are welcome! Feel free to fork the repository, make changes, and submit pull requests.

## License

This project is licensed under the [MIT License](LICENSE).
