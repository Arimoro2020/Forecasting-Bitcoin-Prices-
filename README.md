# Forecasting-Bitcoin-Prices-
31 days forecast of Bitcoin prices using auto regression technique


Overview/ Definition of Problem: This is best framed as a Times series problem which forecast 31 days opening prices for Bitcoin cryptocurrency.

Dataset: The original dataset was downloaded from Kaggle, https://www.kaggle.com/mczielinski/bitcoin-historical-data, as a CSV file with bitcoin exchanges for the time period of Jan 2012 to December March 2021, with minute to minute updates of OHLC (Open, High, Low, Close), Volume in BTC and indicated currency, and weighted bitcoin price. Timestamps are in Unix time. Timestamps without any trades or activity have their data fields filled with NaNs.

Data Cleaning & Preparation: Dealt with rows with NAN values by dropping them. Also dropped other colums except Open and Timestamp. Converted time refence from Unix (Timestamp) to DataTime. Data preparation also included normalizing the Open prices using MinMaxScaler & reshaping values to 2D for model_fit and model_predict.

Model Building and Evaluation: The Bitcoin price forecast AutoReg model, a univariate auto-regression model, was built to include constant & time trend, 'ct', and lags 24 to 31. The model was evaluated to have Root Mean Square Error (RMSE) of 3675.61.

Conclusion: The predicted prices trend mostly matches the actual prices trend (see figure: Predicted Bitcoin Price for March 2021 below):


![image](https://user-images.githubusercontent.com/73043768/141615396-834a2bb5-2e0c-4523-85cb-478ebdd323c7.png)


