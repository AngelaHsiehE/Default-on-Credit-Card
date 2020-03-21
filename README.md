# Default on Credit Card

## Business Problem
This project is to solve the problem of increase in customer default rates, which causes revenue and customer loss for credit card companies. The loss can be limited if credit card companies can pre-qualify customers of low risk and avoid those that are likely to default on payment. In this project, we'll identify the target groups with low and high risk of defaulting on credit card, as well as minimize the loss for credit card companies by minimizing the number of false negatives in our prediction.     

## Exploratory Data Analysis
In this section, we investigated the relationship between customers' demographic variables, payment history, bill amount, payment amount, and their chances of defaulting on payment. The results showed that customers' credit limit, payment history and payment amount seemed to be good predictors. Customers who have low credit limit, make small amount of monthly payment and use revolving credit or delay payment by 1-2 months are the high risk group. When we look at customers' demographic variables, single women with a college degree or higher has the highest chances of defaulting on payment.     

## Model Selection: Logisitc Regression And Random Forest 

After exploring t

## Actionable Recommendations
According to our model and the exploratory data analysis, we can identify the customers of high risk of defaulting on payment with these predictors:

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
