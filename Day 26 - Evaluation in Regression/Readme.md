
# 📊 Day 26 of 50 Days of Data Science: Evaluation in Regression Models 📈💻

Welcome to **Day 26** of the **50 Days of Data Science Challenge**! 🎉  
Today's task focuses on the crucial aspect of **evaluation in regression models**. After building your regression models, evaluating their performance is key to understanding how well they generalize to unseen data. Let's dive into the different techniques for assessing regression models!

---

## 🎯 Objectives
- **Understand Evaluation Metrics**: Learn about the most common metrics for evaluating regression models.
- **Implement in Python**: Utilize scikit-learn to compute these metrics.
- **Compare Models**: Compare the performance of various regression models using these evaluation techniques.

---

## 📂 Files Included
- **`evaluation-in-regression.ipynb`**: The notebook for this task, which contains code for evaluating regression models.

---

## 📖 Topics Covered

### 1. 🌟 Importance of Model Evaluation
   - Model evaluation is essential to:
     - Ensure the model's predictions are accurate and reliable.
     - Avoid overfitting or underfitting.
     - Compare different models to choose the best one.

### 2. 📐 Evaluation Metrics for Regression
   Here are the most commonly used metrics for evaluating regression models:

   - **Mean Absolute Error (MAE)** 🧮:
     - The average of absolute differences between predicted and actual values.
     - Formula: 
       \[
       MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i|
       \]

   - **Mean Squared Error (MSE)** 🔢:
     - The average of squared differences between predicted and actual values.
     - Formula: 
       \[
       MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2
       \]

   - **Root Mean Squared Error (RMSE)** 🔍:
     - The square root of MSE, providing error in the same units as the target variable.
     - Formula: 
       \[
       RMSE = \sqrt{MSE}
       \]

   - **R-Squared (R²)** 📊:
     - Measures the proportion of variance in the target variable explained by the model.
     - Formula: 
       \[
       R^2 = 1 - \frac{\sum (y_i - \hat{y}_i)^2}{\sum (y_i - \bar{y})^2}
       \]
     - Ranges from 0 to 1, where 1 indicates perfect predictions.

   - **Adjusted R-Squared** 📉:
     - Adjusts R² for the number of predictors in the model, useful when comparing models with different numbers of features.
     - Formula: 
       \[
       \text{Adjusted } R^2 = 1 - \left( \frac{(1 - R^2)(n - 1)}{n - p - 1} \right)
       \]

### 3. 💻 Implementing Metrics in Python
   Using **scikit-learn**, you can easily compute these metrics for your models:

   - **Mean Absolute Error (MAE)**:
     ```python
     from sklearn.metrics import mean_absolute_error
     mae = mean_absolute_error(y_true, y_pred)
     ```

   - **Mean Squared Error (MSE)**:
     ```python
     from sklearn.metrics import mean_squared_error
     mse = mean_squared_error(y_true, y_pred)
     ```

   - **Root Mean Squared Error (RMSE)**:
     ```python
     rmse = mean_squared_error(y_true, y_pred, squared=False)
     ```

   - **R-Squared (R²)**:
     ```python
     from sklearn.metrics import r2_score
     r2 = r2_score(y_true, y_pred)
     ```

   - **Adjusted R-Squared**:
     This is not directly available in scikit-learn, but you can compute it manually:
     ```python
     def adjusted_r2(r2, n, p):
         return 1 - (1 - r2) * (n - 1) / (n - p - 1)
     ```

### 4. 📊 Visualizing Model Performance
   Visualizing the differences between predicted and actual values can be very insightful. You can plot the residuals or use scatter plots for a better understanding of model performance.

   - **Residual Plot**:
     ```python
     import matplotlib.pyplot as plt
     plt.scatter(y_pred, y_true - y_pred)
     plt.title("Residual Plot")
     plt.show()
     ```

   - **Actual vs Predicted**:
     ```python
     plt.scatter(y_true, y_pred)
     plt.title("Actual vs Predicted")
     plt.show()
     ```
