
#  Day 27 of 50 Days of Data Science: Logistic Regression from Scratch 📈🐍

Welcome to **Day 27** of the **50 Days of Data Science Challenge**! 🎉  
Today, we're diving into the implementation of **logistic regression from scratch**. This exercise will help you understand the inner workings of one of the most fundamental algorithms in machine learning.

---

## 🎯 Objectives
- **Understand Logistic Regression**: Learn the theory behind logistic regression.
- **Implement from Scratch**: Write Python code to implement logistic regression without using libraries like scikit-learn.
- **Model Evaluation**: Evaluate the performance of your logistic regression model.
- **Visualize Results**: Use visualizations to interpret your model's outcomes.

---

## 📂 Files Included
- **`logistic-regression-from-scratch.ipynb`**: The Jupyter notebook for this task, containing the code to implement logistic regression from scratch.

---

## 📖 Topics Covered

### 1. 🌟 Introduction to Logistic Regression
   - **Definition**: Logistic regression is a statistical model used for binary classification problems.
   - **Applications**: Commonly used in fields like medicine, finance, and social sciences to predict binary outcomes.

### 2. 🔍 Theory Behind Logistic Regression
   - **Sigmoid Function**: The core of logistic regression, mapping any real-valued number into the range [0, 1].
     \[
     \sigma(z) = \frac{1}{1 + e^{-z}}
     \]
   - **Decision Boundary**: The threshold (usually 0.5) used to classify the input data into two classes.
   - **Cost Function**: The function to be minimized, typically the log-loss or binary cross-entropy.
     \[
     J(\theta) = -\frac{1}{m} \sum_{i=1}^{m} [y^{(i)} \log(h_\theta(x^{(i)})) + (1 - y^{(i)}) \log(1 - h_\theta(x^{(i)}))]
     \]

### 3. 🛠️ Implementation from Scratch
   - **Initialize Parameters**: Start with random or zero values for the weights.
   - **Compute Predictions**: Use the sigmoid function to get the probability estimates.
   - **Calculate Cost**: Implement the cost function to measure the error.
   - **Gradient Descent**: Update the weights using the gradient of the cost function.
   - **Iterate**: Repeat the process until convergence.

   ```python
   import numpy as np

   def sigmoid(z):
       return 1 / (1 + np.exp(-z))

   def compute_cost(X, y, theta):
       m = len(y)
       h = sigmoid(X.dot(theta))
       cost = -(1/m) * np.sum(y * np.log(h) + (1 - y) * np.log(1 - h))
       return cost

   def gradient_descent(X, y, theta, alpha, iterations):
       m = len(y)
       for i in range(iterations):
           gradient = X.T.dot(sigmoid(X.dot(theta)) - y) / m
           theta -= alpha * gradient
       return theta
   ```

### 4. 📊 Model Evaluation
   - **Accuracy**: The proportion of correctly predicted instances.
   - **Precision & Recall**: Metrics for evaluating classification performance, especially in imbalanced datasets.
   - **Confusion Matrix**: A matrix to visualize true positives, false positives, true negatives, and false negatives.

   ```python
   from sklearn.metrics import accuracy_score, precision_score, recall_score, confusion_matrix

   y_pred = (sigmoid(X.dot(theta)) >= 0.5).astype(int)
   accuracy = accuracy_score(y, y_pred)
   precision = precision_score(y, y_pred)
   recall = recall_score(y, y_pred)
   cm = confusion_matrix(y, y_pred)
   ```

### 5. 📈 Visualizing Results
   Visualize the decision boundary, cost reduction over iterations, and the confusion matrix.

   - **Decision Boundary**:
     ```python
     import matplotlib.pyplot as plt
     plt.scatter(X[:, 1], X[:, 2], c=y, cmap='viridis')
     x_value = np.array([np.min(X[:, 1]), np.max(X[:, 1])])
     y_value = -(theta[0] + theta[1] * x_value) / theta[2]
     plt.plot(x_value, y_value, "r")
     plt.show()
     ```

   - **Cost Reduction**:
     ```python
     costs = []
     for i in range(iterations):
         cost = compute_cost(X, y, theta)
         costs.append(cost)
         theta = gradient_descent(X, y, theta, alpha, 1)
     plt.plot(range(iterations), costs)
     plt.xlabel("Iterations")
     plt.ylabel("Cost")
     plt.title("Cost Reduction over Iterations")
     plt.show()
     ```

   - **Confusion Matrix**:
     ```python
     import seaborn as sns
     sns.heatmap(cm, annot=True, fmt="d", cmap="YlGnBu")
     plt.xlabel("Predicted")
     plt.ylabel("Actual")
     plt.title("Confusion Matrix")
     plt.show()
     ```

---