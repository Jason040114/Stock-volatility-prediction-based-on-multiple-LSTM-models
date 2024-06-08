# Stock-volatility-prediction-based-on-multiple-LSTM-models
## Introduction
Stock volatility can reflect the volatility of the price and the future risk of the assets, and historical volatility is an important measure of stock volatility. The scientific and accurate prediction model of stock historical volatility is of great significance for the estimation of the future asset risk situation and the maintenance of the smooth operation of the financial market. Classical time series models have been widely used. <br>In order to obtain more accurate prediction models, this report proposes the stock historical volatility prediction model composed of *`two LSTM neural networks and two fully connected layers`*, so as to improve the ability of the model to effectively capture the complex nonlinear relationship in the time series prediction task.
## Model
### LSTM model of two fully connected layers
The neural network structure we take consists of two fully connected layers and two LSTM layers. In order to accelerate the convergence speed, enhance the model stability, and improve the generalization ability, we add the batch standardization (BN) layer before the LSTM network of each layer. To improve the ability of the model to express non-linear sequences, we added the full connection (Dense) layer before and at the end of the LSTM network. The specific structure of the model is as follows:

![图片1](https://github.com/opdpjfj/Stock-volatility-prediction-based-on-multiple-LSTM-models/assets/125139348/fa903923-8004-4732-8e4a-b1daebfe0a23)
