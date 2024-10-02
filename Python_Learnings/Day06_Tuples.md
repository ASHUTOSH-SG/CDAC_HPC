
---

### **Hands-On Assignments**

#### **Assignment 1: Extract Vowels from a List**  
Write a Python program that takes a given list of characters, specifically `['a', 'b', 'c', 'k', 'o', 'z', 'i']`, and extracts the vowels from that list. The program should iterate through the list and identify which characters are vowels, then display those vowels in a new list.

**Solution:**
```python
input_list = ['a', 'b', 'c', 'k', 'o', 'z', 'i']
vowels = [char for char in input_list if char in 'aeiou']
print("Extracted vowels:", vowels)
```

---

### **Tuples**  
A tuple is a data structure in Python that is used to store an ordered collection of elements. Here are some characteristics of tuples:
- **Immutable lists**: Tuples cannot be changed after they are created, making them a stable option for storing data.
- **Ordered**: The items in a tuple have a defined order, which means that the position of each element is fixed.
- **Heterogeneous**: Tuples can store elements of different types, allowing for a diverse collection of data.
- **Memory efficient**: Tuples generally use less memory than lists, which can make them a better choice for large datasets.
- **Faster than lists**: Due to their immutability, tuples can be more efficient in terms of performance compared to lists.

---

### **Tuple Operations**  
In Python, tuples can be manipulated through several operations, which are implemented in the file `TupleFunctions.py`:

- **Defining a Tuple**: Tuples are defined using parentheses. For example, you can create an empty tuple like this:  
  `empty_tuple = ()`

- **Accessing Tuple Elements**: You can access elements in a tuple using indexing. For instance, to access the first element of a tuple named `my_tuple`, you would use:  
  `my_tuple[ind]`

- **Slicing a Tuple**: You can retrieve a specific range of elements from a tuple using slicing. For example:  
  `my_tuple[strtInd:endInd]` retrieves elements from index `strtInd` to `endInd - 1`.

- **Concatenation**: Tuples can be concatenated using the `+` operator, allowing you to join two tuples together.

- **Repetition**: You can repeat the elements of a tuple using the `*` operator, which creates a new tuple with the specified number of repetitions.

- **Membership Testing**: You can check if an element exists within a tuple using the `in` or `not in` keywords.

- **Built-in Methods**: Tuples come with built-in methods such as:
  - **Count**: `my_tuple.count(item)` returns the number of occurrences of `item` in the tuple.
  - **Index**: `my_tuple.index(item)` returns the first index of the specified `item` in the tuple.

- **Tuple Unpacking**: You can unpack the elements of a tuple into individual variables using a syntax like this:  
  `item1, item2, item3 = my_tuple`

- **Nested Tuples**: Tuples can contain other tuples, which can be useful for organizing complex data structures. For example:  
  `nested_tuple = (1, (2, 3), (4, 5, 6))`

- **Converting Tuples to Lists**: You can convert a tuple into a list using the `list()` function.

---

### **Hands-On Assignments (Continued)**

#### **Assignment 2: Tuple Manipulation**  
Write a program that prompts the user to enter a list of elements separated by commas (for example, `10, 20, 30, 40, 50`). The program should convert the input string into a tuple of integers. After conversion, it should perform the following operations and display the results:
1. Print the first element of the tuple.
2. Print the last element of the tuple.
3. Print the tuple excluding the first and last elements, which means you should show a slice of the tuple from the second element to the second-to-last element.
4. Print every second element of the tuple using appropriate slicing techniques.
5. Print the tuple in reverse order using slicing.

**Solution:**
```python
input_str = input("Enter elements separated by commas: ")
input_tuple = tuple(map(int, input_str.split(',')))

print("First element:", input_tuple[0])
print("Last element:", input_tuple[-1])
print("Tuple excluding first and last elements:", input_tuple[1:-1])
print("Every second element:", input_tuple[::2])
print("Reversed tuple:", input_tuple[::-1])
```

---

#### **Assignment 3: Tuple Packing and Unpacking**  
Develop a program that prompts the user to enter their information, specifically their name (as a string) and their age (as an integer). The program should pack these two pieces of information into a single tuple and then unpack the tuple back into individual variables. Finally, display the unpacked variables.

**Solution:**
```python
name = input("Enter your name: ")
age = int(input("Enter your age: "))
info_tuple = (name, age)

# Unpacking
name_unpacked, age_unpacked = info_tuple
print("Packed Tuple:", info_tuple)
print("Unpacked Name:", name_unpacked)
print("Unpacked Age:", age_unpacked)
```

---

#### **Assignment 4: Tuple Statistics**  
Write a program that prompts the user to enter a tuple of integers, separated by commas (for example, `5, 10, 15, 20`). Convert the input string into a tuple of integers, then calculate and display:
- The sum of all elements in the tuple.
- The average of the elements in the tuple.
- The maximum value found in the tuple.
- The minimum value found in the tuple.
- The total number of elements contained in the tuple.

**Solution:**
```python
input_str = input("Enter a tuple of integers separated by commas: ")
num_tuple = tuple(map(int, input_str.split(',')))

total = sum(num_tuple)
average = total / len(num_tuple)
maximum = max(num_tuple)
minimum = min(num_tuple)
count = len(num_tuple)

print(f"Sum: {total}, Average: {average}, Max: {maximum}, Min: {minimum}, Count: {count}")
```

---

#### **Assignment 5: Tuple Sorting and Filtering**  
Create a program that prompts the user to enter a tuple of integers separated by commas (for example, `8, 3, 7, 1, 4`). Convert the input string to a tuple of integers. After conversion, perform the following tasks:
1. Sort the tuple in ascending order.
2. Filter out all elements from the sorted tuple that are greater than a specified threshold, which should be provided by the user.
3. Finally, display both the sorted tuple and the filtered elements.

**Solution:**
```python
input_str = input("Enter a tuple of integers separated by commas: ")
num_tuple = tuple(map(int, input_str.split(',')))

sorted_tuple = sorted(num_tuple)
threshold = int(input("Enter the threshold: "))
filtered_elements = [num for num in sorted_tuple if num <= threshold]

print("Sorted tuple:", sorted_tuple)
print("Filtered elements:", filtered_elements)
```

---

### **Tuples vs Lists**

| **Tuples** | **Lists** |
|------------|-----------|
| Immutable  | Mutable   |
| Used for storing fixed collections of data | Used for storing or manipulating dynamic collections of data |
| Suitable for storing keys in dictionaries | Suitable for returning values from functions |
| Can be used to create data structures like stacks, queues, and matrices | Flexible for modifying contents |
| Syntax: `()` | Syntax: `[]` |

---

### **Functions**  
Functions in Python are defined as blocks of reusable code that perform a specific task. They are essential building blocks in programming and come with several important components:
- **Defining Functions**: You define functions using the `def` keyword.
- **Calling Functions**: Once defined, functions can be called by their name followed by parentheses.
- **Parameters and Arguments**: Functions can take inputs (parameters) and can be provided with specific values (arguments) when called.
- **Return Values**: Functions can return results back to the caller, allowing for data to be processed and reused.

**Benefits of Using Functions**:
- They help organize code into manageable sections.
- Functions make code more readable and understandable.
- They reduce redundancy by allowing code to be reused.
- In Python, functions are first-class objects, meaning they can be passed around as arguments or assigned to variables.

---

### **Hands-On Assignments (Continued)**

#### **Assignment 6: Find Longest Word**  
Create a function called `find_longest_word()` that takes a list of words as an argument and returns the length of the longest word in that list. Your program should prompt the user to input a list of words, then call the function and display the result.

**Solution:**
```python
def find_longest_word(words):
    return max(len(word) for word in words)

words_list = input("Enter a list of words separated by commas: ").split(',')
longest_length = find_longest_word(words_list)
print("Length of the longest word:", longest

_length)
```

---

### **Homework Assignments**

#### **Homework Assignment 1**:  
Develop a simple calculator program that can perform basic mathematical operations such as addition, subtraction, multiplication, and division. Create a separate function for each operation. The program should continuously prompt the user for an operation until they choose to exit. For each operation, prompt the user for the two numbers and then display the result.

**Solution:**  
```python
def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    return x / y

while True:
    operation = input("Enter operation (+, -, *, /) or 'exit' to quit: ")
    
    if operation == 'exit':
        break
    
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))
    
    if operation == '+':
        print("Result:", add(num1, num2))
    elif operation == '-':
        print("Result:", subtract(num1, num2))
    elif operation == '*':
        print("Result:", multiply(num1, num2))
    elif operation == '/':
        print("Result:", divide(num1, num2))
    else:
        print("Invalid operation. Please try again.")
```

---

#### **Homework Assignment 2**:  
Create a program that allows users to repeat specific elements within a tuple. The program should prompt the user to enter a tuple of elements separated by commas, and then ask for an element to repeat and the number of times to repeat it. The program should create a new tuple containing the original elements along with the specified repeated element.

**Solution:**
```python
input_str = input("Enter a tuple of elements separated by commas: ")
original_tuple = tuple(input_str.split(','))

repeat_element = input("Enter the element to repeat: ")
repeat_count = int(input("Enter the number of times to repeat: "))

new_tuple = tuple(original_tuple) + (repeat_element,) * repeat_count
print("Original Tuple:", original_tuple)
print("New Tuple:", new_tuple)
```

---

#### **Homework Assignment 3**:  
Develop a program that extracts all unique words from a user-input paragraph and prints them in alphabetical order. The program should prompt the user for a paragraph of text, split the text into words, and then use a set to find unique words before sorting and displaying them.

**Solution:**
```python
paragraph = input("Enter a paragraph: ")
words = paragraph.split()
unique_words = sorted(set(words))
print("Unique words in alphabetical order:", unique_words)
```

---
