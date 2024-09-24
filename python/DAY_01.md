

### **Introduction to Python**
- Created by Guido van Rossum (1991)
- Open Source, Free, Cross-Platform
- Object-Oriented, Dynamically Typed
- High-level, interpreted

---

### **Python Applications**
- Data Visualization, AI, Web Development
- Solve complex math problems

---

### **Setup**
- Install Python: [Anaconda.com/download](https://www.anaconda.com/download)
- IDE Options: PyCharm, VS Code, Jupyter, IDLE, Spyder

---

### **Test Installation**
#### Code Example:
```python
# Simple test to verify installation
print("Hello, World!")  # Prints Hello World
```

---

### **Python Basics**
- Indentation matters
- Case sensitive
- \_\_main\_\_

---

### **Assignment 1**
- **Declare Variables and Print Them**

#### Code Example:
```python
# Declare and print variables
my_int = 10  # Integer
my_float = 3.14  # Float
my_bool = True  # Boolean
my_str = "Hello"  # String

print(my_int, my_float, my_bool, my_str)  # Print values
```

---

### **Assignment 2**
- **Swap Values**

#### Code Example:
```python
# Swap values of two variables
a, b = 5, 10  # Assign initial values
a, b = b, a  # Swap values

print(a, b)  # Output will be 10, 5
```

---

### **Assignment 3**
- **Arithmetic and Assignment Operators**

#### Code Example:
```python
# Arithmetic operations
x = 10
y = 5
print(x + y, x - y, x * y, x / y)  # +, -, *, /

# Assignment operations
x += 1  # Increment x by 1
print(x)  # x is now 11
```

---

### **Assignment 4**
- **Input and Output (Formatted Strings)**

#### Code Example:
```python
# Input from user and formatted output
name = input("Enter your name: ")  # Get input
age = int(input("Enter your age: "))  # Convert input to integer

print(f"My name is {name} and I am {age} years old.")  # Formatted string
```

---

### **Assignment 5**
- **Add Two Numbers**

#### Code Example:
```python
# Accept two numbers and add
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))

result = num1 + num2  # Add numbers
print(f"The sum is {result}")  # Print result
```

---

### **Assignment 9**
- **Calculate Area of a Circle**

#### Code Example:
```python
# Calculate area of a circle
PI = 3.14
radius = float(input("Enter radius: "))  # Get radius from user

area = PI * radius ** 2  # Area formula
print(f"Area of the circle is {area}")  # Display area
```

### **Conditional Statements**
- **if, elif, else**: Used for decision making

---

### **Assignment 11**
- **Comparison Operators**

#### Code Example:
```python
# Use of comparison operators
x = 10
y = 20

print(x == y)  # False
print(x != y)  # True
print(x > y)   # False
```

---

### **Assignment 12**
- **Build a Calculator (+, -, *, /)**

#### Code Example:
```python
# Simple calculator using if-else
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
operation = input("Enter operation (+, -, *, /): ")

if operation == '+':
    result = num1 + num2
elif operation == '-':
    result = num1 - num2
elif operation == '*':
    result = num1 * num2
elif operation == '/':
    result = num1 / num2
else:
    result = "Invalid operation"

print(f"Result: {result}")  # Output the result
```

---

### **Assignment 13**
- **Ticket Price Based on Age**

#### Code Example:
```python
# Determine ticket price based on age
age = int(input("Enter your age: "))

if age < 5:
    price = 0  # Free
elif 5 <= age <= 12:
    price = 5
elif 13 <= age <= 60:
    price = 10
else:
    price = 7

print(f"Ticket price: Rs {price}")
```

---

### **Assignment 14**
- **Leap Year Calculation**

#### Code Example:
```python
# Check if a year is a leap year
year = int(input("Enter a year: "))

if (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0):
    print(f"{year} is a leap year.")
else:
    print(f"{year} is not a leap year.")
```

---

### **Loops**
- **For Loop**: Iterate over a sequence
- **While Loop**: Continue until condition is false

---

### **Assignment 15**
- **Factorial of a Number**

#### Code Example:
```python
# Factorial using for loop
num = int(input("Enter a number: "))
factorial = 1

for i in range(1, num + 1):
    factorial *= i  # Multiply each number

print(f"Factorial of {num} is {factorial}")
```

---

### **Assignment 16**
- **Sum of Digits**

#### Code Example:
```python
# Calculate the sum of digits of a number
num = input("Enter a positive integer: ")
sum_of_digits = sum(int(digit) for digit in num)  # Add each digit

print(f"Sum of digits: {sum_of_digits}")
```

---

### **Assignment 17**
- **Multiplication Table**

#### Code Example:
```python
# Generate multiplication table up to 12
num = int(input("Enter a number: "))

for i in range(1, 13):
    print(f"{num} x {i} = {num * i}")  # Display multiplication table
```

---

### **Debugging**
- **Errors**: Syntax, runtime, logic
- **Print Statements**: Simple debugging
- **Debugger**: Set breakpoints, inspect variables

---

### **Assignment 18**
- **Guessing Game**

#### Code Example:
```python
# Guess the secret number (max 10 tries)
secret_number = 7
attempts = 0
max_attempts = 10

while attempts < max_attempts:
    guess = int(input("Guess the number: "))
    if guess == secret_number:
        print("Correct!")
        break
    else:
        print("Try again.")
    attempts += 1
```

---

### **Assignment 19**
- **ATM Withdrawal Simulation**

#### Code Example:
```python
# Simulate ATM withdrawal
balance = float(input("Enter your balance: "))
withdraw = float(input("Enter amount to withdraw: "))

if withdraw % 10 != 0:
    print("Amount must be a multiple of 10.")
elif withdraw > balance:
    print("Insufficient balance.")
else:
    balance -= withdraw
    print(f"Withdrawal successful. Remaining balance: {balance}")
```

---

### **Assignment 20**
- **Password Strength Checker**

#### Code Example:
```python
# Check password strength
password = input("Enter your password: ")

criteria_met = 0
if len(password) >= 8:
    criteria_met += 1
if any(char.isdigit() for char in password):
    criteria_met += 1
if any(char.isupper() for char in password) and any(char.islower() for char in password):
    criteria_met += 1
if any(char in "!@#$%^&*" for char in password):
    criteria_met += 1

if criteria_met == 4:
    print("Strong password")
elif criteria_met == 3:
    print("Moderate password")
else:
    print("Weak password")
```

---
