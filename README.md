
# Customer Churn Prediction — End-to-End Data Science Project

## Project Overview
This project focuses on analyzing customer and pricing data to identify key factors influencing customer churn and building a predictive model to identify customers at risk of leaving.

The project follows a complete data science workflow including Exploratory Data Analysis (EDA), Feature Engineering, Model Building, and Evaluation.

---

## Client and Business Problem

• The client is PowerCo, an energy supply company that provides electricity and gas services to business customers.

• PowerCo has been experiencing customer churn, where customers stop using their services and switch to competitors.

• Customer churn leads to loss of revenue and increases the cost of acquiring new customers.

• PowerCo wants to understand the main factors causing customers to churn.

• The company is especially concerned about how electricity price changes influence customer churn.

• PowerCo wants to identify customers at high risk of churn in advance.

• This will help the company take preventive actions such as offering discounts, better pricing, or improved customer service.

• The goal of this project is to analyze customer and pricing data, identify churn drivers, and build a predictive model to detect at-risk customers.

---

## Business Objective
Customer churn directly impacts business revenue. The objective of this project is to:

- Identify key factors influencing customer churn
- Create meaningful features from raw data
- Build a predictive model to detect churn risk
- Help businesses take proactive retention actions

---

## Dataset Description

### Client Dataset
Contains customer-level information such as:

- Customer consumption
- Contract dates
- Margins and profitability
- Customer segment
- Churn status (Target variable)

### Price Dataset
Contains time-based electricity pricing information including:

- Off-peak prices
- Peak prices
- Price variations over time

This dataset was used to create price sensitivity features.

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

Performed analysis to:

- Understand dataset structure
- Analyze target variable distribution
- Identify missing values
- Separate numerical and categorical features
- Identify important churn drivers

Key findings:

- Customers with lower consumption had higher churn probability
- Customer tenure strongly influenced churn
- Customer segment and sales channel influenced churn behavior

---

### 2. Feature Engineering

Created meaningful features including:

- Tenure feature to represent customer duration
- Customer lifecycle features (months active, months to renewal)
- Price change feature (offpeak_price_change_dec_jan) using price data
- Encoded categorical features into numerical format
- Converted binary features into numeric format

These features improved model ability to learn churn patterns.

---

### 3. Model Building

Used Random Forest Classifier because:

- Handles nonlinear relationships well
- Works well with mixed feature types
- Robust against overfitting

Model parameters:

- n_estimators = 300
- max_depth = 10
- class_weight = balanced

---

### 4. Model Evaluation

Model performance:

- ROC-AUC Score: 0.65
- Accuracy: 0.48
- Churn Recall: 0.71

The model successfully identified 71% of churn customers.

This is important because early detection allows businesses to take preventive action.

---

## Feature Importance

Important features included:

- Customer tenure
- Price change features
- Consumption features
- Margin features

These features played a major role in predicting churn.

---

## Business Impact

This model helps businesses:

- Identify high-risk customers
- Reduce churn
- Improve retention strategies
- Increase revenue stability

---

## Technologies Used

- Python
- Pandas
- NumPy
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Project Structure

```
├── eda.ipynb
├── feature_engineering.ipynb
├── model.ipynb
├── README.md
```

---

## Conclusion

This project demonstrates a complete churn prediction pipeline. Feature engineering and proper model tuning improved churn detection performance significantly.

This model can help businesses proactively identify and retain at-risk customers.

---
