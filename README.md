# Short-Term Bitcoin Price Prediction Using LSTM Networks

![Bitcoin Image](bitcoin.jpeg)

## Problem Statement
The cryptocurrency market, particularly Bitcoin, is characterized by extreme volatility and rapid price changes. Accurately predicting short-term price movements of Bitcoin can provide substantial advantages for traders and investors, enabling more informed decision-making and potential profit maximization. However, the inherent volatility and the influence of various external factors make this prediction task highly challenging. This project aims to address this challenge by developing a model using Long Short-Term Memory (LSTM) networks, a type of Recurrent Neural Network (RNN), to predict short-term price movements of Bitcoin using historical price data obtained from Yahoo Finance.

## Objective
The objective of this project is to leverage LSTM networks to predict short-term price movements of Bitcoin based on historical data from Yahoo Finance.

## Project Structure
- **data**: Contains the historical Bitcoin price data.
- **notebooks**: Jupyter notebooks used for data exploration, model training, and evaluation.
- **models**: Saved models and weights.
- **images**: Contains images used in the README and notebooks.

## Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- yfinance
- pandas_ta
- scikit-learn
- tensorflow

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/bitcoin-price-prediction.git
    cd bitcoin-price-prediction
    ```
2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Download the historical Bitcoin price data using Yahoo Finance API:
    ```python
    import yfinance as yf
    data = yf.download("BTC-USD", start="2010-01-01", end="2023-01-01")
    data.to_csv("data/bitcoin_price.csv")
    ```
2. Preprocess the data and train the LSTM model:
    ```python
    from yourmodule import preprocess_data, train_model
    data = preprocess_data("data/bitcoin_price.csv")
    model = train_model(data)
    model.save("models/bitcoin_lstm_model.h5")
    ```
3. Predict Bitcoin prices:
    ```python
    from yourmodule import predict_price
    predictions = predict_price(model, data)
    ```

## Results
The LSTM model's performance is evaluated using Mean Squared Error (MSE). The model's predictions are compared against actual Bitcoin prices to visualize its accuracy.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any changes.
