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

## Exploratory Data Analysis
A comprehensive breakdown between churned vs. not churned user base is provided within [EDA Notebook](https://github.com/tpoozhikala/Bank-Churnrate/blob/main/3_EDA/03_EDA_Bank_Churnrate.ipynb) as well as assessing different correlation between the target "Attrition_Flag" column and other features of both 'missing' and 'dropped' datasets.

## Pre-Processing and Training
A description of avoiding the dummy variable trap and generating 70/30 test train splits for the datasets is given within [Preprocess_and_Training Notebook](https://github.com/tpoozhikala/Bank-Churnrate/blob/main/4_Preprocess_and_Training/04_Preprocess_and_Training_Bank_Churnrate.ipynb).

## Modeling
Different models (Logistic Regression, Random Forest, Gradient Boosting, Support Vector Classifier, AdaBoost to improve Random Forest and Gradient Boosting models, and Mulit-Layer Perceptron Neural Network) were tested with the 70/30 train test split and cross validated with GridSearchCV to obtain optimal hyperparameters given a list of parameters for each associated model. The final best performing and easily reproducible model was the Gradient Boosting model with ROC_AUC scores of 0.92 and 0.91 for missing and dropped datasets respectively.
[Modeling Notebook](https://github.com/tpoozhikala/Bank-Churnrate/blob/main/5_Modeling/05_Modeling_Bank_Churnrate.ipynb) for reference.

## Results/Conclusion
Additional efforts can be made along with deploying a hyperparameterized Gradient Boosting model such as having marketing deals towards the higher to likely attrite audience of females or older demographic or efforts can be made to maximize the not churned population or younger married males with children or dependents.
[Final Project Report](https://github.com/tpoozhikala/Bank-Churnrate/blob/main/6_Documentation/Bank_Churn_Rate_Final_Project_Report.pdf) for further documentation and reference.

## Future Work
Future work will be to further fine tune the Gradient Boosting Model in order to reduce its respective training time as well as further optimize the Multi-Layer Perceptron Neural Network Classifier model in order to see if the model with further tuned hyperparameters can outperform the Gradient Boosting model as well as the Optimal Gradient Boosting Model with the AdaBoost Classifier model.










