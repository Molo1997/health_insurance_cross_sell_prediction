# health_insurance_cross_sell_prediction

Insurance Cross-Sell Prediction Model

Project Overview
This project leverages machine learning techniques to predict which health insurance customers are likely to be interested in purchasing vehicle insurance. By analyzing customer data including demographics, current insurance status, and vehicle information, the model helps identify potential cross-selling opportunities, allowing insurance companies to focus their marketing efforts more efficiently.

Dataset Description
The dataset contains information about insurance customers with the following features:
Gender, Age, Driving License status
Region Code (anonymized location data)
Previously Insured status (whether they already have vehicle insurance)
Vehicle Age and Damage history
Annual Premium of current insurance
Policy Sales Channel (anonymized sales channel)
Vintage (customer tenure in days)
Response (target variable: 1 if interested in vehicle insurance, 0 if not)

Key Challenge
The primary challenge in this project is dealing with class imbalance, as only 12.26% of customers in the dataset showed interest in vehicle insurance. This imbalance requires special handling techniques to develop a model that performs well for the minority class.
Methodology

Data Preprocessing:
Feature encoding of categorical variables
Train-test split with additional holdout sample for final evaluation
Feature standardization


Model Selection and Evaluation:
Logistic Regression with various class imbalance handling techniques:
Class weighting
Oversampling (SMOTE)
Undersampling


Model evaluation focused on Recall to ensure maximum identification of interested customers
Cross-validation to prevent overfitting


Model Optimization:
Tested various sampling ratios
Applied probability threshold adjustment for final predictions



Results
The best performing model was Logistic Regression with random undersampling (1:1 ratio), which achieved:

High recall (97.65%) for identifying interested customers
AUC score of 0.83, indicating good discriminative ability
Maintained consistent performance between training and test sets

Business Value
This model provides significant business value by:

Allowing targeted marketing campaigns that focus on customers most likely to purchase
Reducing marketing costs by avoiding outreach to uninterested customers
Improving customer experience by reducing unwanted solicitations
Providing probability scores that can be used to prioritize leads

Usage
The model can be integrated into customer relationship management systems to automatically score existing health insurance customers on their propensity to purchase vehicle insurance. The probability scores can help marketing teams prioritize their outreach efforts.
Future Improvements

Potential enhancements include:
Testing more complex models (gradient boosting, neural networks)
Incorporating additional customer data if available
Exploring feature engineering to improve predictive power
Implementing model monitoring to detect performance drift over time
