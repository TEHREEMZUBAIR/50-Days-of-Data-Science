# 📄 Day 44: Time Series Forecasting with RNNs 🧠

## Task Overview
Welcome to **Day 44** of your data science journey! 🚀 Today’s task dives into **Recurrent Neural Networks (RNNs)**, specifically focusing on their application to **time series forecasting** 📈. RNNs are ideal for sequential data as they retain memory, making them powerful tools for predicting future events in a sequence.

---

## 🛠️ Prerequisites
Before starting, make sure you have the following libraries installed:
1. **Python 3.x** 🐍
2. **Jupyter Notebook** (to run the notebook)
3. **Keras** (for building the RNN model)
   - Install via `pip install keras`
4. **TensorFlow** (as the backend for Keras)
   - Install via `pip install tensorflow`
5. **NumPy** (for numerical computations)
   - Install via `pip install numpy`
6. **Pandas** (for data manipulation)
   - Install via `pip install pandas`
7. **Matplotlib** (for plotting results)
   - Install via `pip install matplotlib`

---

## 📂 File Structure
- `task-44.ipynb` - Main notebook containing the RNN model for time series prediction.
- **Dataset** - A time series dataset (e.g., stock prices, weather data, etc.) for training and testing the RNN model.

---

## 🔄 Instructions

1. **Load the Time Series Dataset** 📊
   Start by loading the dataset, which contains the historical time series data for training the RNN model.
   ```python
   import pandas as pd
   data = pd.read_csv('your_timeseries_data.csv')
   data.head()
   ```

2. **Data Preprocessing** 🧹
   To prepare the data for the RNN, we need to:
   - Normalize the data (to help the model train more effectively).
   - Split the data into **training** and **testing** sets.
   - Reshape the data into 3D arrays suitable for RNNs: `(samples, timesteps, features)`.

   Here’s an example:
   ```python
   from sklearn.preprocessing import MinMaxScaler
   scaler = MinMaxScaler(feature_range=(0, 1))
   scaled_data = scaler.fit_transform(data)

   # Creating a sliding window of input sequences
   X_train, y_train = [], []
   for i in range(60, len(scaled_data)):
       X_train.append(scaled_data[i-60:i])
       y_train.append(scaled_data[i])
   
   # Convert to numpy arrays
   X_train, y_train = np.array(X_train), np.array(y_train)

   # Reshape for RNN
   X_train = np.reshape(X_train, (X_train.shape[0], X_train.shape[1], 1))
   ```

3. **Build the RNN Model** 🧠
   Using the **Keras Sequential API**, you’ll create an RNN model that processes sequential data. Here's an example:
   ```python
   from keras.models import Sequential
   from keras.layers import Dense, SimpleRNN

   # Initialize RNN
   model = Sequential()

   # Add a SimpleRNN layer
   model.add(SimpleRNN(units=50, return_sequences=True, input_shape=(X_train.shape[1], 1)))

   # Add output layer
   model.add(Dense(units=1))

   # Compile the model
   model.compile(optimizer='adam', loss='mean_squared_error')
   ```

4. **Train the Model** 🏋️‍♂️
   Train the RNN using the training data.
   ```python
   model.fit(X_train, y_train, epochs=100, batch_size=32)
   ```

5. **Make Predictions** 🔮
   Use the trained RNN model to predict the future values and compare them with the actual data.
   ```python
   predicted = model.predict(X_test)
   predicted = scaler.inverse_transform(predicted)  # Inverse scaling to original values
   ```

6. **Evaluate the Model** 📉
   Evaluate the performance of the model using **Root Mean Squared Error (RMSE)**:
   ```python
   from sklearn.metrics import mean_squared_error
   import numpy as np

   rmse = np.sqrt(mean_squared_error(test_data, predicted))
   print(f"Root Mean Squared Error: {rmse}")
   ```

---

## 🎯 Task Objectives
- Learn how to preprocess time series data for RNNs.
- Build and train an RNN model using Keras.
- Predict future values in a sequence and evaluate the model’s performance using RMSE.

---

## 🧪 Additional Experiments
- Try adding **LSTM layers** (Long Short-Term Memory) instead of SimpleRNN to improve long-term memory retention.
- Experiment with different numbers of **timesteps** and **units** in the RNN layers to improve the model’s performance.

---

## 💡 Tips
- **Preprocessing** is crucial for time series. Normalize the data and carefully create sequences for training the model.
- **RMSE** is a good metric for evaluating time series predictions, but feel free to explore others like **Mean Absolute Error (MAE)**.

---

## 📚 Resources
- [Keras Documentation](https://keras.io/)
- [TensorFlow Documentation](https://www.tensorflow.org/)

---

Happy coding! 💻✨

---