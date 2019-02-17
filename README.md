# Crypto_ML
To develop a machine learning model to forecast future prices of Cryptocurrencies
____________________________________________________________________________________

## Data
Using the Quandl and Poloniex Exchange API to pull a few of the largest cryptocurrencies by marketcap as well as the SP500 index for reference with aim to create visualizatons and get a feel for the data.

A look at Closing Price dating back to 2015
![alt text](images/Crypto_Close_Subplot.png)

Candlestick Chart with moving average and Bollinger Bands
![alt text](images/Candlestick_BTC.png)

Overlapping comparison of trend in closing price
![alt text](images/Crypto_Log_Prices.png)

Correlation between asset closing price
![alt text](images/Heatmap_Correlation.png)

## Linear Regression
The first attempt at predicting future price was with a linear regression model taking just the historic closing price data as the input. Using Ethereum as the asset of choice, again plot and add some new features to use in future predictions

![alt text](images/Eth_Close.png)

![alt text](images/Eth_HL_Perc.png)

![alt text](images/Eth_OC_Perc.png)

Using the SciKitLearn Library to train the model and create a forecast out of 5 days, with a Linear Accuracy of 0.812

![alt text](images/Ethereum_Forecast.png)

![alt text](images/Ethereum_Forecast_zoom.png)

Price for last 5 days

|date      |     price |
|----------|----------:|
|2019-02-13| 122.042960|
|2019-02-14| 120.350000|
|2019-02-15| 121.424776|
|2019-02-16| 122.843760|
|2019-02-17| 129.395100|

Price for next 5 days

|date      |     price |
|----------|----------:|
|2019-02-17| 119.234912|
|2019-02-18| 118.977214|
|2019-02-19| 113.845250|
|2019-02-20| 117.969306|
|2019-02-21| 110.417734|


## LSTM
The final attempt at forecasting prices used a Long short-term memory(LTSM) neural network with SciKitLearn to normalize and process the data and the Keras library to develop the model


![alt text](images/LTSM.png)

Ethereum price for tomorrow:  [[117.84889]]
