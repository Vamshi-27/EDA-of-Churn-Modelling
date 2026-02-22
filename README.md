# EDA of Churn Modelling Dataset

## Problem Statement
Customer churn is a critical issue for banks as it directly impacts profitability and long-term growth. This dataset contains customer demographic details, financial information, and account activity data, along with a target variable indicating whether a customer has exited the bank.

The main objectives of this analysis are:
- To understand the overall structure and quality of the dataset
- To identify patterns and trends related to customer churn
- To analyze the relationship between customer attributes and churn behavior
- To determine the key factors that contribute most to customer exit
- To generate insights that can help improve customer retention strategies

## Project Objectives
- Understand the dataset structure and variables
- Perform data wrangling and data cleaning
- Conduct univariate, bivariate, and multivariate analysis
- Identify patterns, trends, and anomalies
- Summarize insights for decision-making
- Provide conclusions and actionable recommendations

## Tools and Libraries
- NumPy
- Pandas
- Matplotlib
- Seaborn

## Dataset Information
**Source:** Kaggle – Bank Customer Churn / Churn Modelling Dataset

### Data Dictionary
| Column Name     | Description                                                            | Data Type   |
| --------------- | ---------------------------------------------------------------------- | ----------- |
| RowNumber       | Unique row identifier for each record                                  | Numerical   |
| CustomerId      | Unique customer identification number                                  | Numerical   |
| Surname         | Customer's last name                                                   | Text        |
| CreditScore     | Customer's credit score                                                | Numerical   |
| Geography       | Country where the customer resides (e.g., France, Germany, Spain)      | Categorical |
| Gender          | Customer's gender                                                      | Categorical |
| Age             | Customer's age                                                         | Numerical   |
| Tenure          | Number of years the customer has been with the bank                    | Numerical   |
| Balance         | Customer's account balance                                             | Numerical   |
| NumOfProducts   | Number of bank products the customer is using                          | Numerical   |
| HasCrCard       | Whether the customer has a credit card (1 = Yes, 0 = No)               | Categorical |
| IsActiveMember  | Whether the customer is an active member (1 = Yes, 0 = No)             | Categorical |
| EstimatedSalary | Estimated annual salary of the customer                                | Numerical   |
| Exited          | Whether the customer left the bank (1 = Yes, 0 = No) — Target Variable | Categorical |

## Methodology

### 1. Data Wrangling
- Dropped irrelevant columns: RowNumber, CustomerId, Surname
- Renamed columns to snake_case format
- Created new features:
  - Age Groups: Young (18-30), Middle_Age (31-45), Senior (46-60), Elder (60+)
  - Tenure Groups: New_Customer (0-3 years), Mid_Term (4-7 years), Long_Term (8-10 years)

### 2. Data Cleaning
- Checked for duplicate rows (none found)
- Checked for missing values (none found)

### 3. Univariate Analysis
Analyzed individual variable distributions:
- Age, Credit Score, Balance, Salary, Tenure
- Geography, Gender, Churn, Active Member status

### 4. Bivariate Analysis
Analyzed relationships between variables:
- Age vs Churn
- Balance vs Churn
- Gender vs Churn
- Geography vs Churn
- Active Member vs Churn
- Credit Score vs Churn

### 5. Multivariate Analysis
- Correlation heatmap
- Pair plots
- Scatter plots with multiple variables

## Key Insights
- Older customers are more likely to churn than younger customers
- Inactive members show significantly higher churn rates compared to active members
- Customers from Germany have a higher churn rate than other regions
- Customers with higher account balances tend to churn more frequently
- Credit score has a moderate influence on churn behavior
- The dataset shows class imbalance (~80% stayed, ~20% exited)

## Conclusion
- Age, activity status, geography, and balance are the key factors influencing churn
- Customer engagement plays a crucial role in retention
- Older and inactive customers form the high-risk churn segment
- There is no strong multicollinearity among variables
- The dataset is suitable for building a churn prediction model

## Recommendations
- Strengthen engagement strategies to reduce churn among inactive customers
- Provide targeted offers and loyalty programs for older customers
- Implement region-specific retention strategies in high-churn areas like Germany
- Offer personalized services to high-balance customers to improve retention
- Develop a predictive churn model to identify and retain at-risk customers early
