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
