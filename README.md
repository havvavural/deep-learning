# LSTM Stock Predictor

![deep-learning.jpg](Images/deep-learning.jpg)

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG)](https://alternative.me/crypto/fear-and-greed-index/) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. I have been asked to help build and evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

I will use deep learning recurrent neural networks to model bitcoin closing prices. One model will use the FNG indicators to predict the closing price while the second model will use a window of closing prices to predict the nth closing price.


- - -


### Prepare the data for training and testing

For the Fear and Greed model, I used the FNG values to try and predict the closing price.

For the closing price model, I used previous closing prices to try and predict the next closing price.

Each model will use 70% of the data for training and 30% of the data for testing.

I applied MinMaxScaler to the X and y values to scale the data for the model.

Finally, I reshaped the X_train and X_test the values to fit the model's requirement of samples, time steps, and features. (*example:* `X_train = X_train.reshape((X_train.shape[0], X_train.shape[1], 1))`)


### Evaluate the performance of each model

Finally, I used the testing data to evaluate each model and compare the performance.


- - -
