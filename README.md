# Bank-Churnrate
![Churn-Rate-Reduction](https://github.com/tpoozhikala/Bank-Churnrate/assets/57980120/5f58805b-3772-4305-889e-ea1ba2de1196)

Determining or predicting churn rate is key in increasing business effectiveness and allowing for targeted marketing and resources to increase customer retention. This is especially the case for a bank who released their user data on Kaggle for assistance on predicting churn in order to reduce it. The goal then of this project is to provide a churn prediction model to mitigate the bank’s churn rate and increase overall bank revenue by 20% for the next financial quarter. 

## Data Wrangling
In order to begin steps of model development, the dataset was first assessed and evaluated. It seemed that applying the standard df.isnull() did not seem at first to locate any missing values for the dataset, however upon closer inspection the missing values were actually imputed with the value of ‘Unknown.’ Therefore, replacing all the ‘Unknown’ values with NaN retrieved the below results for the columns that had missing or null values and their respective percent of missingness from the dataset.

|         | count     | %missing  |
| ------- | --- | --- |
| Education_Level | 1205 | 14.874707 |
| Income_Category | 889 | 10.973954 |
| Marital_Status | 579 | 7.147266 |

In order to deal with the ‘missingness’ for the above values, two datasets were created and then assessed throughout the project to assess future model performance. One where the above columns' null data were replaced with the categorical value or string of ‘missing’ and one where any observations in the above three columns that had null values were dropped. These two datasets as reference to subsequent steps are referred to respectively as ‘missing’ dataset and ‘dropped’ dataset respectively.
