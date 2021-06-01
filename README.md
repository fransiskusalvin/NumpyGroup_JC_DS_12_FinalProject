# NumpyGroup_JC_DS_12_FinalProject

# CREDIT CARD CUSTOMER CLUSTERING OPTIMIZED WITH MACHINE LEARNING

## BACKGROUND
Almost every American, it seems, gets a new credit card offer in the mail almost every week. Credit cards are highly profitable, but only if the customers stays around for a while. It **costs about 80 dollars** to **acquire a new credit card customer** who **returns about 120 dollars per year** in profit, but **only if she keeps the card**. If customers **drops the card after a few weeks, or doesn’t use the card**, the issuer will **lose that 80 dollars, plus some more money spent trying to reactivate her**. It is a tough business.
 
Source: https://www.dbmarketing.com/articles/Art175.htm

## PROCESS WORKFLOWS

![image](https://user-images.githubusercontent.com/78836373/120300137-d9b18d00-c2f5-11eb-9f5c-56fe6224274f.png)

## 1. BUSINESS PROBLEMS
- **Customer loyalty** is one of the **key** to survive in this credit card business competition
    - Source: https://www.dbmarketing.com/articles/Art175.htm
- The **cost of acquiring new customers** is estimated at **five times** the rate of **retaining existing ones**
    - Source : https://www.fpsc.com/the_cost_of_customer_churn.pdf
- In order to retain customers, we must first understanding our customers type and customer behaviour
- Previously, our bank only has 1 product of credit card, resulting low customer loyalty because inaccurate marketing program
- After do long research, our management decides to make 3 different products: **Business Unlimited (High), Business Cash (Medium), and Performance Business (Low)**
- In other hand, the company doesn't know which customers belongs to which products

## 2. GOALS SETTINGS
- Understanding Customers Type and Customer Behaviour through Customer Data Clustering
- Define product details based on clustering results to ensure that customers get the proper product
- Help Marketing Team to define new Customers type through Machine Learning Modelling 

## 3. DATA EXTRACTION, DATA LOAD, AND DATA UNDERSTANDING

- Our data set is taken from Kaggle: https://www.kaggle.com/arjunbhasin2013/ccdata
- Below is the small part of our dataset which consist of 18 Features and 8950 data
CUST_ID | BALANCE | BALANCE_FREQUENCY | PURCHASES | ONEOFF_PURCHASES | INSTALLMENTS_PURCHASES | CASH_ADVANCE | PURCHASES_FREQUENCY | ONEOFF_PURCHASES_FREQUENCY | PURCHASES_INSTALLMENTS_FREQUENCY | CASH_ADVANCE_FREQUENCY | CASH_ADVANCE_TRX | PURCHASES_TRX | CREDIT_LIMIT | PAYMENTS | MINIMUM_PAYMENTS | PRC_FULL_PAYMENT | TENURE
-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----
C10001 | 40.900749 | 0.818182 | 95.4 | 0 | 95.4 | 0 | 0.166667 | 0 | 0.083333 | 0 | 0 | 2 | 1000 | 201.802084 | 139.509787 | 0 | 12



Joni | 20 | Bandung
Desi | 23 | Jakarta
Doni | 24 | Depok


COLUMNS DESCRIPTION

- `CUST_ID` - Identification of Credit Card Holder
- `BALANCE` - Balance amount left in their account to make purchases
- `BALANCE_FREQUENCY` - How frequently the Balance is updated, score between 0 and 1 (1 = frequently updated, 0 = not frequently updated)
- `PURCHASES` - Amount of purchases made from account 
- `ONEOFF_PURCHASES` - Maximum purchase amount done in one-go
- `INSTALLMENTS_PURCHASES` - Amount of purchase done in installment
- `CASH_ADVANCE` - Amount of Cash Money user take from credit card
- `PURCHASES_FREQUENCY` - How frequent the Purchases are being made, score between 0 and 1 (1 = frequently purchased, 0 = not frequently purchased)
- `ONEOFF_PURCHASES_FREQUENCY` - How frequent Purchases are happening in one-go (1 = frequently purchased, 0 = not frequently purchased)
- `PURCHASES_INSTALLMENTS_FREQUENCY` - How frequent purchases in installments are being done (1 = frequently done, 0 = not frequently done)
- `CASH_ADVANCE_FREQUENCY` - How frequent user take money from credit card
- `CASH_ADVANCE_TRX` - Number of Transactions made with "Cash in Advanced" 
- `PURCHASES_TRX ` - Number of purchase transactions made 
- `CREDIT_LIMIT` - Limit of Credit Card for user
- `PAYMENTS` - Amount of Payment done by user
- `MINIMUM_PAYMENTS` - Minimum amount of payments made by user
- `PRC_FULL_PAYMENT` - Percent of full payment paid by user
- `TENURE` - Tenure of credit card service for user


