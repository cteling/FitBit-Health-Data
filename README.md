# FitBit-Health-Data
 
This project involves applying data science techniques to the analysis of health and fitness levels. 
I found online at <a href="https://www.openhumans.org">openhumans.org</a> a publicly accessible archive where users can post data collected by their Fitbit,
which is a commerically available fitness monitor. The data contains information about weight, body fat, activity level, calories burned, and even sleep. It is in
the form of time series. The goal of this project is to make predictions about weight and also to model how potential changes
in calories burned and/or activity level affect weight. These types of models should be of interest to many users. 

We perform an detailed analysis of the weight time series on its own and then study how other time series affect the 
subject's weight. In general we found that fairly simple moving average models of the (first differenced) weight can be good predictors. We also considered
an alternative approach were we transform the time series into a set of feature and target variables. The problem is now amenable to supervised learning and 
we use a Random Forest model to make predictions. Given a reasonable set of training data from the user these models can be used to make forecasts. For example,
suppose we have weight data for the past 30 days for a user who wishes to start a fitness program or diet. The predictions made by the model could serve as
a baseline reference point to measure the effect of the program or diet on weight over time. 

Finally, we propose linear regression models relating weight to the time series of features constructed from calories burned and/or activity. Here the analysis is complicated
because residuals are not normal, identical and independently distributed random variables, instead they have their own time series structure. 
A limitation of the present analysis is that the data did not include information about calories taken in due to food consumption. With this data included
I believe it would be possible to build even stronger models. 
