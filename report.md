# Module 12 Report

## Overview of the Analysis

In this project, I have utilized a Logistic Regression model to predict whether loans are healthy or high risk. The purpose of this model is to utilize historic loan status data to predict a healthy or high risk loan status on a potential new loan. The training data included the following fields to train on.

* loan_size
* interest_rate
* borrower_income
* debt_to_income
* num_of_accounts
* derogatory_marks
* total_debt

The first step was to seperate out the training data from the testing data. I utilized the train_test_split function of SciKitLearn to seperate out the data.

The data needed to be scaled to not give any special weight to any particular field. I utilized the StandardScaler function inlcuded in SciKitLearn to scale the data. I then utilized the "lbfgs" Logistic Regression solver to generate a classification model.

## Results

This model proved to be very accurate when tested with our seperated out test data.

* Linear Regression Model:
    * Accuracy: 1.00 (100%)
    * Healthy Loan Precision: 1.00 (100%)
    * High Risk Loan: 0.84 (84%)
    * Healthy Loan Recall: 0.99
    * High Risk Loan Recall: 0.99

## Summary

The logistic regression model is very accurate. It is accurate in a few different ways. 1. The model is generally accurate 99% of the time. However it has a precision for predicting healthy loans at 100% precision. This means that all healthy loans are accuately categorized. However the model only has a precision of 84% when predicting high risk loans. This means that 16% of predicted high risk loans are actually healthy loans. This is advantageous to the lender, but disadvantageous to the borrower.
