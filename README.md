# Deep Learning Bitcoin Price

Due to the volatility of cryptocurrency speculation, investors will often try to incorporate sentiment from social media and news articles to help guide their trading strategies. One such indicator is the [Crypto Fear and Greed Index (FNG) which attempts to use a variety of data sources to produce a daily FNG value for cryptocurrency. With this in mind, this project was built to evaluate deep learning models using both the FNG values and simple closing prices to determine if the FNG indicator provides a better signal for cryptocurrencies than the normal closing price data.

This project used deep learning recurrent neural networks to model Bitcoin closing prices. One model used the FNG indicators to predict the closing price while the second model used a window of closing prices to predict the nth closing price.

The following is a list of the steps undertaken:

1. Prepare the data for training and testing
2. Build and train custom LSTM RNNs
3. Evaluate the performance of each model

- - -

### Prepare the data for training and testing

For the Fear and Greed model, the project used the FNG values to predict the closing price.

For the closing price model, it used previous closing prices to predict the next closing price.

Each model used 70% of the data for training and 30% of the data for testing.

Applied a MinMaxScaler to the X and y values to scale the data for the model.

Finally, reshaped the X_train and X_test values to fit the model's requirement of (samples, time steps, features).

### Build and train custom LSTM RNNs

In each Jupyter notebook, created the same custom LSTM RNN architecture. In one notebook, the project fit the data using the FNG values. In the second notebook, it fit the data using only closing prices.

It also use the same parameters and training steps for each model. This was necessary to compare each model accurately.

### Evaluate the performance of each model

Finally, used the testing data to evaluate each model and compare the performance.

Then used the data to answer the following:

> Which model has a lower loss?
>
> Which model tracks the actual values better over time?
>
> Which window size works best for the model?

## Built With

* [Python](https://www.python.org/) - Programming language.
* [Pandas](https://pandas.pydata.org/) - Data analysis and manipulation tool.

## Authors

* **Roberto Cantu**  - [GitHub](https://github.com/RCantu92)