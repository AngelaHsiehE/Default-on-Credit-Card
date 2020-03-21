# Default on Credit Card

## Business Problem
This project is to solve the problem of increase in customer default rates, which causes revenue and customer loss for credit card companies. The loss can be limited if credit card companies can pre-qualify customers of low risk and avoid those that are likely to default on payment. In this project, we'll identify the target groups with low and high risk of defaulting on credit card, as well as minimize the loss for credit card companies by minimizing the number of false negatives in our prediction.     

## Exploratory Data Analysis
In this section, we'll investigate the relationship between customers' demographic variables, payment history, bill amount, payment amount, and their chances of defaulting on payment. Therefore, we can identify the features that are likely to be good predictors. Finally, we'll use feature engineering techniques to normalize the numerical features. 

## Model Selection: Logisitc Regression And Random Forest 
## Actionable Recommendations
According to our model and the exploratory data analysis, we can identify the customers with high risk of defaulting on payment based on the below attributes:

1. Payment amount
2. Credit limit
3. Payment history
4. Age
5. Education

Payment history, payment amount and credit limit are the most significant factors in predicting defaulting on payment, but we use the demographic attributes to pre-qualify those customers of low risk. We cannot mitigate with 100% certainty any customer possibly defaulting on a payment. However, there are some steps that we can take to reduce the level of risk.

Customers we can approve with high certainty:
- Customers with an approved credit limit of more than 120000 NTD.
- Customers aged between 25-35 and their highest education is high school.

Customers that have high chances of defaulting on payments:
- Customers have delayed payment for more than 1 month.
- Customers whose monthly payment is less than appromately 25000 NTD.
- Customers with a credit limit less than 120000 NTD and aged over 35, chances increase if they have college or graduate degree.

Recommend further analysis:
- Perform analysis on the spending habits of the target groups of high risk. Try to identify trends in spend that coincide with default of payment.
- Analyze other possible contributing factors to those likely to default on a payment; income, outstanding debit (credit, loans etc).
