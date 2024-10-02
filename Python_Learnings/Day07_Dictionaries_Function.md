
---

### **Dictionaries**  
Dictionaries are versatile data structures in Python that store data in key-value pairs. They are designed for efficient data retrieval and manipulation. Here are some key characteristics of dictionaries:
- **Mutable**: Dictionaries can be changed after their creation, allowing for modifications such as adding or removing key-value pairs.
- **Powerful and Flexible**: They can efficiently store and manage complex data types, making them ideal for a wide range of applications.
- **Indexed by Unique Keys**: Each key in a dictionary must be unique, and it is used to access the corresponding value.

---

### **Dictionary Operations**  
- **Definition**: A dictionary is defined using curly braces. For example:  
  `empty_dict = {}`

- **Accessing Dictionary Elements**: You can access values in a dictionary using keys. For instance:  
  `my_dict[key]` retrieves the value associated with `key`. Alternatively, you can use the `get()` method:  
  `my_dict.get("age")` returns the value for the key `"age"`.

- **Removing Key-Value Pairs**: There are several methods to remove items from a dictionary:
  - **pop()**: Removes the specified key and returns its value.  
  `my_dict.pop("age")`
  - **popitem()**: Removes the last inserted key-value pair.  
  `my_dict.popitem()`
  - **del()**: Deletes the specified key-value pair.  
  `del my_dict["age"]`
  - **clear()**: Removes all items from the dictionary.  
  `my_dict.clear()`

- **Modifying Lists**: You can add key-value pairs to a dictionary using:  
  `my_dict["key"] = [newVal1, newValn]`

- **Checking for Key Existence**: Use `in` or `not in` to check for the existence of a key in the dictionary.

- **Directory Methods**: Some commonly used dictionary methods include:
  - **keys()**: Returns a view object displaying a list of all keys.
  - **values()**: Returns a view object displaying a list of all values.
  - **items()**: Returns a view object displaying a list of all key-value pairs.
  - **copy()**: Creates a shallow copy of the dictionary.

---

### **Hands-On Assignments**

#### **Assignment 1**:  
Create a dictionary where the keys are integers from 1 to 5 and the values are their cubes.

**Solution:**
```python
cubes_dict = {i: i**3 for i in range(1, 6)}
print("Cubes dictionary:", cubes_dict)
```

---

#### **Assignment 2**:  
Generate a dictionary with letters 'a' to 'e' as keys and their ASCII values as values.

**Solution:**
```python
ascii_dict = {chr(i): i for i in range(97, 102)}  # 97 to 101 corresponds to 'a' to 'e'
print("ASCII values dictionary:", ascii_dict)
```

---

#### **Assignment 3**:  
Generate a dictionary with the following keys: “Name”, “RollNo”, “Science”, “Maths”, “English”. Accept values for these from the user. Calculate “Average” and “Percentage” and add these to the dictionary. Print the final dictionary.

**Solution:**
```python
student_dict = {}
student_dict["Name"] = input("Enter Name: ")
student_dict["RollNo"] = input("Enter Roll No: ")
student_dict["Science"] = float(input("Enter Science marks: "))
student_dict["Maths"] = float(input("Enter Maths marks: "))
student_dict["English"] = float(input("Enter English marks: "))

total_marks = student_dict["Science"] + student_dict["Maths"] + student_dict["English"]
student_dict["Average"] = total_marks / 3
student_dict["Percentage"] = (total_marks / 300) * 100

print("Final Dictionary:", student_dict)
```

---

### **Dictionary Keys**  
- **Valid Keys**:
  - **Strings**:  
    `my_dict = {"key": "value"}`
  - **Numbers**:  
    `my_dict = {1: "one", 2: "two"}`
  - **Tuples**:  
    `my_dict = {(1, 2): "pair"}`

- **Invalid Keys**:
  - **Lists**:  
    `my_dict = {[1, 2]: "list"}`  # Raises a TypeError
  - **Dictionaries**:  
    `my_dict = {{1: 2}: "dict"}`  # Raises a TypeError

---

### **Hands-On Assignments (Continued)**

#### **Assignment 4**:  
Develop a program to manage an inventory system for a small store.
- **Input**: Prompt the user to enter items, their quantities, and prices. Store the data in a dictionary where keys are item names, and values are another dictionary containing quantity and price.

- **Logic**: Implement functions to:
  - Add new items to the inventory.
  - Update the quantity or price of existing items.
  - Calculate the total value of the inventory (sum of all items' value = quantity * price).

- **Output**: Display the current inventory and the total value of the inventory.

**Solution:**
```python
inventory = {}

def add_item(name, quantity, price):
    inventory[name] = {"quantity": quantity, "price": price}

def update_item(name, quantity=None, price=None):
    if name in inventory:
        if quantity is not None:
            inventory[name]["quantity"] = quantity
        if price is not None:
            inventory[name]["price"] = price

def total_inventory_value():
    return sum(item["quantity"] * item["price"] for item in inventory.values())

while True:
    action = input("Choose action: add, update, total, view, exit: ")
    if action == "exit":
        break
    elif action == "add":
        item_name = input("Enter item name: ")
        item_quantity = int(input("Enter item quantity: "))
        item_price = float(input("Enter item price: "))
        add_item(item_name, item_quantity, item_price)
    elif action == "update":
        item_name = input("Enter item name to update: ")
        item_quantity = input("Enter new quantity (or leave blank): ")
        item_price = input("Enter new price (or leave blank): ")
        update_item(item_name, int(item_quantity) if item_quantity else None,
                     float(item_price) if item_price else None)
    elif action == "total":
        print("Total inventory value:", total_inventory_value())
    elif action == "view":
        print("Current inventory:", inventory)
```

---

### **Homework Assignments**

#### **Homework Assignment 1**:  
Build a simple phonebook application using dictionaries.
- **Input**: Allow the user to add, search, update, and delete contacts in the phonebook. Each contact should have a name, phone number, and email.

- **Logic**: Use a dictionary where keys are contact names and values are another dictionary containing the phone number and email. Implement functions for adding, searching, updating, and deleting contacts. Ensure the phonebook is case-insensitive when searching for contacts.

- **Output**: Display all contacts after each operation. Display a message if a contact is not found during a search or delete operation.

**Solution:**
```python
phonebook = {}

def add_contact(name, phone, email):
    phonebook[name.lower()] = {"phone": phone, "email": email}

def search_contact(name):
    return phonebook.get(name.lower(), None)

def update_contact(name, phone=None, email=None):
    contact = search_contact(name)
    if contact:
        if phone:
            contact["phone"] = phone
        if email:
            contact["email"] = email

def delete_contact(name):
    return phonebook.pop(name.lower(), None)

while True:
    action = input("Choose action: add, search, update, delete, view, exit: ")
    if action == "exit":
        break
    elif action == "add":
        name = input("Enter contact name: ")
        phone = input("Enter phone number: ")
        email = input("Enter email: ")
        add_contact(name, phone, email)
    elif action == "search":
        name = input("Enter contact name to search: ")
        contact = search_contact(name)
        if contact:
            print("Contact found:", contact)
        else:
            print("Contact not found.")
    elif action == "update":
        name = input("Enter contact name to update: ")
        phone = input("Enter new phone number (or leave blank): ")
        email = input("Enter new email (or leave blank): ")
        update_contact(name, phone if phone else None, email if email else None)
    elif action == "delete":
        name = input("Enter contact name to delete: ")
        if delete_contact(name):
            print("Contact deleted.")
        else:
            print("Contact not found.")
    elif action == "view":
        print("Phonebook:", phonebook)
```
