# Advanced Programming Using Python
### Introduction - Python
- Created by **Guido van Rossum** in 1991
- Open Source, Free
- Simple and readable
- Minimalist
- Cross-Platform compatible
- Dynamically Typed variables
- Object-Oriented
- High-level, interpreted

---

### Execution of Programming Languages
Translates source code into machine code:
- **Compiler**: Translation before program is run (e.g., C, C++, C#)
- **Interpreter**: Translation line-by-line, executing each line as it goes (e.g., Python, Javascript, Ruby, PHP)
- **Hybrid / JIT**: Translation to bytecode, interpretation at runtime by JVM (e.g., Java)

---

### Compiler vs Interpreter

| Compiled Languages | Interpreted Languages |
|--------------------|-----------------------|
| Translate directly to machine code | Translation and execution on the fly |
| Needs entire program | Line by line execution |
| Can start executing as soon as it starts reading | Creates an executable, native and fast |
| Usually statically typed | Usually dynamically typed |
| Ideal for compute-heavy and efficiency-intensive tasks | Ideal for small tasks |

**Examples**: 
- Compiled: C, C++, FORTRAN
- Interpreted: Python, Perl, PHP, Bash

---

### Python Applications
- Data Visualization
- Solve Complex Math Problems
- Graphics
- AI Applications
- Building Websites

---

### Words of the author!!
“Python is an experiment in how much freedom programmers need. Too much freedom and nobody can read another’s code; too little and expressiveness is endangered.”  
— *Guido van Rossum*

---

---

### Python Basics (mainExplain1.py, mainExplain2.py)
- Indentation
- Case sensitive
- `__main__`

---

### Datatypes
- Fundamental datatypes
- Custom Types - Classes
- Specialized types - Modules
- None

---

### Fundamental Datatypes (Variables.py)
| Type                  | Examples               |
|-----------------------|------------------------|
| Numeric Types         | Integer, Float, Complex|
| Mapping Type          | Dictionary             |
| Sequence Types        | String, List, Tuple    |
| Set Types             | Set, Frozen set        |
| Boolean Type          | True, False            |
| None Type             | None (null)            |

---

### Binary Types (Variables.py)
Variables are placeholders that allow you to store, modify, and retrieve data during execution of a program.

- **Variable Assignment**
- **Dynamic Typing**
- **Reassigning Variables**
- **Multiple Assignments**
- **Constants**
- **Dunder Variables**

---

### Naming Conventions
- Variable names must start with a letter or an underscore (_), but not a number.
- Can contain letters, numbers, and underscores (_).
- Case-sensitive: `myVar` and `myvar` are different.
- Avoid using Python keywords (like `if`, `for`, `while`) as variable names.

---

### Hands on
**Assignment 1**: Declare variables of integer, float, boolean, and string type and print their values.

```python
# Assignment 1 Solution
integer_var = 10
float_var = 10.5
boolean_var = True
string_var = "Hello, Python!"

print("Integer:", integer_var)
print("Float:", float_var)
print("Boolean:", boolean_var)
print("String:", string_var)
```

**Assignment 2**: Swap values.

```python
# Assignment 2 Solution
a = 5
b = 10
print("Before swap: a =", a, "b =", b)
a, b = b, a
print("After swap: a =", a, "b =", b)
```

---

### Operators (Operators.py)
Special symbols or keywords used to perform operations on variables and values:
- **Arithmetic Operators**: `+, -, *, /, %, //, **`
- **Assignment Operators**: `=, +=, -=, *=, /=, %=, **=, //=`
- **Bitwise Operators**: `&, |, ^, ~, <<, >>`
- **Logical Operators**: `and, or, not`
- **Comparison Operators**: `==, !=, >, <, >=, <=`
- **Membership Operators**: `in, not in`
- **Identity Operators**: `is, is not`
- **Ternary Operator**: `'value_if_true' if condition else 'value_if_false'`

---

### Hands on
**Assignment 3**: Try out Arithmetic and Assignment operators.

```python
# Assignment 3 Solution
x = 10
y = 5
print("Addition:", x + y)
print("Subtraction:", x - y)
print("Multiplication:", x * y)
print("Division:", x / y)
```

---

### Input/output from console (inputOutput.py)
Interface between end users and programs:
- **Input**: `input("prompt")`
- **Output**: `print("....")`
- Custom separators: `sep`
- Custom endings: `end`
- Formatted output: `format()` or f-strings
- Truncate a float number to 2 decimal places: `{var_name:.2f}`

---

### Hands on
**Assignment 4**: Accept 2 strings from user and print them with format and f-strings.

```python
# Assignment 4 Solution
str1 = input("Enter first string: ")
str2 = input("Enter second string: ")
print("Using format:", "{} and {}".format(str1, str2))
print(f"Using f-string: {str1} and {str2}")
```

---

### Type Casting (inputOutput.py)
Process of converting one datatype to another:
- `int()`
- `float()`
- `str()`
- `bool()`
- `list()`
- `tuple()`
- `set()`
- `dict()`

## Type Casting Example
```
num_str = "42.5"        # A string representing a float
num_float = float(num_str)  # Convert string to float
num_int = int(num_float)     # Convert float to intege
```
---

### Hands on
**Assignment 5**: Accept 2 numbers from user, add them, and print the result.

```python
# Assignment 5 Solution
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
result = num1 + num2
print("The sum is:", result)
```

**Assignment 6**: Add an integer and a float, print result and type of result.

```python
# Assignment 6 Solution
integer_num = 5
float_num = 10.5
result = integer_num + float_num
print("Result:", result)
print("Type of result:", type(result))
```

**Assignment 7**: Accept a float value from console, typecast it to float, and print its square.

```python
# Assignment 7 Solution
float_value = float(input("Enter a float value: "))
print("Square of the value is:", float_value ** 2)
```

**Assignment 8**: Add a string and a number, print result and type of result.

```python
# Assignment 8 Solution
string_num = "10"
number = 5
result = string_num + str(number)
print("Result:", result)
print("Type of result:", type(result))
```

---

### Hands on
**Assignment 9**: Calculate the area of a circle – constant PI = 3.14.

```python
# Assignment 9 Solution
radius = float(input("Enter the radius of the circle: "))
PI = 3.14
area = PI * radius ** 2
print("Area of the circle:", area)
```

**Assignment 10**: Calculate savings of a person.

```python
# Assignment 10 Solution
monthly_income = float(input("Enter your monthly income: "))
monthly_expenses = float(input("Enter your total monthly expenses: "))

savings = monthly_income - monthly_expenses
percentage_saved = (savings / monthly_income) * 100
percentage_spent = (monthly_expenses / monthly_income) * 100

print("Total savings:", savings)
print("Percentage of income saved: {:.2f}%".format(percentage_saved))
print("Percentage of income spent: {:.2f}%".format(percentage_spent))
```

---

### Conditional Statements (ifElseControlStructure.py), (elif.py), (nestedifElse.py)
Fundamental control structure used to make decisions based on conditions:
- **If-else condition**
- **If-elif condition**
- **Nested if-else condition**

---

### Hands on
**Assignment 11**: Write a program to check if a

 number is positive, negative, or zero.

```python
# Assignment 11 Solution
number = float(input("Enter a number: "))
if number > 0:
    print("The number is positive.")
elif number < 0:
    print("The number is negative.")
else:
    print("The number is zero.")
```

---

### Homework Assignments
**Assignment 1**: Convert inches to feet, meters, and centimeters until user wishes to stop.

```python
# Homework Assignment 1 Solution
while True:
    inches = float(input("Enter inches (or type '0' to exit): "))
    if inches == 0:
        break
    feet = inches / 12
    meters = inches * 0.0254
    centimeters = inches * 2.54
    print(f"{inches} inches is equal to {feet} feet, {meters} meters, and {centimeters} centimeters.")
```

---

**Assignment 2**: Build a calculator using if-else for +, -, *, / operations.

```python
# Homework Assignment 2 Solution
def calculator():
    operation = input("Enter operation (+, -, *, /): ")
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))

    if operation == '+':
        print(f"{num1} + {num2} = {num1 + num2}")
    elif operation == '-':
        print(f"{num1} - {num2} = {num1 - num2}")
    elif operation == '*':
        print(f"{num1} * {num2} = {num1 * num2}")
    elif operation == '/':
        if num2 != 0:
            print(f"{num1} / {num2} = {num1 / num2}")
        else:
            print("Cannot divide by zero.")
    else:
        print("Invalid operation.")

calculator()
```

---



# **Hands-On Assignments**

## **Assignment 1: Sum of Digits**
**Objective:** Write a program to calculate the sum of the digits of a given positive integer.

### **Instructions:**
- **Input:** Prompt the user to enter a positive integer.
- **Logic:** Use a `for` loop to iterate through each digit of the number and calculate the sum.
- **Output:** Display the sum of the digits.

### **Code:**
```python
# Assignment 1: Sum of Digits
num = int(input("Enter a positive integer: "))
sum_of_digits = 0

for digit in str(num):
    sum_of_digits += int(digit)

print("Sum of the digits:", sum_of_digits)
```

---

## **Assignment 2: Multiplication Table**
**Objective:** Write a program to generate and display the multiplication table of a given number up to 12.

### **Instructions:**
- **Input:** Prompt the user to enter a number.
- **Logic:** Use a `for` loop to calculate and display the multiplication table for the number.
- **Output:** Display the multiplication table.

### **Code:**
```python
# Assignment 2: Multiplication Table
number = int(input("Enter a number: "))

print(f"Multiplication Table for {number}:")
for i in range(1, 13):
    print(f"{number} x {i} = {number * i}")
```

---

## **Assignment 3: ATM Withdrawal Process**
**Objective:** Develop a program that simulates an ATM withdrawal process.

### **Instructions:**
- **Input:** Prompt the user to enter their account balance and the amount they wish to withdraw.
- **Logic:** 
  - Check if the withdrawal amount is greater than the account balance. If so, display an error message.
  - If the withdrawal amount is valid, subtract it from the balance.
  - Ensure the withdrawal amount is a multiple of 10.
- **Output:** 
  - Display the remaining balance if the withdrawal is successful.
  - If not, display an appropriate error message.
  - Check if the user wishes to withdraw more money; otherwise, exit.

### **Code:**
```python
# Assignment 3: ATM Withdrawal Process
balance = float(input("Enter your account balance: "))

while True:
    withdraw_amount = float(input("Enter amount to withdraw: "))
    
    if withdraw_amount > balance:
        print("Insufficient balance.")
    elif withdraw_amount % 10 != 0:
        print("Amount must be a multiple of 10.")
    else:
        balance -= withdraw_amount
        print("Remaining balance:", balance)

    more = input("Do you want to withdraw more money? (yes/no): ")
    if more.lower() != 'yes':
        break
```

---

## **Assignment 4: Multiplication Tables Using Nested For Loops**
**Objective:** Create multiplication tables for numbers 1–5 using nested `for` loops.

### **Instructions:**
- **Logic:** Use nested `for` loops to generate the multiplication tables for numbers 1 to 5.

### **Code:**
```python
# Assignment 4: Multiplication Tables (Nested For Loops)
for i in range(1, 6):
    print(f"Multiplication table for {i}:")
    for j in range(1, 13):
        print(f"{i} x {j} = {i * j}")
    print()  # Print a newline for better readability
```

---

## **Assignment 5: Triangular Pattern Using Nested While Loop**
**Objective:** Write a program to generate and display a triangular pattern of numbers based on user input using nested `while` loops.

### **Instructions:**
- **Input:** Prompt the user to enter the number of rows for the pattern.
- **Output:** The program should display the pattern in a triangular format.

### **Code:**
```python
# Assignment 5: Triangular Pattern (Nested While Loop)
rows = int(input("Enter the number of rows for the pattern: "))
i = 1

while i <= rows:
    j = 1
    while j <= i:
        print(j, end=' ')
        j += 1
    print()  # Move to the next line after each row
    i += 1
```

---

## **Assignment 6: Calculator Using Match-Case**
**Objective:** Create a calculator for performing addition, subtraction, division, and multiplication operations using match-case.

### **Instructions:**
- **Input:** Ask the user what operation needs to be performed.
- **Logic:** Use match-case to perform the operation.
- **Output:** Ask the user if they want to perform another operation; repeat or exit based on their answer.

### **Code:**
```python
# Assignment 6: Calculator (Match-Case)
def calculator():
    while True:
        operation = input("Enter operation (add, subtract, multiply, divide) or 'exit' to quit: ")
        
        if operation == 'exit':
            break
            
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
        
        match operation:
            case 'add':
                print(f"{num1} + {num2} = {num1 + num2}")
            case 'subtract':
                print(f"{num1} - {num2} = {num1 - num2}")
            case 'multiply':
                print(f"{num1} * {num2} = {num1 * num2}")
            case 'divide':
                if num2 != 0:
                    print(f"{num1} / {num2} = {num1 / num2}")
                else:
                    print("Cannot divide by zero.")
            case _:
                print("Invalid operation.")

calculator()
```

---

