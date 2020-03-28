# Default on Credit Card

## Business Problem
This project is to solve the problem of increase in customer default rates, which causes revenue and customer loss for credit card companies. The loss can be limited if credit card companies can pre-qualify customers of low risk and avoid those that are likely to default on payment. In this project, we'll identify the target groups with low and high risk of defaulting on credit card, as well as minimize the loss for credit card companies by minimizing the number of false negatives in our prediction.     

## Exploratory Data Analysis
In this section, we investigated the relationship between customers' demographic variables, payment history, bill amount, payment amount, and their chances of defaulting on payment. The results showed that customers' credit limit, payment history and payment amount seemed to be good predictors. Customers who have low credit limit, make small amount of monthly payment and use revolving credit or delay payment by 1-2 months are the high risk group. When we look at customers' demographic variables, single women with a college degree or higher has the highest chances of defaulting on payment.     

## Model Selection: Logisitc Regression And Random Forest 
This data set is a class imbalance problem because the number of customers who did not default on payment is signigicantly higher than the number of those who did. In this case, accuracy wouldn't be a good matric to evaluate our models. Instead, we focused on type II error(false negatives) because we wanted to minimize the number of customers we predicted to not default but actually did, which would cause great loss for the company. 

Logistic Regression model turned out to have better recall score than Random Forest. After adjusting the threshold to 0.3 of predicted probabilities, recall score increased to 0.9.   

Based on the results of feature importance, payment amount, credit limit and age seem to be the most significant factors in determining the chances of defaulting on payment. Therefore, we used partial dependency plot to investigate the relationship between these three important predictors and the target feature.
- Age: customers have higher chances of defaulting onpayment if they are over 35.
- Credit limit: the lower the credit limit, the more likely the customer will default on payment.
- Payment amount: customers that pay only a small amount of monthly payment are more likely to default on payment.

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
