# Sparkify

User churn prediction for a hypothetical music Sparkify using PySpark

This project is towards my Udacity Datascience nanodegree's cap stone project.

## Project motivation and background

This project aims to understand user churn for a hypothetical music streaming service called Sparkify. 

Sparkify offers two levels of service - free tier and paid tier. Users in the free tier can listen to songs for free but will have ads played between them. Users in the paid tier pay a subscription fee and can listen to songs ad-free.

At any point paid user can downgrade their service level to the free tier. Or users either paid or free tier can cancel their account and leave the service. The latter is particularly concerning since it decreases Sparkify's user base and leads to loss in revenue.

The objective of this project is to identify those users who are more most likely to cancel their account and leave the service. If we could identify these people upfront then Sparkify could incentivize them to stay on the platform by providing discounts or other rewards.

User churn is a general problem that is extremely relevant and common across the B2C industry. The high relevance of the problem combined with the need to use big data technologies like Spark are what motivated me to pick this project over others

## Requirements

I have explored the data and built the model using a Jupyter notebook. Hence you need a Jupyter notebook setup to be able to view the file

The project needs the following libraries:

1. pyspark 2.4.3
2. scikit-learn 0.20.1
3. numpy 1.15.4
4. pandas 0.23.4

## Files description

There are 2 files in the project:

1. README
<br> This readme file

2. Sparkify.ipynb
<br> Jupyter notebook that contains code and explanations for the data exploration and model building parts

## Result

After exploring the data and understanding what features relate to user churn, I built multiple models using different methods to predict users who will churn. I tried 3 different classifiers:

1. Random forest classifier
2. Gradient boosted tree classifier
3. Logistic regression

For each of the above I built a baseline model using the default hyper parameters. I then used 3-fold cross validation to fine tune the hyper parameters

The best model was chosen on the basis of F1 Score that gives equal importance to precision and recall. The model that performed the best was the baseline Gradient boosted tree classifier. It had the following metrics on the validation dataset:

|Metric|Value|
|---|---|
|F1 score| 0.714286 |
|Precision| 0.83333
|Recall|0.625|
|Accuracy| 0.870968|

## Blog post

I have detailed my steps and approach in a [blog post](https://medium.com/@karthikvijayakumar/sparkify-user-churn-prediction-a1bceec38265) as well
