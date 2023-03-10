Time Series Data and Basic Forecasting Techniques:
Time Series data is any data that is collected at regular time intervals, with changing observations at every
time interval. Processing time series data effectively can help gain meaningful insights into how a quantity
changes with time.
Forecasting a quantity into the future is an essential task, that predicts future values at any particular time.
Forecasts can be made using various techniques like Exponential Smoothing to much more complex techniques
such as Recurrent Neural Networks. Let’s try to process time-series data and forecast values using basic
techniques!

Prerequisites:
• Revise the following concepts
– Components of Time-Series Data
– Single, Double and Triple Exponential Smoothing
– Regression (Refer to worksheets and slides from Unit 2)
– Croston’s Forecasting
– Time-Series Accuracy Metrics

Task:
Let’s imagine it is 2012 and you are in the market to buy an Orange Ultrabook Laptop for college. But this
laptop is rare to find and expensive. You would want to put your Data Analytics skills to use, and predict
the best time to buy your laptop, such that you can get it for the best price! You would also like to predict
when the Orange Ultrabook would be in stock and when it would have high demand.
An electronics store collected sales data for their store weekly, from February 2010 to October 2012, a period
of 143 months. You have gotten your hands on this, and will use it to predict how the prices will change in
the future.
The data for the following tasks can be downloaded from this Github Repository.

Data Dictionary:
Date - Date on which data was collected (end of the week)
Sales - Weekly sales of the store (in $)
Holiday_Flag - Boolean Flag. 0 for normal week and 1 for holiday season
Temperature - Average temperature during the week
Fuel_Price - Average price during the week (in $/gallon)
CPI - Consumer Price Index
Unemployment - Average percentage of Unemployment in the city
Laptop_Demand - Number of Orange Ultrabook laptops sold during the week

Problem 1 (1 Point)
Decompose the Sales column into trend, seasonal and random components. Plot these components as well
(Hint: Look at the decompose function).

Problem 2 (3 Points)
• Perform forecasts using Single, Double and Triple Exponential Smoothing.
• Plot the forecasts of all three forecasts (different colours) against the true values. (Hint: use lines)
• Use only one function needed for all 3 forecasts, only changing parameters to get each of the 3
models (Hint: Think about alternate names)

Problem 3 (2 Points)
• Forecast Sales values by Regression using all other columns. Print summary of regression model.
• Plot the predicted values against original as well. (Hint: Regression model predictions will not be a
Time Series, so need to get both to common index/x-axis)
• (Hint: Will not work unless one column is dropped/transformed before including it in the regression.
Use the lm function to get linear model)
Note: This is Multiple Linear Regression, that is, using all the columns for regression

Problem 4 (2 Points)
Plot the Laptop_Demand column as a time series. Identify the forecasting required for this type of Time-series,
and forecast the values for all 143 weeks (Hint: Look at functions in the forecast package)

Problem 5 (2 Points)
Evaluate the accuracy of all 3 Exponential Smoothing models (from Problem 2) and Regression models
using the MAPE and RMSE metrics. Comment on which is the best Exponential Smoothing method, and
if Regression is better than Exponential Smoothing? Provide a reasoning for why the best model is better
suited for the Sales data (Bonus Point: reasoning for why the 2 other models perform similarly)
