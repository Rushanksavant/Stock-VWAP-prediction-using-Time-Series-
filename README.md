# Reliance Stock Price Prediction 

## About Dataset

The data was taken from Kaggle, and is the price history and trading volumes of the fifty stocks in the index NIFTY 50 from NSE (National Stock Exchange) India. The dataset is at a day-level with pricing and trading values split across .cvs file for Reliance stock along with a metadata file with some macro-information about the stocks itself. The data spans from 1st January, 2000 to 31st May, 2020.

## Target Variable

VWAP- The volume weighted average price (VWAP) is a trading benchmark used by traders that gives the average price a security has traded at throughout the day, based on both volume and price. It is important because it provides traders with insight into both the trend and value of a security.

## Feature Dealing

The Features- (Open, High, Low, Volume, Turnover, Trades) were selected and their mean, rolling mean and standard deviation were calculated, further each of these were added as new features for prediction to the data.

## Model

The ARIMAX model was trained using the new features generated, followed by the forcast of the time series.

## Errors

Root Mean Square Error of Auto ARIMAX: 35.35717643310448 
Mean Absolute Error of Auto ARIMAX: 23.85492279341704


Till now the model was trained and forcasted results were checked on the test set which was itself part of the main dataset.
But what if I want to predict the future?

## Predicting Features for Future
[ "Open", "High", "Low", "Volume", "Turnover", "Trades"]

Each feature was predicted using the ARIMA time series model. 

Feature Engineering was applied to these predicted features and new features were generated.

## Predicting the Future

The ARIMAX model which was trained earlier was used to forcast VWAP for next month. The newly generated features(mentioned above) were used to make predictions by fitting the ARIMAX model on them. A new dataset of dates (for the next month) was also generated to know the daywise predictions.

## Verify results 
Visit https://www.moneycontrol.com/india/stockpricequote/refineries/relianceindustries/RI to verify the VWAP from the historic graph, for the month of June 2020
