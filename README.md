# Supervised Machine Learning Homework - Predicting Credit Risk

In this assignment, I built a machine learning model that attempts to predict whether a loan from LendingClub will become high risk or not. 

## Background

LendingClub is a peer-to-peer lending services company that allows individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market. LendingClub offers their previous data through an API.

You will be using this data to create machine learning models to classify the risk level of given loans. Specifically, you will be comparing the Logistic Regression model and Random Forest Classifier.


### Retrieve the data

In the `Generator` folder in `Resources`, there is a [GenerateData.ipynb](/Resources/Generator/GenerateData.ipynb) notebook that will download data from LendingClub and output two CSVs: 

* `2019loans.csv`
* `2020Q1loans.csv`

I brought an entire year's worth of data (2019) to predict the credit risk of loans from the first quarter of the next year (2020).

Note: these two CSVs have been undersampled to give an even number of high risk and low risk loans. In the original dataset, only 2.2% of loans are categorized as high risk. To get a truly accurate model, special techniques need to be used on imbalanced data. Undersampling is one of those techniques. Oversampling and SMOTE (Synthetic Minority Over-sampling Technique) are other techniques that are also used.

## Preprocessing: Convert categorical data to numeric

Create a training set from the 2019 loans using `pd.get_dummies()` to convert the categorical data to numeric columns. Similarly, create a testing set from the 2020 loans, also using `pd.get_dummies()`. 

## Consider the models

I then created and compared two models on this data: a logistic regression, and a random forests classifier. Before I createed, I fit the data, scored the models, and then made a prediction as to which model I thought would perform better. Y

## Fit LogisticRegression model and RandomForestClassifier model

Createed a LogisticRegression model, fit it to the data, and printed the model's score. I then did the same for the RandomForestClassifier. 

## Revisit the Preprocessing: Scale the data

The data going into these models was never scaled, an important step in preprocessing. I used `StandardScaler` to scale the training and testing sets. Before re-fitting the LogisticRegression and RandomForestClassifier models on the scaled data, I made another prediction about how I thought scaling would affect the accuracy of the models. 
 
