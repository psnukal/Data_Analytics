AR and MA models:
Auto Regressive and Moving Average are some of the most powerful, yet simple models for time-series
forecasting. They can be used individually or together as ARMA. There are many other variations as well. We
will use these models to forecast time-series in this worksheet.

Task:
Cryptocurrency is all the rage now and it uses the very exciting technology behind blockchain. People even
claim it to be revolutionary. But if you have invested in cryptocurrencies, you know how volatile these
cryptocurrencies really are! People have become billionaires by investing in crypto, and others have lost all
their money on crypto. The most recent instance of this volatility was seen during the Terra Luna crash. Find
more info about that here (https://www.forbes.com/sites/lawrencewintermeyer/2022/05/25/from-hero-tozero-how-terra-was-toppled-in-cryptos-darkest-hour/?sh=5a7e83bf389e) and here
(https://c.ndtvimg.com/2021-02/4lo9ita_elon-musk-dogecoin-meme_625x300_04_February_21.jpg) if you
are interested.
Your task is to effectively forecast the prices of DogeCoin, a crypto that started as a meme but now is a
crypto that people actually invest in. DogeCoin prices however, are affected even by a single tweet by Elon
Musk. The image below tweeted by Elon Musk shot up the prices of DogeCoin by 200%!

Data Dictionary:
Date - Date on which price was recorded
Price - Price of DogeCoin on a particular day

Prolems:
Problem 0 (0.5 point)
Set the index of DataFrame to the Date column to make it a time series

Problem 1 (1.5 point)
Plot the time-series. Analyze the stationarity from the time-series. Provide reasoning for stationarity/nonstationarity based on visual inspection of time-series plot (0.5 point)
Plot the ACF plot of the Time series (upto 50 lags). Analyze the stationarity from ACF plot and provide
reasoning (Hint: look at functions in statsmodels package) (1 Point)

Problem 2 (2 point)
Run Augmented Dickey Fuller Test. Analyze whether the time-series is stationary, based on ADF results
(1 point)
f not stationary, apply appropriate transformations. Run the ADF test again to show stationarity after
transformation (1 Point)

Problem 3 (1 point)
Plot both ACF and PACF plot. From these select optimal parameters for the ARIMA(p,q) model
Hint: Negative values that are significantly outside the Confidence interval are considered significant too.
Hint: p+q = 3

Problem 4 (2 point)
Write a function to forecast values using only AR(p) model (2 Points)
Only use pandas functions and Linear Regression from sklearn . LR documentation (https://scikitlearn.org/stable/modules/generated/sklearn.linear_model.LinearRegression.html)
Hint: Create p new columns in a new DataFrame that is a copy of transformed_df
Each new column has lagged value of Price. Price_t-i (From Price_t-1 upto Price_t-p )
Look at the shift function in pandas to create these new columns Link
(https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.shift.html)
Hint:
Seperate into X_train and y_train for linear regression
We know that AR(p) is linear regression with p lagged values, and we have created p new columns with
the p lagged values
X_train is training input that consists of the columns Price_t-1 upto Price_t-p (p columns in
total)
y_train is the training output (truth values) of the Price, i.e the Price column (Only 1 column)


Problem 5 (1 Point)
Phew! Just handling AR(2) manually required us to difference, apply regression, undifference. Let's make all
of this much easier with a simple library function
Use the ARIMA function using parameters picked to forecast values (1 point)
Hint: Look at ARIMA function the statstmodels . Pass the p,d,q inferred from the previous tasks
We DO NOT need to pass the transformed_df to the ARIMA function.
Pass the orirginal df as input to ARIMA function, with the d value inferred when Transforming the df to
make it stationary
The ARIMA function automatically performs the differencing based on the d value passed
Store the .fit() results in an object named res.

Problem 6 (1 point)
Evaluate the ARIMA model using Ljung Box test. Based on p-value infer if the Model shows lack of fit
Hint: Pass the res.resid (Residuals of the ARIMA model) as input the Ljung-Box Text.
Pass lags=[10] . Set return_df=True For inference, refer back to the Null and Alternate Hypotheses
of Ljung-Box test. (If p value high, Null Hypothesis is significant)
