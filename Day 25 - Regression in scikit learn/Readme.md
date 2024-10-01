
# 📊 Day 25 of 50 Days of Data Science: Regression in Scikit-Learn 🧑‍💻

Welcome to **Day 25** of the **50 Days of Data Science Challenge**! 🎉  
Today, we'll dive into the world of **regression modeling** using the powerful **scikit-learn** library. In this task, we will explore various types of regression models, how to implement them in Python, and evaluate their performance.

---

## 🌟 Objectives
1. **Understand Regression**: Learn about regression analysis and its applications.
2. **Explore Scikit-Learn**: Utilize scikit-learn to implement regression models.
3. **Model Evaluation**: Assess the performance of different regression techniques.
4. **Visualize Results**: Use visualizations to interpret model outcomes.

---

## 📂 Files Included
- **`regression-in-scikit-learn.ipynb`**: The main Jupyter notebook that contains the code for today's task.

---

## 📖 Topics Covered

### 1. 🚀 Introduction to Regression
   - **Definition**: Regression is a statistical approach to estimate the relationships among variables.
   - **Types of Regression**:
     - **Linear Regression** 📈: Simple and multiple linear regression.
     - **Polynomial Regression** 🔄: Adding complexity to fit non-linear data.
     - **Ridge & Lasso Regression** 🔒: Regularization techniques to prevent overfitting.
     - **Decision Tree Regression** 🌳: Non-linear regression using decision trees.

### 2. 📦 Scikit-Learn Overview
   - **scikit-learn** is a widely used machine learning library in Python. It includes tools for:
     - **Data Preprocessing** 🧹
     - **Model Training** 🧠
     - **Model Evaluation** 📊

### 3. 🛠️ Implementing Regression Models
   - **Linear Regression Model**:
     ```python
     from sklearn.linear_model import LinearRegression
     model = LinearRegression()
     model.fit(X_train, y_train)
     ```
   - **Polynomial Features & Regression**:
     ```python
     from sklearn.preprocessing import PolynomialFeatures
     poly = PolynomialFeatures(degree=2)
     X_poly = poly.fit_transform(X)
     ```
   - **Ridge & Lasso Regularization**:
     ```python
     from sklearn.linear_model import Ridge, Lasso
     ridge = Ridge(alpha=1.0)
     lasso = Lasso(alpha=0.1)
     ```
   - **Decision Tree Regression**:
     ```python
     from sklearn.tree import DecisionTreeRegressor
     tree = DecisionTreeRegressor()
     tree.fit(X_train, y_train)
     ```

### 4. 📊 Model Evaluation
   - **Mean Squared Error (MSE)**: Measures the average squared difference between actual and predicted values.
   - **R-Squared (R²)**: Represents the proportion of the variance for a dependent variable that's explained by the independent variables.

   ```python
   from sklearn.metrics import mean_squared_error, r2_score
   mse = mean_squared_error(y_test, y_pred)
   r2 = r2_score(y_test, y_pred)
   ```

### 5. 📈 Visualization of Results
   Use libraries like **Matplotlib** and **Seaborn** to visualize the regression model's performance.
   ```python
   import matplotlib.pyplot as plt
   plt.scatter(X_test, y_test, color="blue")
   plt.plot(X_test, y_pred, color="red")
   plt.show()
   ```

---

## 🏁 Conclusion
By the end of this task, you will have a strong understanding of different regression models, how to implement them in Python, and how to evaluate their performance. You will also know how to interpret the results using visualization techniques.