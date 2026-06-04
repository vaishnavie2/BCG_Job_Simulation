# Customer Churn Prediction for PowerCo

## Project Overview

This project focuses on analyzing customer and pricing data to identify key factors influencing customer churn and building a predictive model to identify customers at risk of leaving.

The project follows a complete data science workflow including:

- Exploratory Data Analysis (EDA)
- Feature Engineering
- Model Building
- Model Evaluation

The objective was to understand customer churn behavior, identify important churn drivers, and help the business take proactive retention actions.

---

# Client and Business Problem

PowerCo is an energy supply company that provides electricity and gas services to business customers.

The company has been experiencing customer churn, where customers stop using their services and switch to competitors.

Customer churn creates several business challenges:

- Loss of recurring revenue
- Increased customer acquisition costs
- Reduced customer lifetime value
- Lower profitability

PowerCo was particularly interested in understanding whether electricity price changes influence customer churn.

The company wanted to identify customers at risk of leaving before they churn so that retention actions such as discounts, pricing adjustments, or customer engagement initiatives could be implemented.

---

# Business Objective

- Identify key factors influencing customer churn
- Understand customer behavior patterns
- Create meaningful features from raw customer and pricing data
- Build a predictive model to identify customers at risk of churn
- Support proactive customer retention strategies

---

# Dataset Description

## Client Dataset

- Customer consumption data
- Contract dates
- Customer profitability and margins
- Customer acquisition information
- Customer segment information
- Churn status (Target Variable)

## Price Dataset

- Off-peak prices
- Peak prices
- Price variations over time

Used to create price sensitivity and price change features.

---

# Project Workflow

## 1. Exploratory Data Analysis (EDA)

### Key Findings

- Dataset showed class imbalance
- Lower energy consumption customers showed higher churn tendency
- Lower profit margin customers were more likely to churn
- Sales channel showed different churn patterns
- Customer behavior and profitability appeared to be important churn drivers

---

## 2. Feature Engineering

### Customer Lifecycle Features

- months_activ
- months_to_end
- months_modif_prod
- months_renewal

### Price Sensitivity Feature

- offpeak_price_change_dec_jan

### Data Transformation

- Converted has_gas to binary format
- One-hot encoded categorical variables
- Removed original date columns

---

## 3. Model Building

Random Forest Classifier

Parameters:

- n_estimators = 300
- max_depth = 10
- class_weight = balanced
- random_state = 42

---

## 4. Model Evaluation

| Metric | Value |
|----------|----------|
| ROC-AUC | 0.65 |
| Accuracy | 0.48 |
| Churn Recall | 0.71 |

### Threshold Tuning

Classification threshold reduced from 0.50 to 0.30 to improve churn recall.

---

# Feature Importance

Important feature groups:

- Margin-related features
- Consumption-related features
- Customer lifecycle features
- Price variation features

Key variables:

- margin_net_pow_ele
- margin_gross_pow_ele
- cons_12m
- cons_last_month
- months_activ
- off_peak_peak_var_mean_diff

---

# Business Impact

- Identify high-risk customers
- Improve retention efforts
- Support targeted retention campaigns
- Increase revenue stability

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# Project Structure

```text
├── eda.ipynb
├── feature_engineering.ipynb
├── model.ipynb
├── README.md
```

---

# Conclusion

This project demonstrates a complete end-to-end churn prediction pipeline using EDA, feature engineering, machine learning, and threshold tuning to identify at-risk customers and support retention strategies.
