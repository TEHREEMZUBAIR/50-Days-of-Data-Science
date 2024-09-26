---

# 🌟 **Task 4: Mastering Conditional Statements (Leap Year Checker)**

### 👩‍💻 **Overview**
Welcome to Day 4 of your Data Science challenge! 🎉 Today, you'll learn how to use conditional statements in Python to perform decision-making tasks. Specifically, you'll be building a **Leap Year Checker** 🗓️—a simple yet powerful program that teaches the fundamentals of `if`, `elif`, and `else` statements.

### 🌟 **Objectives**
By the end of this task, you will:
- 📌 Understand how to use Python’s conditional statements.
- 🧠 Learn to structure your code to handle different scenarios.
- 🔍 Build a leap year checker using Python's `if-else` statements.

### 📚 **Topics Covered**
1. **Conditional Statements**: `if`, `elif`, and `else` for decision-making.
2. **Leap Year Logic**: The rules to determine if a year is a leap year.

### ⚙️ **Task Details**

#### 📝 1. **Understanding `if` Statements**
The `if` statement is used to test a condition. If the condition is `True`, the code block inside the `if` is executed; otherwise, it skips to the next condition.

#### 🧮 2. **Leap Year Logic**
A year is a leap year if:
- It is divisible by 4 **and** not divisible by 100, **or**
- It is divisible by 400.

#### 🛠️ **Example Code: Leap Year Checker**
```python
# Leap Year Checker
year = int(input("Enter a year: "))
if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print(f"{year} is a leap year!")
else:
    print(f"{year} is not a leap year.")
```
In this code:
- We use the `input()` function to get a year from the user.
- The conditions check whether the year is a leap year based on the rules.

#### ➡️ **Exploring Conditionals**
- **`if`**: Executes a code block if the condition is `True`.
- **`else`**: Executes a code block if all preceding conditions are `False`.
- **`elif`**: Used for additional conditions if the previous ones are `False`.

### 🛠️ **Requirements**
- Python installed on your machine or access to a Jupyter Notebook environment.
  
### 🔑 **How to Complete the Task**
1. 🏗️ **Set up your environment**: Make sure you have Python ready.
2. 🎯 **Build your leap year checker**: Use conditional statements to check if a year is a leap year.
3. 🧪 **Test your code**: Try different years (e.g., 2000, 1900, 2024) and see if your program works as expected.
4. 💾 **Document your code**: Add comments in Markdown cells to explain how your logic works.

### 📦 **Deliverables**
- A Jupyter Notebook (.ipynb) containing:
  - Your leap year checker code.
  - Markdown explanations and comments about how the conditional logic works.

### 🚀 **Bonus Challenge**
Can you extend the program to check multiple years in a row? 🎯 Try using a `while` or `for` loop to handle repeated inputs!

---
