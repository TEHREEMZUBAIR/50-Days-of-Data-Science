
# 📘 Day 10: Practical Projects with Python Data Structures

Welcome to **Day 10** of the 50 Days of Data Science challenge! Today, you'll use the data structures you've learned to build projects that simulate real-world applications. Get ready to create a **Product Inventory System**, a **Phone Book Application**, and a **Restaurant Billing System**.

---

## 📝 Objectives:
- Implement a **Product Inventory System** to manage products and their stock.
- Build a **Phone Book Application** to store and manage contacts.
- Create a **Restaurant Billing System** that allows users to order and calculate bills.

---

## 🛠️ Instructions:

### 1️⃣ Product Inventory System:
Manage an inventory of products with details such as product ID, name, category, and stock.

#### Tasks:
1. **Add a product** with a unique ID, name, category, and initial stock.
2. **Update the stock** of a product by its ID.
3. **Display all products** or filter them by category.

### 2️⃣ Phone Book Application:
Use a dictionary to store and manage contacts in a phone book.

#### Tasks:
1. **Add a new contact** with a name and phone number.
2. **Delete a contact** by name.
3. **Update an existing contact**'s phone number.
4. **Display all contacts** in the phone book.

### 3️⃣ Restaurant Billing System:
Simulate a restaurant's ordering and billing process using lists and dictionaries.

#### Tasks:
1. **Display the menu** with item names and prices.
2. **Add items** to the customer’s order.
3. **View the current order** showing item names and quantities.
4. **Calculate the total bill** based on the items in the order.

---

## 🧪 Code Examples:

### Product Inventory System:
```python
# Example for adding a product
inventory = {}

def add_product(product_id, name, category, stock):
    if product_id in inventory:
        print(f"Product ID {product_id} already exists.")
    else:
        inventory[product_id] = {'name': name, 'category': category, 'stock': stock}
        print(f"Added {name} to inventory.")

# Add products
add_product('01', 'Table', 'Furniture', 100)
add_product('02', 'Chair', 'Furniture', 50)
```

### Phone Book Application:
```python
# Phone book application
phone_book = {}

def add_contact(name, phone_number):
    if name in phone_book:
        print(f"{name} is already in the phone book.")
    else:
        phone_book[name] = phone_number
        print(f"Added {name} with phone number {phone_number} to the phone book.")

# Add a contact
add_contact('Alice', '123-456-7890')
```

### Restaurant Billing System:
```python
# Restaurant billing system
menu = {'Burger': 150, 'Pizza': 200, 'Taco': 100}
order = {}

def add_to_order(item, quantity):
    if item in menu:
        if item in order:
            order[item] += quantity
        else:
            order[item] = quantity
        print(f"Added {quantity} {item}(s) to your order.")
    else:
        print("Item not available.")

# Add items to order
add_to_order('Burger', 3)
add_to_order('Taco', 5)
```

---