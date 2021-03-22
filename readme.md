# Store Item Demand Forecasting Challenge
# Few Questions
a.	[What is the overall purpose of this project?](#Overall-Purpose)\
b.	[What do each file in your repository do?](#File-Function)\
c.	[What methods did you use to clean the data or do feature engineering?](#Feature-Engineering)\
d.	[What methods did you use to generate predictions?](#Prediction-Method)

## Overall Purpose
This competition is provided as a way to explore different time series techniques on a relatively simple and clean dataset.

You are given 5 years of store-item sales data, and asked to predict 3 months of sales for 50 different items at 10 different stores.

What's the best way to deal with seasonality? Should stores be modeled separately, or can you pool them together? Does deep learning work better than ARIMA? Can either beat xgboost?

This is a great competition to explore different models and improve your skills in forecasting.
Submission is evaluated by SMAPE!

## File Function
There're 2 files in this Repo: store-item-demand-forecasting-challenge1/2/3.ipynb and README file (this file). These ipynb files represent different ideas that I have while trying to predict the future data. 

## Feature Engineering
### Data Fields
* Date: based on each day from 01/01/2013 - 12/31/2017
* Store: Integer that represents different stores
* Item: Integer represents different items

## Prediction Method

XGBoost is the method that I used for submission-1. By using the SMAPE function to valuate the score, the model scores 13.640531729189487 based on X_train and y_train. However, I used basic parameters in the xgboost instead of Hyperparameter Tuning. The final public score is 15.41678.

In submission-2, I think it's better to use different hyperparameters to optimize the model. From the chart I found that different test samples makes it different to train the model. In the mean while, random_state makesit a liitle bit different. From this time, I got a public score of 15.36774. 

In submission-3, I tried another model of ARIMA, which is specifically time series analysis to compare with XGBoost model.
