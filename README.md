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
