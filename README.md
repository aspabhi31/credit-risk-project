# Credit Card Default Risk Modeling

## Business Problem
Credit card issuers must decide which applicants to approve while minimizing credit losses.
This project builds a predictive model to estimate the Probability of Default (PD) and
supports approval decisions using risk-based strategies.

## Dataset
Public credit default dataset containing demographic, behavioral, and credit history features.

## Objective
- Predict Probability of Default (PD)
- Evaluate model performance using risk-appropriate metrics
- Demonstrate how model outputs support approval decisions

## Feature Understanding
Features were categorized into behavioral (payment history, utilization, credit activity)
and demographic (age, income, debt ratio). Behavioral features are expected to be more
predictive of default risk, consistent with industry risk modeling practices.

## Risk Insights (EDA)

- Default rates increase sharply with higher credit utilization, indicating strong monotonic risk behavior.
- Customers with any history of 90+ day delinquency show significantly higher default rates.
- Behavioral variables provide clearer risk separation than demographic variables.
- Several features contain extreme or missing values, which will require careful treatment before modeling.

## Feature Engineering Summary

- Created missing income indicator to capture data quality risk.
- Capped extreme utilization and debt ratio values to improve model stability.
- Engineered TotalDelinquencyCount to summarize repayment behavior.
- Added HighUtilizationFlag as a risk threshold indicator.

## Approach
1. Risk-focused EDA to understand default behavior
2. Data cleaning and risk-driven feature engineering
3. Logistic regression PD model with class imbalance handling
4. Model evaluation using ROC-AUC and KS statistic
5. Cutoff-based approval strategy
6. Business impact simulation (loss reduction)

## Key Results
- ROC-AUC: ~0.7+
- KS Statistic: ~0.3+
- Clear separation of risk bands
- Significant reduction in expected loss vs baseline

## Business Impact
The model demonstrates how data-driven decisioning can reduce credit losses while maintaining healthy approval rates.

## Tools
Python, Pandas, NumPy, Scikit-learn, Matplotlib
