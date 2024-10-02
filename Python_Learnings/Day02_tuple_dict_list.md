## **Lists**

### **Overview:**
- Lists are versatile data structures that store an ordered collection of items.
- **Properties:**
  - Mutable
  - Can hold elements of different data types
  - Allows duplicate data
  - Maintains order of insertion

### **List Operations:**
- **Creation:** `empty_list = []`
- **Accessing Elements:** 
  - Indexing: `my_list[index]`
  - Slicing: `my_list[startInd:endInd]`
- **Modifying List:**
  - Assigning: `my_list[index] = new_value`
- **Adding Elements:**
  - `append()`, `insert()`, `extend()`
- **Removing Elements:**
  - `remove()`, `pop()`, `clear()`
- **Copying List:** `copy()`
- **Concatenation:** `+` operator
- **Repetition:** `*` operator
- **Membership:** `in`, `not in`
- **Nested Lists:** `nested_list = [1, [2, 3], [4, 5, 6]]`
- **List Methods:** `sort()`, `reverse()`, `index()`, `count()`

---

## **Assignment 8: Prime Numbers List**
**Objective:** Create a program that generates and stores all prime numbers up to a given number in a list.

### **Instructions:**
- **Input:** Prompt the user to enter a positive integer `n`.
- **Logic:** Write a function that checks if a number is prime. Use a loop to generate all prime numbers up to `n` and store them in a list.
- **Output:** Display the list of prime numbers.

### **Code:**
```python
# Assignment 8: Prime Numbers List
def is_prime(num):
    if num <= 1:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

n = int(input("Enter a positive integer n: "))
prime_numbers = [i for i in range(2, n + 1) if is_prime(i)]

print("Prime numbers up to", n, ":", prime_numbers)
```

---

## **Assignment 9: Basic To-Do List**
**Objective:** Write a program that implements a basic to-do list where users can add, remove, and view tasks.

### **Instructions:**
- **Input:** Allow the user to add tasks, remove tasks by specifying the task name, and view the current list of tasks.
- **Logic:** Use a list to store the tasks. Implement a loop that continuously prompts the user to choose an action.
- **Output:** Display the updated to-do list after each operation.

### **Code:**
```python
# Assignment 9: Basic To-Do List
to_do_list = []

while True:
    action = input("Choose an action: add, remove, view, exit: ").strip().lower()
    
    if action == 'add':
        task = input("Enter the task to add: ")
        to_do_list.append(task)
        print("Task added.")
        
    elif action == 'remove':
        task = input("Enter the task to remove: ")
        if task in to_do_list:
            to_do_list.remove(task)
            print("Task removed.")
        else:
            print("Task not found.")
    
    elif action == 'view':
        print("Current To-Do List:", to_do_list)
    
    elif action == 'exit':
        break
    
    else:
        print("Invalid action. Please choose again.")
```

---

## **Tuples**

### **Overview:**
- Tuples store ordered collections of elements.
- **Properties:**
  - Immutable lists
  - Ordered
  - Heterogeneous
  - Memory efficient
  - Faster than lists

### **Tuple Operations:**
- **Creation:** `empty_tuple = ()`
- **Accessing Elements:**
  - Indexing: `my_tuple[ind]`
  - Slicing: `my_tuple[startInd:endInd]`
- **Concatenation:** `+` operator
- **Repetition:** `*` operator
- **Membership:** `in`, `not in`
- **Built-in Methods:** `count()`, `index()`
- **Tuple Unpacking:** `item1, item2, item3 = my_tuple`
- **Nested Tuples:** `nested_tuple = (1, (2, 3), (4, 5, 6))`
- **Converting Tuples to Lists**

---

## **Assignment 11: Tuple Manipulation**
**Objective:** Convert a list of elements to a tuple and perform various operations.

### **Instructions:**
- **Input:** Prompt the user to enter a list of elements separated by commas.
- **Tasks:**
  - Convert the input string to a tuple of integers.
  - Perform various operations and display the results.
- **Output:** Display results of the operations.

### **Code:**
```python
# Assignment 11: Tuple Manipulation
input_elements = input("Enter elements separated by commas (e.g., 10, 20, 30): ")
elements_tuple = tuple(int(x) for x in input_elements.split(','))

print("First element:", elements_tuple[0])
print("Last element:", elements_tuple[-1])
print("Tuple excluding first and last elements:", elements_tuple[1:-1])
print("Every second element:", elements_tuple[::2])
print("Reversed tuple:", elements_tuple[::-1])
```

---

## **Assignment 12: Tuple Packing and Unpacking**
**Objective:** Demonstrate tuple packing and unpacking, including nested tuple unpacking.

### **Instructions:**
- **Input:** Prompt the user for name, age, and a nested tuple containing city and country.
- **Logic:** Pack this information into a tuple, unpack it back into variables, and display the unpacked values.
- **Output:** Display the packed tuple and unpacked values.

### **Code:**
```python
# Assignment 12: Tuple Packing and Unpacking
name = input("Enter your name: ")
age = int(input("Enter your age: "))
city = input("Enter your city: ")
country = input("Enter your country: ")

# Packing
person_info = (name, age, (city, country))

# Unpacking
unpacked_name, unpacked_age, (unpacked_city, unpacked_country) = person_info

print("Packed tuple:", person_info)
print("Unpacked values: Name =", unpacked_name, ", Age =", unpacked_age, 
      ", City =", unpacked_city, ", Country =", unpacked_country)
```

---

## **Assignment 13: Tuple Statistics**
**Objective:** Calculate and display statistics for a tuple of integers.

### **Instructions:**
- **Input:** Prompt the user to enter a tuple of integers.
- **Tasks:** Convert the input string to a tuple of integers and calculate the sum, average, maximum, minimum, and count of elements.
- **Output:** Display results in a clear format.

### **Code:**
```python
# Assignment 13: Tuple Statistics
input_tuple = input("Enter a tuple of integers separated by commas (e.g., 5, 10, 15): ")
tuple_of_integers = tuple(int(x) for x in input_tuple.split(','))

total = sum(tuple_of_integers)
average = total / len(tuple_of_integers) if len(tuple_of_integers) > 0 else 0
maximum = max(tuple_of_integers)
minimum = min(tuple_of_integers)
count = len(tuple_of_integers)

print("Sum:", total)
print("Average:", average)
print("Maximum:", maximum)
print("Minimum:", minimum)
print("Count of elements:", count)
```

---

## **Assignment 14: Tuple Sorting and Filtering**
**Objective:** Sort and filter a tuple of integers.

### **Instructions:**
- **Input:** Prompt the user to enter a tuple of integers.
- **Tasks:** Convert the input string to a tuple of integers, sort it, and filter out elements greater than a specified threshold.
- **Output:** Display the sorted tuple and filtered elements.

### **Code:**
```python
# Assignment 14: Tuple Sorting and Filtering
input_tuple = input("Enter a tuple of integers separated by commas (e.g., 8, 3, 7, 1, 4): ")
tuple_of_integers = tuple(int(x) for x in input_tuple.split(','))

sorted_tuple = tuple(sorted(tuple_of_integers))
threshold = int(input("Enter a threshold for filtering: "))
filtered_elements = tuple(x for x in sorted_tuple if x <= threshold)

print("Sorted tuple:", sorted_tuple)
print("Filtered elements (<= threshold):", filtered_elements)
```

---



---

# Dictionaries

**Definition:**
Dictionaries are data structures that store data in key-value pairs, allowing for powerful and flexible management of complex data. They are mutable and indexed by unique keys.

**Key Characteristics:**
- **Mutable:** Can be changed after creation.
- **Indexed by Unique Keys:** Each key must be unique within a dictionary.

**Basic Operations:**
- **Declaration:**
  ```python
  empty_dict = {}
  ```

- **Accessing Dictionary Elements:**
  - Using keys:
    ```python
    my_dict = {"name": "Alice"}
    print(my_dict["name"])  # Output: Alice
    ```
  - Using the `get()` method:
    ```python
    print(my_dict.get("age", "Not found"))  # Output: Not found
    ```

- **Removing Key-Value Pairs:**
  ```python
  my_dict.pop("name")  # Removes key 'name'
  my_dict.popitem()     # Removes the last inserted key-value pair
  del my_dict["age"]    # Deletes the key 'age'
  my_dict.clear()       # Clears the dictionary
  ```

- **Modifying Dictionaries:**
  - Adding key-value pairs:
    ```python
    my_dict["key"] = [newVal1, newValn]
    ```

- **Checking for Key Existence:**
  ```python
  if "key" in my_dict:
      print("Key exists")
  ```

- **Dictionary Methods:**
  ```python
  keys = my_dict.keys()       # Get all keys
  values = my_dict.values()   # Get all values
  items = my_dict.items()     # Get all key-value pairs
  copy_dict = my_dict.copy()  # Create a copy of the dictionary
  ```

---

### Hands-on Assignments

#### Assignment 15: Create a program that stores and analyzes student’s grades using dictionaries.

**Input:**
Prompt the user to enter student names and their corresponding grades. Store the data in a dictionary where keys are student names and values are lists of grades.

**Logic:**
- Implement functions to:
  - Calculate the average grade for each student.
  - Find the student with the highest average grade.
  - Display students who have grades above a certain threshold.

**Output:**
- Display each student's average grade.
- Display the student with the highest average grade.
- Display the list of students with grades above a user-specified threshold.

**Code:**
```python
def student_grades_analysis():
    grades_dict = {}
    while True:
        name = input("Enter student name (or 'exit' to finish): ")
        if name.lower() == 'exit':
            break
        grades = list(map(float, input(f"Enter grades for {name} separated by spaces: ").split()))
        grades_dict[name] = grades

    for student, grades in grades_dict.items():
        avg_grade = sum(grades) / len(grades)
        print(f"{student}'s average grade: {avg_grade:.2f}")

    highest_student = max(grades_dict, key=lambda x: sum(grades_dict[x]) / len(grades_dict[x]))
    print(f"Student with the highest average grade: {highest_student}")

    threshold = float(input("Enter a grade threshold: "))
    above_threshold = [student for student, grades in grades_dict.items() if sum(grades) / len(grades) > threshold]
    print("Students with average grades above the threshold:", above_threshold)

student_grades_analysis()
```

---

#### Assignment 16: Develop a program to manage an inventory system for a small store.

**Input:**
Prompt the user to enter items, their quantities, and prices. Store the data in a dictionary where keys are item names, and values are another dictionary containing quantity and price.

**Logic:**
- Implement functions to:
  - Add new items to the inventory.
  - Update the quantity or price of existing items.
  - Calculate the total value of the inventory (sum of all items' value = quantity * price).

**Output:**
- Display the current inventory.
- Display the total value of the inventory.

**Code:**
```python
def inventory_management():
    inventory = {}
    while True:
        item = input("Enter item name (or 'exit' to finish): ")
        if item.lower() == 'exit':
            break
        quantity = int(input("Enter quantity: "))
        price = float(input("Enter price: "))
        inventory[item] = {'quantity': quantity, 'price': price}

    total_value = sum(item['quantity'] * item['price'] for item in inventory.values())
    print("Current Inventory:", inventory)
    print(f"Total value of inventory: ${total_value:.2f}")

inventory_management()
```

---
---

#### Assignment 17: Create a country capitals quiz program using dictionaries.

**Input:**
Store a dictionary of countries and their capitals. The keys will be the country names and the values will be the corresponding capitals.

**Logic:**
- Implement a quiz that randomly asks the user for the capital of various countries.
- Keep track of the number of correct answers and provide feedback for each answer.

**Output:**
- Display the number of correct answers after the quiz is finished.

**Code:**
```python
import random

def capitals_quiz():
    capitals = {
        "USA": "Washington D.C.",
        "France": "Paris",
        "Germany": "Berlin",
        "India": "New Delhi",
        "Brazil": "Brasilia"
    }
    questions = list(capitals.items())
    random.shuffle(questions)
    correct = 0

    for country, capital in questions:
        answer = input(f"What is the capital of {country}? ")
        if answer.lower() == capital.lower():
            print("Correct!")
            correct += 1
        else:
            print(f"Wrong! The correct answer is {capital}")

    print(f"You got {correct} out of {len(questions)} correct.")

capitals_quiz()
```

---

#### Assignment 18: Develop a phonebook application using dictionaries.

**Input:**
Prompt the user to add, search, update, delete, or display contacts in a phonebook. Each contact will have a name, phone number, and email.

**Logic:**
- Implement functions for:
  - Adding a new contact.
  - Searching for a contact by name.
  - Updating an existing contact's information.
  - Deleting a contact.
  - Displaying all contacts.

**Output:**
- Display appropriate messages based on the user's actions, including showing the current phonebook.

**Code:**
```python
def phonebook_application():
    phonebook = {}
    while True:
        action = input("Choose an action (add, search, update, delete, display, exit): ").lower()
        if action == 'exit':
            break
        if action == 'add':
            name = input("Enter name: ")
            phone = input("Enter phone number: ")
            email = input("Enter email: ")
            phonebook[name] = {'phone': phone, 'email': email}
        elif action == 'search':
            name = input("Enter name to search: ")
            if name in phonebook:
                print(f"Contact found: {phonebook[name]}")
            else:
                print("Contact not found.")
        elif action == 'update':
            name = input("Enter name to update: ")
            if name in phonebook:
                phone = input("Enter new phone number: ")
                email = input("Enter new email: ")
                phonebook[name] = {'phone': phone, 'email': email}
            else:
                print("Contact not found.")
        elif action == 'delete':
            name = input("Enter name to delete: ")
            if name in phonebook:
                del phonebook[name]
                print(f"Deleted contact for {name}.")
            else:
                print("Contact not found.")
        elif action == 'display':
            print("Phonebook contacts:")
            for name, details in phonebook.items():
                print(f"{name}: {details}")

phonebook_application()
```

---

#### Assignment 19: Write a program to count the frequency of elements in a list.

**Input:**
Prompt the user to enter a list of elements separated by spaces.

**Logic:**
- Use a dictionary to count the frequency of each element in the list.
- Store each element as a key and its count as the corresponding value.

**Output:**
- Display the frequency of each element.

**Code:**
```python
def frequency_count():
    elements = input("Enter a list of elements separated by spaces: ").split()
    frequency = {}
    for element in elements:
        frequency[element] = frequency.get(element, 0) + 1

    print("Frequency of each element:", frequency)

frequency_count()
```

---

#### Assignment 20: Create a book collection management system using dictionaries.

**Input:**
Prompt the user to enter book titles, authors, genres, and publication years. Store this data in a dictionary.

**Logic:**
- Implement functions for:
  - Adding new books to the collection.
  - Removing books from the collection.
  - Searching for books by author or genre.
  - Displaying the entire book collection.

**Output:**
- Show the current book collection and allow for various actions on the collection.

**Code:**
```python
def book_collection_management():
    books = {}
    while True:
        action = input("Choose an action (add, remove, search, display, exit): ").lower()
        if action == 'exit':
            break
        if action == 'add':
            title = input("Enter book title: ")
            author = input("Enter author: ")
            genre = input("Enter genre: ")
            year = input("Enter year of publication: ")
            books[title] = {'author': author, 'genre': genre, 'year': year}
        elif action == 'remove':
            title = input("Enter title to remove: ")
            if title in books:
                del books[title]
                print(f"Removed book: {title}.")
            else:
                print("Book not found.")
        elif action == 'search':
            search_query = input("Enter author or genre to search: ")
            found_books = {title: details for title, details in books.items() if details['author'] == search_query or details['genre'] == search_query}
            if found_books:
                print("Found books:", found_books)
            else:
                print("No books found.")
        elif action == 'display':
            print("Current Book Collection:")
            for title, details in books.items():
                print(f"{title}: {details}")

book_collection_management()
```

---

### Homework Assignments

#### Homework Assignment 1: Create a pyramid of stars based on user input.

**Input:**
Prompt the user to enter the number of rows for the pyramid.

**Logic:**
- Print spaces and stars in each row to create a pyramid shape.

**Output:**
- Display a pyramid of stars.

**Code:**
```python
def print_star_pyramid():
    rows = int(input("Enter number of rows: "))
    for i in range(1, rows + 1):
        print(' ' * (rows - i) + '*' * (2 * i - 1))

print_star_pyramid()
```

---

#### Homework Assignment 2: Build a simple calculator that uses match-case for operations.

**Input:**
Prompt the user to enter an operation (+, -, *, /) and two numbers.

**Logic:**
- Perform the requested operation using match-case.

**Output:**
- Display the result of the operation.

**Code:**
```python
def calculator():
    while True:
        operation = input("Enter operation (+, -, *, /) or 'exit' to quit: ")
        if operation == 'exit':
            break
        match operation:
            case '+':
                a, b = map(float, input("Enter two numbers separated by space: ").split())
                print(f"Result: {a + b}")
            case '-':
                a, b = map(float, input("Enter two numbers separated by space: ").split())
                print(f"Result: {a - b}")
            case '*':
                a, b = map(float, input("Enter two numbers separated by space: ").split())
                print(f"Result: {a * b}")
            case '/':
                a, b = map(float, input("Enter two numbers separated by space: ").split())
                if b != 0:
                    print(f"Result: {a / b}")
                else:
                    print("Error: Division by zero.")
            case _:
                print("Invalid operation. Please try again.")

calculator()
```

---

#### Homework Assignment 3: Calculate a student’s final grade based on different assessment weights.

**Input:**
Prompt the user to enter the student's name and their scores for homework, quizzes, midterms, and finals.

**Logic:**
- Calculate the final grade using the formula:
  - Final Grade = (Homework * 0.2) + (Quizzes * 0.2) + (Midterm * 0.3) + (Final * 0.3)

**Output:**
- Display the final grade for the student.

**Code:**
```python
def calculate_final_grade():
    name = input("Enter student's name: ")
    homework = float(input("Enter homework score (20%): "))
    quizzes = float(input("Enter quizzes score (20%): "))
    midterm = float(input("Enter midterm score (30%): "))
    final_exam = float(input("Enter final exam score (30%): "))

    final_grade = (homework * 0.2) + (quizzes * 0.2) + (midterm * 0.3) + (final_exam * 0.3)
    print(f"{name}'s final grade: {final_grade:.2f}")

calculate_final_grade()
```

---

