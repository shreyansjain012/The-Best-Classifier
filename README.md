# The Best Classifier

## Problem Statement
We have been given a historical dataset of Bank Customers applying for loan and we have to predict whether a new customer will be able to pay the loan on time or not. It is a typical classification problem, here we can apply different machine learning models to predict the final outcome and then we have to choose which among these models and algorithms is best for the given problem.

## Dataset Description

Rows, Cols: 364, 10 

| Unnamed:0  | Unnamed:1 | loan_status  | Principal | terms | effective_date | due_date  | age | education            | gender |
| ---------- | --------- | ------------ | --------- | ----- | -------------- | --------  | --- | -------------------- | ------ |
| 0          | 0         | PAIDOFF      | 1000      | 30    | 9/8/2016       | 10/7/2016 | 45  | High school or below | Male   |
| 2          | 2         | PAIDOFF      | 1000      | 30    | 9/8/2016       | 10/7/2016 | 33  | Bachelor             | Female |
| 3          | 3         | PAIDOFF      | 1000      | 15    | 9/8/2016       | 9/22/2016 | 27  | College              | Male   |


As shown above are the 3 rows from the dataframe, the dataset is labelled and target label is **loan_status** which can take either of two values **PAIDOFF** or **COLLECTION**. This data is then pre-processed to apply the machine learning models.
- **effective_date** and **due_date** columns consist of dates, we have converted these to python datetime objects
- **due_date** and **terms** column are correlated so **due_date** column is dropped from **feature_labels**
- **Unnamed:0** and **Unnamed:1** columns are irrelevant, we have excluded them from **feature_labels**
- In **loan_status** column we are denoting **PAIDOFF** as **1** and **COLLECTION** as **0**
- In **gender** column we are denoting **Female** as **1** and **Male** as **0**
- **education** column consists of string which can take any one of these values:
  - Bachelor
  - High School or Below
  - Master or Above
  - College
  
  One hot encoding method is then applied and **Master or Above** is dropped from **feature_labels**
