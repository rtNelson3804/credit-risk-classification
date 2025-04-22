# Module 12 Report Template

## Overview of the Analysis

The goal of this analysis is to determine whether a loan is likely to remain in good standing or default. Each loan includes details such as loan amount, interest rate, and total debt. Our target variable is the "loan_status" attribute. We began by splitting the dataset into training and testing sets using train_test_split(). Next, we initialized a LogisticRegression model and trained it on the training data. Finally, we used the model to make predictions on the testing data and displayed the results.

## Results

Using bulleted lists, describe the accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
    * Overall accuracy is almost perfect at .99.
    * Accuracy for the Healthy Loans was a perfect 100% with a recall of .99.
    * Accuracy for the High-Risk Loans was .89 with a recall of .94

## Summary

The machine learning model demonstrates strong overall performance with an accuracy of 99%, indicating it correctly classifies the vast majority of loans. The model is especially effective at identifying loans in good standing (class 0), achieving a precision of 1.00 and recall of 0.99.

For loans at risk of default (class 1), the model performs well but with slightly lower metrics: a precision of 0.84 and recall of 0.94, resulting in an F1-score of 0.89. This means the model is good at identifying most risky loans, though it occasionally misclassifies them or includes some false positives.

Recommendation:

I would recommend this model for use by the company, with the following considerations:

    * The high recall for risky loans (0.94) is valuable, as it means the model correctly flags most loans likely to default.

    * The slightly lower precision (0.84) for risky loans suggests some loans may be incorrectly flagged as high risk, which could affect customer relationships if not handled carefully.

    * The near-perfect performance on good loans (class 0) indicates strong reliability in low-risk loan assessment.

Overall, the model is well-suited for supporting loan risk evaluation and could be effectively integrated into the company’s decision-making process, potentially with human review on edge cases.
