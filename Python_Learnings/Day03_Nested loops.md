
### **Hands-on Assignments**

#### **Assignment 1: Print even numbers (up to 50) using while loop.**

**Solution**:
```python
i = 2
while i <= 50:
    print(i, end=" ")
    i += 2
```

---

#### **Assignment 2: Reverse a String (for loop)**  
Example:  
Input: `Hello`  
Output: `olleH`

**Solution**:
```python
string = input("Enter a string: ")
reversed_string = ""
for char in string:
    reversed_string = char + reversed_string
print("Reversed string is:", reversed_string)
```

---

#### **Assignment 3: Find Prime Numbers (for loop)**  

**Solution**:
```python
n = int(input("Enter a number: "))
for num in range(2, n + 1):
    is_prime = True
    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            is_prime = False
            break
    if is_prime:
        print(num, end=" ")
```

---

### **Nested loops**  
- Nested `for` loop  
- Nested `while` loop  
- `else` clause in loops  

---

#### **Assignment 4: Create Multiplication tables for 1 – 5 numbers using nested for and while loops.**

**Solution (Nested for loop)**:
```python
for i in range(1, 6):
    print(f"Multiplication table for {i}:")
    for j in range(1, 11):
        print(f"{i} x {j} = {i * j}")
    print()  # Blank line for readability
```

**Solution (Nested while loop)**:
```python
i = 1
while i <= 5:
    print(f"Multiplication table for {i}:")
    j = 1
    while j <= 10:
        print(f"{i} x {j} = {i * j}")
        j += 1
    i += 1
    print()  # Blank line for readability
```

---

#### **Assignment 5: Print Right-Angled Triangle**  

**Pattern of numbers using nested for loop**:

**Solution**:
```python
n = 5
for i in range(1, n + 1):
    for j in range(1, i + 1):
        print(j, end=" ")
    print()  # Newline after each row
```

**Right-Angled Triangle Pattern of stars using nested while loop**:

**Solution**:
```python
n = 5
i = 1
while i <= n:
    j = 1
    while j <= i:
        print("*", end=" ")
        j += 1
    print()  # Newline after each row
    i += 1
```

---

### **Homework**

#### **Assignment 1: Count occurrence of letter ‘a’ in a String.**

**Solution**:
```python
string = input("Enter a string: ")
count = 0
for char in string:
    if char == 'a':
        count += 1
print(f"Number of occurrences of 'a': {count}")
```

---

#### **Assignment 2: Ask for a number from a user and count occurrence of digit 0 in it. Print the number and the number of zeros in the number. Ask for the user if she wants to add a new number. If yes, check for zeros again. Continue until user says ‘N’.**

**Solution**:
```python
while True:
    number = input("Enter a number: ")
    count = number.count('0')
    print(f"Number: {number}, Number of zeros: {count}")

    choice = input("Do you want to enter another number? (Y/N): ").upper()
    if choice == 'N':
        break
```

---

#### **Assignment 3: Create a Pyramid pattern of stars.**

**Solution**:
```python
n = 5
for i in range(1, n + 1):
    print(' ' * (n - i) + '* ' * i)
```

---

