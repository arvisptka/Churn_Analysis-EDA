# Churn Analysis : Exploratory Data Analysis

Here will perform standard stages of data exploration analysis. Things to do :
- Data Cleaning: standard processes include handling missing values ​​and data duplication.
- EDA: Data interpretation includes descriptive statistics, frequency distribution analysis (univariate analysis, bivariate analysis and multivariate analysis).
- Further exploration: includes data aggregation and pivot.

## Data Cleaning

### Handling Missing Value

![image](https://github.com/user-attachments/assets/e38d47a6-5e9c-41c0-a775-10b4d2759fe6)

Total Null from each column is still relatively small and the dataset we have is large. So the practical action is to drop null values ​​from each column.
> Stages for handling null values ​​in a dataset:
> 1. If the null value is still relatively small (15% - 30%) and the number of datasets is large, then drop the null value.
> 2. If the null value is more than 30%, then drop the column if it is not used in the analysis, but if the column is important, then recall the data engineer to determine whether the error is from the input process or something else.
> 3. If the column is important and the data engineer does not know for sure where the error is, then check the null value pattern and understand the behavior of this missing value data.
> 4. Perform imputation. numeric data with mean and categorical data with mode. This is an aggressive action because if this is done for data exploration analysis, it can lead to biased insights.

### Data Duplicate

![image](https://github.com/user-attachments/assets/8d5f2fe0-8cde-4313-a2ee-c8d6e9dcbf85)

The total duplicate data is relatively small and there is duplication in the ID, then drop the duplicate data. 

> Data duplication usually occurs during SQL Join. If data duplication occurs in its Primary Key, then it is true data duplication. However, if duplication occurs other than in the Primary Key then it is not data duplication.

## EDA

### Univariate Analysis

![image](https://github.com/user-attachments/assets/e4319dbb-edf6-4fc7-99d5-7538a5223f43)

Observation : The majority of customers choose a monthly contract with a percentage of 55.13% which is more flexible if at any time they do not use it, they can stop their subscription the following month and a quarter of customers choose a 2-year contract which most likely has discounts or other benefits if they take a longer contract.

![image](https://github.com/user-attachments/assets/4c988580-0e97-4d4f-a0e1-945eeed1447a)


Observation:
-   There are no outliers from each column
-   Tenure at the beginning has a decrease that is not significant enough and at the end many customers even subscribe for up to 70 months
-   MonthlyCharges has a decrease at the beginning but in the middle there is an increase which indicates that many customers make more monthly payments, namely 50-80
-   TotalCharges has a decrease on the graph which is in line with tenure/month subscription, namely the longer the customer subscribes, the higher the total billing.

### Bivariate Analysis

![image](https://github.com/user-attachments/assets/90fdfbb0-da0a-4e6f-9ae7-0250e4ecf4f4)


The distribution of duration per month and churn frequency is no different, where customers who churn have the same frequency distribution, which is smaller than customers who remain or do not churn.

### Multivariate Analysis

![image](https://github.com/user-attachments/assets/b2704692-3936-41a2-b193-d8b98a4f5bb5)


Observation:
-   Churned customers have lower total charges and monthly charges than non-churners
-   Churned customers use month-to-month / 0 contracts compared to annual contracts.

## Deep Dive Analysis
- 10 customers who spend the most and use the service the longest (most loyal customers)
- Payment type and best payment type
- Average customer spend based on gender and contract

