# Input/Output in Python

## Overview
Input/output serves as the interface between end users and programs, allowing for interaction through the console.

## Input
- **Description**: Reads a line of text from the user and returns it as a string.
- **Syntax**: 
  ```python
  user_input = input("Enter something: ")
  ```

## Output
- **Basic Output**: Use `print()` to display text.
  ```python
  print("Hello, World!")
  ```

- **Multiple Arguments**: Print multiple items in one statement.
  ```python
  print("Value 1:", 10, "Value 2:", 20)
  ```

- **Custom Separators**: Use `sep` to change the separator between arguments.
  ```python
  print("Hello", "World", sep=", ")
  ```

- **Custom Endings**: Use `end` to change what is printed at the end.
  ```python
  print("Hello", end="!")  # Output: Hello!
  ```

- **Formatted Output**: Use `format()` or f-strings for formatting.
  ```python
  name = "Alice"
  age = 30
  print("My name is {} and I am {} years old.".format(name, age))
  # or using f-string
  print(f"My name is {name} and I am {age} years old.")
  ```

- **Truncate Float Numbers**: Format float numbers to a specific number of decimal places.
  ```python
  var_name = 3.14159
  print(f"{var_name:.2f}")  # Output: 3.14
  ```


# Conditional Statements in Python



## Key Concepts

### 1. `if` Statement
- **Description**: Executes a block of code if the condition is true.
- **Syntax**:
  ```python
  if condition:
      # Code to execute if condition is true
  ```

### 2. `else` Statement
- **Description**: Executes a block of code if the preceding `if` condition is false.
- **Syntax**:
  ```python
  if condition:
      # Code if condition is true
  else:
      # Code if condition is false
  ```

### 3. `elif` Statement
- **Description**: Allows checking multiple conditions. It stands for "else if."
- **Syntax**:
  ```python
  if condition1:
      # Code if condition1 is true
  elif condition2:
      # Code if condition2 is true
  else:
      # Code if both conditions are false
  ```

### 4. Nested Conditionals
- **Description**: You can place an `if` statement inside another `if` statement.
- **Example**:
  ```python
  if condition1:
      if condition2:
          # Code if both conditions are true
  ```

## Example
```python
age = 20
if age >= 18:
    print("You are an adult.")
elif age >= 13:
    print("You are a teenager.")
else:
    print("You are a child.")
```
Here’s a concise Markdown snippet summarizing loops in Python:


# Loops in Python

## Types of Loops

### 1. For Loop
- **Description**: Executes a block of code a specific number of times, iterating over a sequence (like a list, tuple, string, or range).
- **Syntax**:
  ```python
  for item in sequence:
      # Code to execute for each item
  ```
- **Example**:
  ```python
  for i in range(5):  # Iterates from 0 to 4
      print(i)
  ```

### 2. While Loop
- **Description**: Repeatedly executes a block of code as long as a specified condition is true.
- **Syntax**:
  ```python
  while condition:
      # Code to execute while condition is true
  ```
- **Example**:
  ```python
  count = 0
  while count < 5:
      print(count)
      count += 1
  ```

# Loop Control Statements in Python

## Types of Control Statements

### 1. `break`
- **Description**: Exits the loop completely, terminating further iterations.
- **Usage**: Typically used when a certain condition is met.
- **Example**:
  ```python
  for i in range(10):
      if i == 5:
          break  # Exits the loop when i equals 5
      print(i)
  ```

### 2. `continue`
- **Description**: Skips the current iteration of the loop and proceeds to the next iteration.
- **Usage**: Used when you want to bypass certain conditions within the loop.
- **Example**:
  ```python
  for i in range(5):
      if i == 2:
          continue  # Skips the iteration when i equals 2
      print(i)
  ```


Here’s a concise Markdown snippet summarizing nested loops and the use of `else` clauses in Python:


# Nested Loops in Python

## Types of Nested Loops

### 1. Nested For Loop
- **Description**: A for loop inside another for loop, typically used for iterating over multi-dimensional data structures.
- **Example**:
  ```python
  for i in range(3):  # Outer loop
      for j in range(2):  # Inner loop
          print(f"i: {i}, j: {j}")
  ```

### 2. Nested While Loop
- **Description**: A while loop inside another while loop, useful for repetitive conditions within a larger repetitive structure.
- **Example**:
  ```python
  i = 0
  while i < 3:  # Outer loop
      j = 0
      while j < 2:  # Inner loop
          print(f"i: {i}, j: {j}")
          j += 1
      i += 1
  ```

## Else Clause in Loops
- **Description**: An `else` clause can be added to loops, which executes when the loop terminates normally (not via `break`).
- **Usage**: Useful for actions that should occur after the loop completes.
- **Example**:
  ```python
  for i in range(3):
      print(i)
  else:
      print("Loop finished without interruption.")
  ```
Here’s a concise Markdown snippet summarizing loops with an `else` clause in Python:


# Loops with Else 

### 1. For Loop with Else
- **Description**: The `else` block runs after the loop completes all iterations without encountering a `break`.
- **Example**:
  ```python
  for i in range(5):
      print(i)
  else:
      print("For loop finished without interruption.")
  ```

### 2. While Loop with Else
- **Description**: Similar to the `for` loop, the `else` block runs after the `while` loop completes normally.
- **Example**:
  ```python
  count = 0
  while count < 5:
      print(count)
      count += 1
  else:
      print("While loop finished without interruption.")
  ```

### 3. Using Break with Else
- **Description**: If a `break` statement is encountered, the `else` block will not execute.
- **Example**:
  ```python
  for i in range(5):
      if i == 3:
          break
      print(i)
  else:
      print("This will not print if the loop is broken.")
  ```



