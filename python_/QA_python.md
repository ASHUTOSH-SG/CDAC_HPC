## 1 Difference Between List and Tuple


| Feature                  | List                                     | Tuple                                  |
|--------------------------|------------------------------------------|----------------------------------------|
| **Mutability**           | Mutable (can be changed)                | Immutable (cannot be changed)         |
| **Container Type**       | Mixed types (e.g., strings, numbers)    | Mixed types, fixed size                |
| **Syntax**               | `my_list = ['a', 'b', 1]`               | `my_tuple = ('a', 'b', 1)`            |
| **Iteration Speed**      | Slower                                   | Faster                                 |
| **Memory Consumption**   | More memory                              | Less memory                            |
| **Element Modification** | Supports add/remove/modify               | No modification allowed                |
| **Use Case**             | Dynamic collections (e.g., tasks)       | Fixed collections (e.g., coordinates)  |

## 2 What is a Decorator?
A decorator in Python is a function that takes another function as an argument, adds some functionality to it, and returns a new function. Decorators allow you to modify or enhance the behavior of a function without changing its source code.

```
def my_decorator(func):
    def wrapper():
        print("Before the function call.")
        func()  # Call the original function
                # say hello function
        print("After the function call.")
    return wrapper

@my_decorator
def say_hello():
    print("Hello!")

# Call the decorated function
say_hello()


```
## output
```
Before the function call.
Hello!
After the function call.
```

## 3 List and Dictionary Comprehension
**Comprehensions** provide a concise way to create lists and dictionaries in Python. They can replace loops and make your code more readable


**List Comprehension Purpose:** Create a new list from an existing iterable

Syntax
```
new_list = [expression for item in iterable if condition]

```
**example**
generates a list of squares of even numbers from 0 to 9.

```
squares = [x**2 for x in range(10) if x % 2 == 0]
print(squares)  # Output: [0, 4, 16, 36, 64]

```
**Dictionary Comprehension**
Purpose: Create a new dictionary from an existing iterable.

Syntax
```
new_dict = {key_expression: value_expression for item in iterable if condition}

```
Example

```
squares_dict = {x: x**2 for x in range(5)}
print(squares_dict)  # Output: {0: 0, 1: 1, 2: 4, 3: 9, 4: 16}

```

## more example


## List Creation
**Common Way:**
```python
squares = []
for x in range(10):
    squares.append(x**2)
print(squares)  # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

**Using Comprehension:**
```python
squares = [x**2 for x in range(10)]
print(squares)  # Output: [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

### Output
Output for both methods: `[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]`

---

## Dictionary Creation
**Common Way:**
```python
fruits = {}
for fruit in ["apple", "banana", "cherry"]:
    fruits[fruit] = len(fruit)
print(fruits)  # Output: {'apple': 5, 'banana': 6, 'cherry': 6}
```

**Using Comprehension:**
```python
fruits = {fruit: len(fruit) for fruit in ["apple", "banana", "cherry"]}
print(fruits)  # Output: {'apple': 5, 'banana': 6, 'cherry': 6}
```

### Output
Output for both methods: `{'apple': 5, 'banana': 6, 'cherry': 6}`

## 4 . How Memory Managed In Python

### Memory Management in Python (Short and Simple)

- **Private Heap**: Python uses a private heap for storing all objects and data structures. The interpreter manages this heap.

- **Memory Allocation**: The Python memory manager allocates space for objects automatically.

- **Garbage Collection**: Python has a built-in garbage collector that frees memory when objects are no longer needed.

- **GC Module**: You can control garbage collection using:
  - `gc.enable()`: Turns on automatic garbage collection.
  - `gc.disable()`: Turns off automatic garbage collection.

## 5. Difference Between Generators And Iterators


### Table: Difference Between Generators and Iterators

| **Feature**               | **Generator**                                    | **Iterator**                                      |
|---------------------------|--------------------------------------------------|---------------------------------------------------|
| **Definition**            | A special type of iterator that can be iterated only once. | An object that can iterate over a collection of values. |
| **Keyword Used**          | Uses the `yield` keyword to produce values.     | Uses `iter()` and `next()` functions to iterate. |
| **Iteration**             | Generates values on-the-fly in a loop without storing them in memory. | Stores values in memory and can iterate through them. |
| **Use Case**              | Ideal for creating sequences where values are generated one at a time. | Used for iterating over iterable objects like lists, tuples, and sets. |
| **Every**                 | Every generator is an iterator.                  | Every iterator is not a generator.                |

### Example: Generator
**Creating a Generator:** A generator uses yield to produce values one at a time.

**Efficiency:** It saves memory by generating items on-the-fly instead of storing them all.

**Iteration Control:** Use next() to get values one by one.

```python
def sqr(n):
    for i in range(1, n + 1):
        yield i * i

a = sqr(3)
print(next(a))  # Output: 1
print(next(a))  # Output: 4
print(next(a))  # Output: 9
```


### Example: Iterator

- **Creating an Iterator**: The `iter()` function turns a list into an iterator, which keeps track of where you are in the list.

- **Efficiency**: Iterators use less memory, especially with large datasets, since they don’t store all items at once.

- **Iteration Control**: You can use `next()` to get items one at a time, allowing you to control the flow of iteration.

```python
iter_list = iter(['A', 'B', 'C'])
print(next(iter_list))  # Output: A
print(next(iter_list))  # Output: B
print(next(iter_list))  # Output: C
```

##  6 What is the `__init__` Keyword in Python?

#### `__init__.py` File
- **Purpose**: Marks a directory as a Python package, allowing imports from it.
- **Content**: Can be empty or contain initialization code.

#### `__init__()` Function
- **Purpose**: Initializes an object's state when an instance is created.
- **Functionality**: Acts like a constructor.

### Sample Class

```python
class Person: 
    def __init__(self, name):  # Constructor
        self.name = name  # Set name
      
    def say_hi(self):  
        print('Hello, my name is', self.name)  

p = Person('Nitin')  # Create instance
p.say_hi()  # Output: Hello, my name is Nitin
```

## 7. Difference Between Modules and Packages in Python

### Difference Between Modules and Packages in Python

#### Module
- **Definition**: A module is a single Python file with a `.py` extension that contains functions, classes, and variables.
- **Usage**: You can import a module using `import my_module`.
- **Example**: 
  ```python
  import math  # Imports the math module
  ```

#### Package
- **Definition**: A package is a directory that contains multiple modules and a special `__init__.py` file.
- **Usage**: Packages can contain sub-packages and create a namespace for organizing modules.
- **Example**: 
  ```python
  from my_package import my_module  # Imports a module from a package
  ```

## 8. Difference Between Range and Xrange?

### Difference Between `range` and `xrange`

| Parameter            | `range()`                                   | `xrange()`                          |
|----------------------|---------------------------------------------|-------------------------------------|
| **Return Type**      | Returns a list of integers.                 | Returns a generator object.         |
| **Memory Consumption**| Takes more memory because it creates a list. | Uses less memory as it generates values on-the-fly. |
| **Speed**            | Slower execution speed.                     | Faster execution speed.             |
| **Python Version**   | Available in Python 2 and 3.               | Only in Python 2; no longer exists in Python 3. |
| **Operations**       | Supports all arithmetic operations.         | Does not support arithmetic operations directly. |

**Summary**: Use `range()` for lists in Python 2 and 3, and `xrange()` for memory-efficient iterations in Python 2 only. In Python 3, `range()` behaves like `xrange()`.

## 9. What are in-built Data Types in Python OR Explain Mutable and Immutable Data Types

| Data Type      | Mutable or Immutable? | Example                     |
|----------------|------------------------|-----------------------------|
| Boolean (bool) | Immutable              | `is_active = True`         |
| Integer (int)  | Immutable              | `count = 5`                |
| Float          | Immutable              | `price = 19.99`            |
| String (str)   | Immutable              | `name = "Alice"`           |
| Tuple          | Immutable              | `coordinates = (10, 20)`   |
| Frozenset      | Immutable              | `my_frozenset = frozenset([1, 2, 3])` |
| List           | Mutable                | `items = [1, 2, 3]`        |
| Set            | Mutable                | `unique_numbers = {1, 2, 3}` |
| Dictionary     | Mutable                | `person = {"name": "Bob", "age": 30}` |


## 10. Explain Ternary Operator in Python?


### Ternary Operator in Python

The ternary operator lets you choose between two values based on a condition in one line.

### Syntax:
```
[if_true] if [condition] else [if_false]
```

#### Example:
```python
number = 10
result = "Even" if number % 2 == 0 else "Odd"
print(result)  # Output: Even
```

In this example, `result` is set to `"Even"` if `number` is even; otherwise, it is set to `"Odd"`.



## 12. What is Inheritance In Python
### What is Inheritance in Python?

Inheritance allows a child class to inherit attributes and methods from a parent class. This enables code reuse and the creation of a hierarchy of classes.

#### Syntax:
```python
class ChildClass(ParentClass):
```

#### Example:
```python
class A:  
    def display(self):  
        print("A Display")  

class B(A):  # B inherits from A
    def show(self):  
        print("B Show")  

d = B()  
d.show()      # Output: B Show
d.display()   # Output: A Display
```

**Output:**
```
B Show
A Display
```

## 13. Difference Between Local and Global Variable in Python
### Difference Between Local and Global Variables in Python

| Feature                | Local Variable                     | Global Variable                    |
|------------------------|-----------------------------------|------------------------------------|
| **Declaration**        | Inside a function.                | Outside any function.              |
| **Initialization**     | Garbage value if uninitialized.   | Defaults to zero if uninitialized. |
| **Lifetime**           | Exists only during function run.  | Exists for the entire program.     |
| **Data Sharing**       | Not shared; local to the function. | Shared; accessible by all functions.|
| **Modification**       | Changes not visible outside.       | Changes visible throughout the program.|
| **Access**             | Only within the declaring function. | Accessible from anywhere in the program. |
| **Storage**            | Stored on the stack.              | Stored in a fixed memory location. |


## 14. Explain Break, Continue and Pass Statement

### Break, Continue, and Pass Statements in Python

#### 1. Break Statement
- **Description**: Terminates the loop entirely. If used in nested loops, it exits only the current loop.
- **Example**:
  ```python
  for i in range(10):    
      if i == 7:
          break  
      print(i, end=", ")
  ```
  **Output**: 
  ```
  0, 1, 2, 3, 4, 5, 6, 
  ```

#### 2. Continue Statement
- **Description**: Stops the current iteration and skips to the next iteration of the loop.
- **Example**:
  ```python
  for i in range(10):    
      if i == 7:
          continue  
      print(i, end=", ")
  ```
  **Output**: 
  ```
  0, 1, 2, 3, 4, 5, 6, 8, 9, 
  ```

#### 3. Pass Statement
- **Description**: A null statement that does nothing; it's a placeholder that can be used when a statement is syntactically required but no action is needed.
- **Example**:
  ```python
  def my_func():
      print('pass inside function')
      pass

  my_func()
  ```
  **Output**: 
  ```
  pass inside function
  ```

### 15 What is the `self` Keyword in Python?

The `self` keyword refers to the current instance of a class. It is used to access variables and methods that belong to that instance.

#### Example:

```python
class Person:
    def __init__(self, name, age):
        self.name = name  # Assigning name to the instance
        self.age = age    # Assigning age to the instance

    def info(self):
        print(f"My name is {self.name}. I am {self.age} years old.")

c = Person("Nitin", 23)  # Creating an instance of Person
c.info()  # Calling the info method
```

**Output:**
```
My name is Nitin. I am 23 years old.
```

In this example, `self` allows the methods in the `Person` class to access the instance variables `name` and `age`.


### 16 Pickling vs. Unpickling

- **Pickling**: The process of converting a Python object into a byte stream to save it to a file. 
  - **Function**: `pickle.dump()`

- **Unpickling**: The process of converting the byte stream back into the original Python object.
  - **Function**: `pickle.load()`

**Summary**: Pickling saves objects; unpickling loads them back.

## 17. Explain Function of List, Set, Tuple And Dictionary?


### Functions of List

| Function         | Description                              | Example                       |
|------------------|------------------------------------------|-------------------------------|
| `sort()`         | Sorts the list in ascending order.      | `my_list.sort()`             |
| `append()`       | Adds a single element to the list.      | `my_list.append(4)`          |
| `extend()`       | Adds multiple elements to the list.     | `my_list.extend([5, 6])`     |
| `index()`        | Returns the first appearance of a value.| `my_list.index(3)`           |
| `max()`          | Returns the max value from the list.    | `max(my_list)`               |
| `min()`          | Returns the min value from the list.    | `min(my_list)`               |
| `len()`          | Returns the total length of the list.   | `len(my_list)`               |
| `list(seq)`      | Converts a tuple or another iterable to a list.| `my_list = list((1, 2))`   |
| `type()`         | Returns the class type of the object.   | `type(my_list)`              |

### Example Usage
```python
my_list = [3, 1, 2]
my_list.sort()             # Sorts: [1, 2, 3]
my_list.append(4)          # List becomes: [1, 2, 3, 4]
my_list.extend([5, 6])     # List becomes: [1, 2, 3, 4, 5, 6]
print(my_list.index(3))    # Outputs: 2 (index of 3)
print(max(my_list))        # Outputs: 6
print(min(my_list))        # Outputs: 1
print(len(my_list))        # Outputs: 6
new_list = list((7, 8))    # Converts tuple to list: [7, 8]
print(type(my_list))       # Outputs: <class 'list'>
```



### Functions of Tuple

| Function       | Description                                          | Example                           |
|----------------|------------------------------------------------------|-----------------------------------|
| `cmp()`        | Compares two tuples (not available in Python 3).   | `cmp(tuple1, tuple2)`            |
| `len()`        | Returns the total length of the tuple.              | `len(my_tuple)`                  |
| `max()`        | Returns the maximum value from the tuple.           | `max(my_tuple)`                  |
| `min()`        | Returns the minimum value from the tuple.           | `min(my_tuple)`                  |
| `tuple()`      | Converts a list or other iterable into a tuple.     | `my_tuple = tuple([1, 2, 3])`    |
| `sum()`        | Returns the sum of all items in the tuple.          | `sum(my_tuple)`                  |
| `any()`        | Returns True if any item is True, otherwise False.  | `any(my_tuple)`                  |
| `all()`        | Returns True if all items are True, otherwise False.| `all(my_tuple)`                  |
| `sorted()`     | Returns a sorted list from the tuple.               | `sorted(my_tuple)`                |
| `index()`      | Returns the index of the first occurrence of an item.| `my_tuple.index(2)`              |
| `count()`      | Returns the number of times an item appears in the tuple.| `my_tuple.count(1)`           |

### Example Usage
```python
my_tuple = (3, 1, 2)
print(len(my_tuple))          # Outputs: 3
print(max(my_tuple))          # Outputs: 3
print(min(my_tuple))          # Outputs: 1
new_tuple = tuple([4, 5])     # Converts list to tuple: (4, 5)
print(sum(my_tuple))          # Outputs: 6
print(any((0, 1, 2)))         # Outputs: True
print(all((1, 2, 3)))         # Outputs: True
print(sorted(my_tuple))       # Outputs: [1, 2, 3]
print(my_tuple.index(2))      # Outputs: 2
print(my_tuple.count(1))      # Outputs: 1
```




### Functions of Dictionary

| Function          | Description                                                  | Example                                 |
|-------------------|--------------------------------------------------------------|-----------------------------------------|
| `clear()`         | Removes all elements from the dictionary.                   | `my_dict.clear()`                       |
| `copy()`          | Returns a shallow copy of the dictionary.                   | `new_dict = my_dict.copy()`            |
| `fromkeys()`      | Creates a new dictionary with specified keys and a value.  | `dict.fromkeys(['a', 'b'], 0)`        |
| `get()`           | Returns the value of a specified key.                       | `my_dict.get('key1')`                  |
| `items()`         | Returns a view of the dictionary's key-value pairs.         | `my_dict.items()`                      |
| `keys()`          | Returns a view of the dictionary's keys.                    | `my_dict.keys()`                       |
| `pop()`           | Removes and returns the value of the specified key.         | `value = my_dict.pop('key1')`         |
| `popitem()`       | Removes and returns the last inserted key-value pair.       | `last_item = my_dict.popitem()`       |
| `setdefault()`    | Returns the value of a specified key, or inserts it.        | `my_dict.setdefault('new_key', 1)`    |
| `update()`        | Updates the dictionary with specified key-value pairs.      | `my_dict.update({'key2': 2})`        |
| `values()`        | Returns a view of all values in the dictionary.             | `my_dict.values()`                     |
| `cmp()`           | Compares two dictionaries (not available in Python 3).      | `cmp(dict1, dict2)`                   |

### Example Usage
```python
my_dict = {'a': 1, 'b': 2}
my_dict.clear()               # Clears the dictionary
my_dict = {'a': 1, 'b': 2}
new_dict = my_dict.copy()     # Creates a copy of my_dict
default_dict = dict.fromkeys(['x', 'y'], 0)  # Creates {'x': 0, 'y': 0}
value = my_dict.get('a')      # Outputs: 1
key_list = my_dict.keys()     # Outputs: dict_keys(['a', 'b'])
items_list = my_dict.items()   # Outputs: dict_items([('a', 1), ('b', 2)])
removed_value = my_dict.pop('a')  # Outputs: 1, my_dict becomes {'b': 2}
last_item = my_dict.popitem() # Outputs: ('b', 2)
my_dict.setdefault('c', 3)    # Adds 'c': 3 if 'c' is not in my_dict
my_dict.update({'b': 4})      # Updates the value of 'b'
value_list = my_dict.values()  # Outputs: dict_values([4, 3])
```



### Functions of Set

| Function                     | Description                                                      | Example                                  |
|------------------------------|------------------------------------------------------------------|------------------------------------------|
| `add(element)`               | Adds an element to the set.                                     | `my_set.add(3)`                         |
| `clear()`                    | Removes all elements from the set.                              | `my_set.clear()`                        |
| `copy()`                     | Returns a shallow copy of the set.                              | `new_set = my_set.copy()`               |
| `difference(other_set)`      | Returns a set with elements in the current set but not in the other. | `my_set.difference(other_set)`         |
| `difference_update(other_set)`| Removes elements found in another set.                          | `my_set.difference_update(other_set)`  |
| `discard(element)`           | Removes the specified item if present, does nothing if not.     | `my_set.discard(2)`                     |
| `intersection(other_set)`    | Returns a set with elements common to both sets.                | `my_set.intersection(other_set)`       |
| `intersection_update(other_set)`| Retains only elements found in both sets.                     | `my_set.intersection_update(other_set)` |
| `isdisjoint(other_set)`      | Returns True if no elements are common to both sets.           | `my_set.isdisjoint(other_set)`         |
| `issubset(other_set)`        | Returns True if all elements of the set are in another set.    | `my_set.issubset(other_set)`           |
| `issuperset(other_set)`      | Returns True if this set contains all elements of another set.  | `my_set.issuperset(other_set)`         |
| `pop()`                      | Removes and returns an arbitrary element from the set.          | `element = my_set.pop()`                |
| `remove(element)`            | Removes the specified element; raises an error if not found.    | `my_set.remove(2)`                      |
| `symmetric_difference(other_set)`| Returns a set with elements in either set but not in both.  | `my_set.symmetric_difference(other_set)`|
| `symmetric_difference_update(other_set)`| Updates the set with symmetric difference of both sets. | `my_set.symmetric_difference_update(other_set)` |
| `union(other_set)`           | Returns a set with all elements from both sets.                 | `my_set.union(other_set)`               |
| `update(other_set)`          | Updates the set with elements from another set or iterable.     | `my_set.update(other_set)`              |

### Example Usage
```python
my_set = {1, 2, 3}
my_set.add(4)                           # Adds 4
my_set.clear()                          # Clears the set
my_set = {1, 2, 3}                      # Reinitialize set
new_set = my_set.copy()                 # Creates a copy
diff_set = my_set.difference({2, 3})    # {1}
my_set.difference_update({2, 3})        # my_set becomes {1}
my_set.discard(2)                       # Does nothing as 2 is not present
inter_set = my_set.intersection({1, 4}) # {1}
my_set.intersection_update({1, 2})      # my_set remains {1}
is_disjoint = my_set.isdisjoint({2, 3}) # True
is_subset = my_set.issubset({1, 2})     # False
is_superset = my_set.issuperset({1})    # True
removed_element = my_set.pop()          # Removes and returns an element
my_set.remove(1)                        # Removes 1
symmetric_diff = my_set.symmetric_difference({2, 3}) # {2, 3}
my_set.symmetric_difference_update({2, 3}) # my_set becomes {2, 3}
union_set = my_set.union({4, 5})        # {2, 3, 4, 5}
my_set.update({6, 7})                   # my_set becomes {2, 3, 6, 7}
```
## 19. Explain Type Conversion in Python.  [(int(), float(), ord(), oct(), str() etc.)]


### Type Conversion Functions in Python

| Function   | Description                                                    | Example                     |
|------------|---------------------------------------------------------------|-----------------------------|
| `int()`    | Converts a value to an integer.                              | `int('10')` returns `10`   |
| `float()`  | Converts a value to a floating-point number.                 | `float('10.5')` returns `10.5` |
| `oct()`    | Converts an integer to its octal representation (as a string).| `oct(8)` returns `'0o10'`  |
| `hex()`    | Converts an integer to its hexadecimal representation (as a string). | `hex(255)` returns `'0xff'` |
| `ord()`    | Returns the Unicode code point of a character.               | `ord('A')` returns `65`    |
| `chr()`    | Converts an integer (Unicode code point) to its corresponding character. | `chr(65)` returns `'A'`    |
| `eval()`   | Evaluates a string expression as a Python expression.        | `eval('3 + 5')` returns `8` |
| `str()`    | Converts a value to a string.                                | `str(10)` returns `'10'`   |
| `repr()`   | Returns a string representation of a value, useful for debugging. | `repr([1, 2, 3])` returns `'[1, 2, 3]'` |

### Example Usage
```python
# Using int()
print(int('42'))          # Output: 42

# Using float()
print(float('3.14'))     # Output: 3.14

# Using oct()
print(oct(10))           # Output: '0o12'

# Using hex()
print(hex(255))          # Output: '0xff'

# Using ord() and chr()
print(ord('A'))          # Output: 65
print(chr(65))           # Output: 'A'

# Using eval()
print(eval('2 + 3'))     # Output: 5

# Using str()
print(str(100))          # Output: '100'

# Using repr()
print(repr('Hello'))     # Output: "'Hello'"
```

## 20 Open and With Statement in Python

#### `open()` Statement
- Opens a file and returns a file object.
- Requires manual closing with `f.close()`.

**Example:**
```python
f = open("nitin.txt", "r")  # Open file
content = f.read()           # Read content
print(content)               # Print content
f.close()                    # Close file
```

#### `with` Statement
- Automatically handles closing the file.
- Cleaner and safer syntax.

**Example:**
```python
with open("nitin.txt", "r") as f:  # Open file
    content = f.read()               # Read content
    print(content)                   # Print content
# File is closed automatically
```

### Benefits of `with`
- **Automatic closing**: No need for `f.close()`.
- **Cleaner code**: Reduces errors and improves readability.


## 22. Different Ways To Read And Write In A File In Python?

### Different Ways to Read and Write Files in Python

#### Syntax
```python
file_object = open("filename", "mode")
```

### File Modes

1. **Read Only (`'r'`)**
   - Opens a file for reading.
   - Default mode.
   - Raises error if the file doesn't exist.

   **Example:**
   ```python
   with open("file.txt", "r") as f:
       content = f.read()
   ```

2. **Read and Write (`'r+'`)**
   - Opens a file for both reading and writing.
   - Raises error if the file doesn't exist.

   **Example:**
   ```python
   with open("file.txt", "r+") as f:
       content = f.read()
       f.write("New line")
   ```

3. **Write Only (`'w'`)**
   - Opens a file for writing.
   - Truncates existing file or creates a new one.

   **Example:**
   ```python
   with open("file.txt", "w") as f:
       f.write("Hello, World!")
   ```

4. **Write and Read (`'w+'`)**
   - Opens a file for both writing and reading.
   - Truncates existing file.

   **Example:**
   ```python
   with open("file.txt", "w+") as f:
       f.write("Hello!")
       f.seek(0)  # Move to the beginning
       content = f.read()
   ```

5. **Append Only (`'a'`)**
   - Opens a file for writing at the end.
   - Creates a new file if it doesn’t exist.

   **Example:**
   ```python
   with open("file.txt", "a") as f:
       f.write("Adding a new line.")
   ```

6. **Append and Read (`'a+'`)**
   - Opens a file for both appending and reading.

   **Example:**
   ```python
   with open("file.txt", "a+") as f:
       f.write("Another line.")
       f.seek(0)  # Move to the beginning
       content = f.read()
   ```

7. **Exclusive Creation (`'x'`)**
   - Creates a file for writing but raises an error if it already exists.

   **Example:**
   ```python
   with open("file.txt", "x") as f:
       f.write("New file created.")
   ```

8. **Binary Mode (`'b'`)**
   - Opens the file in binary mode. Can be appended to other modes.

   **Example:**
   ```python
   with open("file.bin", "wb") as f:
       f.write(b"Binary data")
   ```

### Text Mode (`'t'`)
- Default mode; translates line endings.
- Can be used with other modes like `'rt'`, `'wt'`.





## 24. How Exception Handled In Python?


### Example

```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
except ValueError:
    print("That's not a valid number!")
except ZeroDivisionError:
    print("You can't divide by zero!")
else:
    print("Result is:", result)
finally:
    print("Execution complete.")
```

### Summary
- Use `try` to wrap code that may fail.
- Use `except` to handle specific exceptions.
- Use `else` for code that should run when no exceptions occur.
- Use `finally` for cleanup code that should run always.

## 30. Difference Between Abstraction and Encapsulation.


| Aspect               | Abstraction                                  | Encapsulation                              |
|----------------------|----------------------------------------------|-------------------------------------------|
| **Level**            | Design level                                 | Application level                          |
| **Purpose**          | Hides unnecessary details; shows relevant data | Hides both code and data from outside use |
| **Focus**            | What an object does                          | How an object works                       |
| **Example**          | Using a car without knowing its engine details | A car's internal mechanics hidden from the user |
| **Implementation**   | Achieved using interfaces and abstract classes | Achieved using access modifiers (private, public) |
| **Summary**          | Hides implementation details                 | Hides data and ensures controlled access  |




## 31. Does Python Support Multiple Inheritance. (Diamond Problem)

Diamond Problem
The diamond problem arises when two parent classes inherit from the same base class, leading to ambiguity. For instance, if both parent classes have a method with the same name, Python needs to determine which method to use when called from the child class.

Example:

Class A is the base class.
Class B and Class C both inherit from Class A.
Class D inherits from both Class B and Class C.
When you call a method from Class D, Python follows a specific order (Method Resolution Order or MRO) to determine which method to execute, usually starting from the leftmost parent.

```
class A:
    def abc(self):
        print("a")  # Method in base class A

class B(A):
    def abc(self):
        print("b")  # Overridden method in class B

class C(A):
    def abc(self):
        print("c")  # Overridden method in class C

class D(B, C):
    pass  # Class D inherits from B and C

# Creating an instance of class D
d = D()
d.abc()  # Calling the abc() method
````

## 32. How to initialize Empty List, Tuple, Dict and Set?

- **List:** `empty_list = []`
- **Tuple:** `empty_tuple = ()`
- **Dictionary:** `empty_dict = {}`
- **Set:** `empty_set = set()`


## 34. How Slicing Works In String Manipulation. Explain.

### Slicing in String Manipulation



### Example with String `s = 'HelloWorld'`



| Index    | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 |
|----------|---|---|---|---|---|---|---|---|---|---|
| Letters  | H | E | L | L | O | W | O | R | L | D |
| Index (-)| -10 | -9 | -8 | -7 | -6 | -5 | -4 | -3 | -2 | -1 |


```python
s = 'HelloWorld'

# Full string
print(s[:])        # Output: HelloWorld

# Full string with step
print(s[::])       # Output: HelloWorld

# Slice from start to index 5 (exclusive)
print(s[:5])       # Output: Hello

# Slice from index 2 to 5 (exclusive)
print(s[2:5])      # Output: llo

# Slice from index 2 to 8 with step 2
print(s[2:8:2])    # Output: loo

# Slice from index 8 to 1 (reverse)
print(s[8:1:-1])   # Output: lroWoll

# Slice using negative indices
print(s[-4:-2])    # Output: or

# Reverse the string
print(s[::-1])     # Output: dlroWolleH
```

### Breakdown of Examples:

1. **`s[:]`**: Returns the entire string.
2. **`s[::]`**: Also returns the entire string, specifying a step of 1.
3. **`s[:5]`**: Extracts characters from the start up to index 5 (not including it).
4. **`s[2:5]`**: Extracts characters from index 2 to 5.
5. **`s[2:8:2]`**: Extracts every second character from index 2 to 8, resulting in 'loo'.
6. **`s[8:1:-1]`**: Extracts characters in reverse order, starting from index 8 down to index 1.
7. **`s[-4:-2]`**: Uses negative indexing to extract characters from the end of the string.
8. **`s[::-1]`**: Reverses the string.

## 35. Can You Concatenate Two Tuples. If Yes, How Is It Possible?  Since it is Immutable?

```python
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)

# Concatenating tuples
result = tuple1 + tuple2

print(result)  # Output: (1, 2, 3, 4, 5, 6)
```

### Explanation:

- `tuple1` and `tuple2` are two separate tuples.
- The expression `tuple1 + tuple2` creates a new tuple that includes all elements from `tuple1` followed by all elements from `tuple2`.
- The original tuples remain unchanged, demonstrating that tuples are immutable.


## 36 Why Tuple Is Immutable and List Is Mutable?

- **Tuples are immutable**: Once created, their elements cannot be changed, making them memory-efficient and faster for fixed data.
- **Lists are mutable**: They can be modified, allowing for dynamic data handling and flexibility.

## 37. Difference Between Python Arrays and Lists

| **Feature**                          | **List**                                         | **Array**                                   |
|--------------------------------------|--------------------------------------------------|---------------------------------------------|
| **Data Type**                        | Can store different types of values              | Consists of the same type of values        |
| **Arithmetic Operations**            | Cannot handle direct arithmetic operations        | Can handle arithmetic operations directly   |
| **Import Requirement**               | Built-in data structure, no import needed        | Requires import (e.g., `from array import array`) |
| **Compatibility**                    | Less compatible for storing data                  | More compatible for data storage           |
| **Memory Consumption**               | Consumes more memory                             | More compact in memory size                 |
| **Data Length**                      | Suitable for longer sequences                     | Suitable for shorter sequences               |
| **Printing**                         | Requires explicit looping to print                | Can print without explicit looping          |


## 37. What Is _a, __a,  __a__ in Python?

Sure! Here’s the structured explanation:

### _a (Single Underscore)
- **Purpose**: Indicates a protected member intended for internal use.
- **Usage**: Signifies "private" but not strictly enforced (weak private).
- **Example**: `_variable` suggests it’s for internal use only.

### __a (Double Underscore)
- **Purpose**: Triggers name mangling to avoid conflicts in subclasses.
- **Mechanism**: Python modifies the variable name to include the class name (e.g., `_ClassName__a`).
- **Usage**: Prevents direct access from outside the class, making it more private.
- **Example**: `__variable` is meant to be used only within the class.

### __a__ (Dunder Methods)
- **Purpose**: Special methods with predefined behaviors in Python.
- **Functionality**: Used for operator overloading and defining behaviors (like `__init__`, `__str__`).
- **Usage**: Helps Python differentiate between user-defined functions and built-in functions.
- **Example**: `__init__()` initializes a class instance.


## 38. How To Read Multiple Values From Single Input?

### 1. Using `map()`
```python
x = list(map(int, input("Enter multiple values: ").split()))
```
- **Input**: `10 20 30`
- **Output**: `List of Values: [10, 20, 30]`
- **Explanation**: Converts space-separated input into a list of integers.

### 2. Using List Comprehension
```python
x = [int(x) for x in input("Enter multiple values: ").split()]
```
- **Input**: `40 50 60`
- **Output**: `Number of list is: [40, 50, 60]`
- **Explanation**: Creates a list of integers from space-separated input.

### 3. Using Commas as Delimiters
```python
x = [int(x) for x in input("Enter multiple values: ").split(",")]
```
- **Input**: `70,80,90`
- **Output**: `Number of list is: [70, 80, 90]`
- **Explanation**: Converts comma-separated input into a list of integers.

## 39. How To Copy and Delete A Dictionary

### Copying a Dictionary

1. **Using the `copy()` Method**
   ```python
   original_dict = {'a': 1, 'b': 2}
   copied_dict = original_dict.copy()
   ```
   - **Explanation**: Creates a shallow copy of the dictionary.

2. **Using the `dict()` Constructor**
   ```python
   copied_dict = dict(original_dict)
   ```
   - **Explanation**: Also creates a shallow copy of the dictionary.

3. **Using Dictionary Comprehension**
   ```python
   copied_dict = {key: value for key, value in original_dict.items()}
   ```
   - **Explanation**: Creates a new dictionary with the same key-value pairs.

### Deleting a Dictionary

1. **Using the `del` Statement**
   ```python
   del original_dict
   ```
   - **Explanation**: Deletes the entire dictionary.

2. **Using the `pop()` Method**
   ```python
   value = original_dict.pop('a')
   ```
   - **Explanation**: Removes the specified key and returns its value.

3. **Using the `clear()` Method**
   ```python
   original_dict.clear()
   ```
   - **Explanation**: Removes all items from the dictionary but keeps the dictionary itself.

### Summary
- You can copy a dictionary using `copy()`, `dict()`, or comprehension.
- You can delete a dictionary with `del`, remove specific items with `pop()`, or clear all items with `clear()`.


## 43. How Class and Object Created in Python?



- **Class**: A blueprint for creating objects.
  ```python
  class MyClass:
      x = 5
  ```

- **Object**: An instance of a class.
  ```python
  obj = MyClass()  # Create an object
  print(obj.x)    # Access the class attribute
  ```

## 44. Explain Namespace and Its Types in Python.

A **namespace** is a way to keep track of variable names and their values in Python, preventing naming conflicts.

#### Types of Namespaces:

1. **Built-in Namespace**: Contains built-in functions and exceptions (e.g., `print()`, `len()`).

2. **Global Namespace**: Holds names defined at the main module level; lasts until the module ends.

3. **Local Namespace**: Created inside functions, containing names local to that function.

4. **Enclosing Namespace**: Refers to names in enclosing functions, useful in nested functions.

### Key Point:
Namespaces help manage names and avoid conflicts in your code.


## 45. Explain Recursion by Reversing a List.

### Recursion: Reversing a List

**Concept**: Recursion is when a function calls itself.

**Code**:
```python
def reverseList(lst):
    if not lst:  # Base case: empty list
        return []
    return [lst[-1]] + reverseList(lst[:-1])  # Recursive case

print(reverseList([1, 2, 3, 4, 5]))  # Output: [5, 4, 3, 2, 1]
```

### Explanation:
- **Base Case**: If the list is empty, return an empty list.
- **Recursive Case**: Return the last element and call the function on the rest of the list.

### Result:
- It outputs the reversed list: `[5, 4, 3, 2, 1]`.





### 48 Using `map()`, `filter()`, and `reduce()` in Python

1. **`map()`**:
   - **Purpose**: Apply a function to all items in an iterable (like a list).
   - **Syntax**: `map(function, iterable)`

   **Example**:
   ```python
   numbers = [1, 2, 3, 4]
   squares = list(map(lambda x: x ** 2, numbers))
   print(squares)  # Output: [1, 4, 9, 16]
   ```

2. **`filter()`**:
   - **Purpose**: Filter items in an iterable based on a function that returns `True` or `False`.
   - **Syntax**: `filter(function, iterable)`

   **Example**:
   ```python
   numbers = [1, 2, 3, 4]
   evens = list(filter(lambda x: x % 2 == 0, numbers))
   print(evens)  # Output: [2, 4]
   ```

3. **`reduce()`**:
   - **Purpose**: Apply a function cumulatively to the items of an iterable, reducing it to a single value.
   - **Syntax**: `from functools import reduce`
   ```python
   reduce(function, iterable)
   ```

   **Example**:
   ```python
   from functools import reduce
   numbers = [1, 2, 3, 4]
   product = reduce(lambda x, y: x * y, numbers)
   print(product)  # Output: 24
   ```

### Summary:
- **`map()`**: Transforms each item.
- **`filter()`**: Selects items that meet a condition.
- **`reduce()`**: Aggregates items to a single result.





### 48. Difference Between Shallow Copy and Deep Copy

1. **Shallow Copy**:
   - Copies the object, but only references to nested objects.
   - Changes to nested objects affect both the original and the copy.
   - Created with `copy()` or `copy.copy()`.
   - **Example**: 
     ```python
     import copy
     original = [1, 2, [3, 4]]
     shallow_copied = copy.copy(original)
     shallow_copied[2][0] = 'Changed'
     print(original)  # Output: [1, 2, ['Changed', 4]]
     ```

2. **Deep Copy**:
   - Copies the object and all nested objects recursively.
   - Changes to nested objects do not affect the original.
   - Created with `copy.deepcopy()`.
   - **Example**:
     ```python
     import copy
     original = [1, 2, [3, 4]]
     deep_copied = copy.deepcopy(original)
     deep_copied[2][0] = 'Changed'
     print(original)  # Output: [1, 2, [3, 4]]
     ```

### Summary:
- **Shallow Copy**: Shared references; changes affect both.
- **Deep Copy**: Independent copies; changes do not affect the original.



## 51. What is Operator Overloading & Dunder Method.

**Operator Overloading**:
- Lets you define how operators (like +, -, *) work with your custom objects.
- Makes your classes easier to use and understand.

**Dunder Methods**:
- Special methods with double underscores (e.g., `__init__`, `__add__`).
- Used for operator overloading and to customize behavior.

### Examples of Dunder Methods:
- `__add__(self, other)`: For the `+` operator.
- `__sub__(self, other)`: For the `-` operator.
- `__mul__(self, other)`: For the `*` operator.

### Summary:
- **Operator Overloading**: Customize how operators work with your classes.
- **Dunder Methods**: Special methods that help implement this functionality.