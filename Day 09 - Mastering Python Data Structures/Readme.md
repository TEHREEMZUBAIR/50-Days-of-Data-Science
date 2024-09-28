# 📚 Day 9: Data Structures in Python

Welcome to **Day 9** of the 50 Days of Data Science journey! Today, we're diving into **Python's data structures**. You will explore two essential structures: **sets** and **deques**, which are widely used for various computational tasks due to their unique properties and efficiencies.

## 📝 Objectives:
- Learn the basics of **sets** and perform operations such as union, intersection, and difference.
- Understand **deques** from the `collections` module and perform efficient operations from both ends of the queue.

---

## 🛠️ Instructions:

### 1️⃣ Sets in Python:
Python sets are unordered collections of unique elements. Sets support operations like union, intersection, and difference. Let's start by working with sets!

#### Tasks:
1. **Create two sets** with a mix of numbers and strings.
2. **Perform set operations**:
   - Union (`set1 | set2`)
   - Intersection (`set1 & set2`)
   - Difference (`set1 - set2`)
   - Symmetric Difference (`set1 ^ set2`)
3. Print the results for each operation and compare the outcomes.

### 2️⃣ Deques in Python:
`deque` (double-ended queue) allows for fast appends and pops from both ends. It's perfect for implementing **queues** efficiently.

#### Tasks:
1. **Initialize a deque** with some elements.
2. **Append new elements** to the right end of the deque.
3. **Pop elements** from the left end of the deque.
4. Print the deque after each operation to observe the changes.

---

## 🧪 Code Examples:

### Set Operations:
```python
# Define two sets
set1 = {1, 2, 3, "apple"}
set2 = {3, 4, 5, "banana"}

# Perform union
union_set = set1 | set2
print("Union:", union_set)

# Perform intersection
intersection_set = set1 & set2
print("Intersection:", intersection_set)

# Perform difference
difference_set = set1 - set2
print("Difference:", difference_set)
```

### Deque Operations:
```python
from collections import deque

# Initialize a deque
queue = deque(["Alice", "Bob", "Charlie"])

# Append to the deque
queue.append("David")
print("After appending David:", queue)

# Pop from the left of the deque
first_out = queue.popleft()
print("First person to leave:", first_out)

# Remaining queue
print("Remaining queue:", queue)
```

---
