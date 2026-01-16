# <u>**CREDIT SCORE MODELLING USING MOMO TRANSACTIONS** </u>

## <u> **Project Description**</u>

Credit score Modelling is a vast project of financial inclusion that aims at taking traditional measurement of creditworthiness and add Mobile money transactions as a new measurement variable.

Credit scoring usually consider the applicant's payment history, bank transactions, Age, number of accounts, Loan size, down payment and many more which are mostly affiliated to bank.

This method of scoring credit have been excluding most people from accessing credits from banks due to many reasons like being unbanked, or being first-time credit applicant.

We will first build credit scorecard model to predict using traditional variables and then add alternative variables.

Thus This project aims at considering alternative variables like Mobile money transactions in determining one's possibilities of default.

## <u> Project Objectives</u>
This project's purposes are:<br>
        - To collect data related to credits, mobile money transactions and accounts.<br>
        - To clean them and prepare them for the model training.<br>
        - To build credit scoring model and validate it.<br>
        - To develop a system that measure the creditworthiness of the applicant.

## <u>Data collection</u>
Due to scarcity of data we faced in the beginning of the project, we thought of developing simulations using external data sources or other lending data from internet.

We then took a lending club dataset, a dataset from kaggle that have lending records of United States of America. It has over 2.2 millions records and 151 attributes.

## <u> Data Preparation</u>
We are trying to predict if a client seeked a loan will default or not. A column called loan_status in lending club dataset contains each loan status. Mainly it has 9 unique values includes Fully Paid,Current, Charged Off, In Grace Period, Late (31-120 days), Late (16-30 days), Default, Does not meet the credit policy. Status:Fully Paid, Does not meet the credit policy. Status:Charged Off and null values.

Since We are predicting default of not, we split the column into two parts namely matured loans and continous loans. Of 2.2 million loans, 1.3M found to be matured and over 900K in progress. 

We continued with matured loans with statuses of "Fully Paid", "Charged Off", "Default", "Does not meet the credit policy. Status:Fully Paid", "Does not meet the credit policy. Status:Charged Off". 

After founding that our dataset has columns with over 300k null values or columns without any values, we went on getting such columns. We explored each columns and split columns into five categories: severe(>50% missing), High (20-50% missing), Medium (5-20% missing), Low (0-5% missing), and No missing values.

We immediately dropped columns in severe category, found none in High, 26 columns found in medium, 29 columns found low, and 38 columns in no missing values. We then dropped 24 columns in medium and tolerated those in low category.

