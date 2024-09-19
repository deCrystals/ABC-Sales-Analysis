# Sales Analysis
![Sales](./image/Dashboard.png)

## Table of Contents
* [Introduction](#Introduction)
* [Data Source](#DataSource)
* [Exploratory Data Analysis](#EDA)
* [Methodology](#Methodology)
* [Models](#Introduction)
    + [Linear Regression](#LinearRegression)
    + [Decision Tree Regressor](#decisionTreeregressor)
    + [Random Forest Regressor](#RandomForestRegressor)
* [Result](#Result)
* [Concluison](#conclusion)

## Introduction
 This project is aimed at performing Monthly Sales Analysis for a company with stores in 3 cities. The dataset, sourced from Kaggle, contains various features related to customer purchases and other sales-related factors. The project's primary objective is to predict the purchase amount based on these features.

## Data Source
The data for this analysis was obtained from Kaggle, a platform that provides open datasets. The dataset includes customer demographics, product categories, and purchase amounts.
* Dataset Name: Kaggle Sales Data
* Features: Various features such as customer age, gender, product categories, and more.
* Target: Purchase Amount


## Exploratory Data Analysis (EDA)
Extensive Exploratory Data Analysis (EDA) was performed to understand the data distribution, detect outliers, and find correlations between features and the target variable. [EDA code](ABC_salesAnalysis.ipynb)
#### Key steps in EDA:
+ Data cleaning (handling missing values, correcting data types).
+ Univariate and bivariate analysis of features.
+ Visualization of key insights using libraries like Matplotlib and Seaborn.
+ Checking for feature correlations and multicollinearity.

## Methodology
The project follows a typical machine learning pipeline, including:
1.	**Data Preprocessing:** Cleaned and transformed the dataset for model training.
2.	**Feature Engineering:** Created additional features to improve model performance.
3.	**Model Training:** Implemented multiple regression models to predict the purchase amount.
4.	**Model Evaluation:** Evaluated models based on RMSE (Root Mean Squared Error), R² score, and MAE (Mean Absolute Error).


## Models
Five models were implemented to predict the purchase amount. [Model code](model.ipynb)
#### Linear Regression
A simple regression model that assumes a linear relationship between input features and the target variable.
+ Key Characteristics: Easy to interpret but may underperform if the relationship between features and target is not linear.

#### Decision Tree Regressor
A decision tree is a non-linear model that splits data based on feature values to make predictions.
+ Key Characteristics: Handles non-linearity well and can overfit on small datasets.

#### Random Forest Regressor
An ensemble learning method combines several decision tree predictions to improve accuracy and generalisation.
+ Key Characteristics: More robust and less prone to overfitting than a single decision tree.

#### XGBOOST Regressor
XGBoost(Extreme Gradient Boosting) uses level-wise tree growth. it uses pruning to control tree complexity, cutting off splits that do not improve loss function.
+ Key Characteristic: It is computational efficient and scalanle. It is more robust with smaller datasets and prevents overfitting

#### LightGBM Regressor
LightGBM(Light Gradient Boosting Machine) grows trees leaf by leaf. It reduces loss efficiently but prone to overfitting with smaller dataset. 
+ Key Characteristics: It is faster and requires less memory

#### Results
The performance of the models was evaluated using the following metrics:
+ Root Mean Squared Error (RMSE)
+ R² score
+ Mean Absolute Error (MAE)



### Conclusion
**Best Model:** XGBoost slightly outperforms all models in terms of R² and error metrics, making it the best model in this case for the sales analysis task.
LightGBM offers a close alternative to XGBoost with similar performance.
Random Forest is also competitive but performs a bit worse than the gradient boosting models.
Linear Regression performs poorly, while Decision Tree performs moderately but lacks the generalization power of ensemble models.






