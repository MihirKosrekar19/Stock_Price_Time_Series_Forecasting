Stock Price Prediction using LSTM Neural Network

Objective:
The project aims to predict the future adjusted closing prices of a stock using Long Short-Term Memory (LSTM) neural networks.

Workflow:
1. Data Collection: 
   - The historical adjusted closing prices of a stock are collected from Yahoo Finance using the `yfinance` library.
   - The data is stored in a CSV file for future reference.

2. Data Preprocessing:
   - The collected data is loaded into a pandas DataFrame and only the 'Date' and 'Adj Close' columns are retained.
   - The data is scaled using Min-Max scaling to normalize the values between 0 and 1.

3. Model Building:
   - The LSTM neural network model is constructed using TensorFlow Keras.
   - The input sequences and corresponding output values are created for training the model.
   - The data is split into training, validation, and testing sets.

4. Model Training:
   - The model is trained on the training set and validated on the validation set.
   - Different combinations of optimizers and loss functions are experimented with to find the best performing model.
   - The model's performance is evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R-squared (R²) score.

5. Model Evaluation:
   - The trained model is evaluated on the validation set to assess its performance.
   - The evaluation metrics are calculated and printed to analyze the model's accuracy.

6. Future Price Prediction:
   - The trained model is used to predict the future adjusted closing prices of the stock.
   - The prediction horizon is extended by a specified number of time steps.
   - The predicted prices are inverse transformed to get the actual price values.

7. Results Visualization:
   - The historical and predicted prices are plotted on a graph to visualize the model's performance.
   - The graph displays the historical prices along with the predicted prices for the future time steps.

Dependencies:
- pandas for data manipulation
- yfinance for fetching historical stock data
- matplotlib for visualization
- TensorFlow for building and training the LSTM model
- scikit-learn for data preprocessing and evaluation metrics

References:
- [YFinance Documentation](https://pypi.org/project/yfinance/)
- [TensorFlow Keras Documentation](https://www.tensorflow.org/api_docs/python/tf/keras)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
