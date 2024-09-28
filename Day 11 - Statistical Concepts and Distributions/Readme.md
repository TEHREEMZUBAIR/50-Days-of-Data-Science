# 📘 Day 11: Statistical Analysis and Probability Distributions

Welcome to **Day 11** of the 50 Days of Data Science challenge! Today, we will explore key statistical concepts that are essential for data analysis, including measures of central tendency and various probability distributions.

---

## 📝 Objectives:
- Understand and calculate **mean**, **median**, and **mode**.
- Solve **probability** problems using different scenarios.
- Compute **variance** and **standard deviation**.
- Work with **binomial**, **Poisson**, and **uniform distributions** to solve real-world problems.

---

## 🛠️ Instructions:

### 1️⃣ Measures of Central Tendency:  
You will calculate **mean**, **median**, and **mode** for given datasets.

#### Tasks:
1. **Mean**: Calculate the arithmetic mean for a set of exam scores.
2. **Median**: Find the median from a dataset representing temperatures.
3. **Mode**: Determine the mode of a dataset representing frequency of occurrences.

### 2️⃣ Probability Calculations:  
You will solve various probability problems, including tossing coins, drawing cards, and rolling dice.

#### Tasks:
1. **Coin Toss Probability**: Calculate the probability of getting 2 heads when tossing two coins.
2. **Card Probability**: Calculate the probability of drawing an honor card from a deck of 52 cards.

### 3️⃣ Variance and Standard Deviation:  
You will compute the **variance** and **standard deviation** for datasets.

#### Tasks:
1. **Exam Scores**: Find the variance and standard deviation of a set of exam scores.
2. **Temperature Data**: Calculate the standard deviation of temperatures recorded over five days.

### 4️⃣ Distributions:  
You will work with **binomial**, **Poisson**, and **uniform distributions** to solve statistical problems.

#### Tasks:
1. **Binomial Distribution**: Find the binomial distribution for getting a six in three rolls of a die.
2. **Poisson Distribution**: Calculate the probability that there will be exactly 3 accidents at an intersection next week.
3. **Uniform Distribution**: Determine the probability that a person waits fewer than 12.5 minutes for a bus, given the wait times are uniformly distributed between 0 and 15 minutes.

---

## 🧪 Code Examples:

### Mean Calculation:
```python
# Example dataset
exam_scores = [92, 95, 85, 80, 75, 50]

# Calculate the mean
mean_score = sum(exam_scores) / len(exam_scores)
print("Mean Score:", mean_score)
```

### Coin Toss Probability:
```python
# Two coins tossed
total_outcomes = 500
two_heads = 105
probability_two_heads = two_heads / total_outcomes
print("Probability of Two Heads:", probability_two_heads)
```

### Poisson Distribution:
```python
# Poisson distribution example
from math import exp, factorial

# Average rate of accidents
lambda_accidents = 1.4

# Calculate Poisson probability for exactly 3 accidents
k = 3
poisson_prob = (lambda_accidents ** k * exp(-lambda_accidents)) / factorial(k)
print("Probability of 3 accidents:", poisson_prob)
```