### **Assignment 1: Initialize Two Numbers, Add Them, Print the Result**
**Concept**: This assignment demonstrates basic arithmetic operations using variables.

**Question**: Initialize two numbers, add them, and print the result.  
**Python Answer**:
```python
num1 = 5
num2 = 10
result = num1 + num2
print("Sum:", result)
```

---

### **Assignment 2: Add an Integer and a Float, Print Result and Type**
**Concept**: This task focuses on arithmetic between different data types (integer and float) and how Python handles mixed-type operations.

**Question**: Add an integer and a float, print the result and the type of the result.  
**Python Answer**:
```python
int_num = 3
float_num = 4.5
result = int_num + float_num
print("Result:", result)
print("Type of result:", type(result))
```

---

### **Assignment 3: Initialize a Float Value, Typecast it to Integer, and Print its Square**
**Concept**: This exercise covers typecasting between different data types and performing mathematical operations.

**Question**: Initialize a float value, typecast it to an integer, and print its square.  
**Python Answer**:
```python
float_num = 4.7
int_num = int(float_num)
square = int_num ** 2
print("Square of", int_num, "is", square)
```

---

### **Assignment 4: Add a String and a Number, Print Result and Type**
**Concept**: This introduces handling data type errors, specifically combining a string with a number and converting data types when necessary.

**Question**: Add a string and a number, print the result and type of the result.  
**Python Answer**:
```python
string_value = "The result is "
num = 10
result = string_value + str(num)
print(result)
print("Type of result:", type(result))
```

---

### **Assignment 1: Convert Inches to Feet, Meters, and Centimeters**
**Concept**: This assignment involves unit conversions, looping, and decision-making based on user input.

**Question**: Create a program to convert inches to feet, meters, and centimeters, continuing until the user wishes to stop.  
**Python Answer**:
```python
def inches_to_feet(inches):
    return inches / 12

def inches_to_meters(inches):
    return inches * 0.0254

def inches_to_cm(inches):
    return inches * 2.54

while True:
    inches = float(input("Enter value in inches: "))
    unit = input("Convert to (feet, meters, cm): ")
    
    if unit == "feet":
        print(f"{inches} inches is {inches_to_feet(inches)} feet.")
    elif unit == "meters":
        print(f"{inches} inches is {inches_to_meters(inches)} meters.")
    elif unit == "cm":
        print(f"{inches} inches is {inches_to_cm(inches)} cm.")
    
    repeat = input("Do you want to continue? (Yes/No): ").lower()
    if repeat == 'no':
        break
```

---

### **Assignment 2: Build a Calculator for Basic Operations**
**Concept**: This covers conditional logic to perform different arithmetic operations based on user input.

**Question**: Build a calculator for addition, subtraction, multiplication, and division using `if-else` statements.  
**Python Answer**:
```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b != 0:
        return a / b
    else:
        return "Cannot divide by zero"

while True:
    choice = input("Choose operation (+, -, *, /): ")
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))
    
    if choice == '+':
        print("Result:", add(num1, num2))
    elif choice == '-':
        print("Result:", subtract(num1, num2))
    elif choice == '*':
        print("Result:", multiply(num1, num2))
    elif choice == '/':
        print("Result:", divide(num1, num2))
    
    repeat = input("Do you want to continue? (Yes/No): ").lower()
    if repeat == 'no':
        break
```

---

### **Assignment 3: Add an Integer and a Float, Print Result and Type**
**Concept**: Revisiting the concept of mixed-type arithmetic operations.

**Question**: Add an integer and a float, print the result, and the type of the result.  
**Python Answer**:
```python
int_num = 7
float_num = 5.5
result = int_num + float_num
print("Result:", result)
print("Type of result:", type(result))
```

---

### **Assignment 1: Count Occurrence of Letter ‘a’ in a String**
**Concept**: This task involves string manipulation and counting specific characters.

**Question**: Write a program to count the occurrence of the letter 'a' in a string.  
**Python Answer**:
```python
input_string = input("Enter a string: ")
count_a = input_string.count('a')
print(f"The letter 'a' appears {count_a} times.")
```

---

### **Assignment 2: Count Occurrence of Digit '0' in a Number**
**Concept**: This covers loops, conditionals, and repeated checks with user input.

**Question**: Ask for a number, count the occurrence of digit 0 in it, and ask if the user wants to continue with another number.  
**Python Answer**:
```python
while True:
    number = input("Enter a number: ")
    zero_count = number.count('0')
    print(f"The digit '0' appears {zero_count} times in {number}.")
    
    repeat = input("Do you want to enter another number? (Yes/No): ").lower()
    if repeat == 'no':
        break
```

---

### **Assignment 3: Create a Pyramid Pattern of Stars**
**Concept**: This assignment introduces nested loops to create a star pattern.

**Question**: Write a program to create a pyramid pattern of stars.  
**Python Answer**:
```python
rows = int(input("Enter the number of rows: "))

for i in range(1, rows+1):
    print(' ' * (rows - i) + '*' * (2 * i - 1))
```

---

### **Assignment 11: Check if a String is a Palindrome**
**Concept**: This task checks if a string reads the same forward and backward, ignoring case and spaces.

**Question**: Write a program to check if a string is a palindrome.  
**Python Answer**:
```python
def is_palindrome(s):
    s = s.replace(" ", "").lower()  # Remove spaces and convert to lowercase
    return s == s[::-1]

input_string = input("Enter a string: ")
if is_palindrome(input_string):
    print("The string is a palindrome.")
else:
    print("The string is not a palindrome.")
```

---

### **Assignment 1: String Operations**
**Concept**: This assignment covers basic string manipulation methods, such as removing characters and joining lists into strings.

**Question**: Try the following string operations:  
- Removing Leading Characters - `lstrip(chars)`
- Removing Trailing Characters - `rstrip(chars)`
- Joining a List into a String with a Space - `" ".join(listname)`
- Joining a List into a String with a Custom Separator - `"#".join(listname)`

**Python Answer**:
```python
# Example string
sample_string = "---hello world---"

# Removing leading characters
print(sample_string.lstrip('-'))  # Output: "hello world---"

# Removing trailing characters
print(sample_string.rstrip('-'))  # Output: "---hello world"

# Joining a list into a string with space
words = ['hello', 'world']
print(" ".join(words))  # Output: "hello world"

# Joining a list into a string with custom separator
print("#".join(words))  # Output: "hello#world"
```

---

### **Assignment 2: Print Calendar for a Month**
**Concept**: This involves using loops and conditionals to print a calendar, based on user input for the number of days and starting day.

**Question**: Write a program that asks the user for the number of days in a month and the starting day of the week, and print a calendar for that month.  
**Python Answer**:
```python
def print_calendar(days, start_day):
    print("Mon Tue Wed Thu Fri Sat Sun")
    
    # Print initial spaces for the starting day
    for _ in range(start_day):
        print("    ", end="")
    
    # Print all the days
    for day in range(1, days + 1):
        print(f"{day:3} ", end="")
        if (start_day + day) % 7 == 0:
            print()

# Example usage
days = int(input("Enter the number of days in the month: "))
start_day = int(input("Enter the starting day (0 for Monday, 6 for Sunday): "))
print_calendar(days, start_day)
```

---

### **Assignment 3: Reverse a List**
**Concept**: This assignment covers reversing a list using Python's slicing techniques or loops.

**Question**: Write a program to reverse a list in Python.  
**Python Answer**:
```python
def reverse_list(lst):
    return lst[::-1]

# Example usage
my_list = [1, 2, 3, 4, 5]
print(reverse_list(my_list))  # Output: [5, 4, 3, 2, 1]
```

---

### **Assignment 4: Concatenate Two Lists Index-wise**
**Concept**: Concatenating two lists element by element is a common operation in Python.

**Question**: Write a program to concatenate two lists index-wise.  
**Python Answer**:
```python
def concatenate_lists(list1, list2):
    return [i + j for i, j in zip(list1, list2)]

# Example usage
list1 = ['a', 'b', 'c']
list2 = ['1', '2', '3']
print(concatenate_lists(list1, list2))  # Output: ['a1', 'b2', 'c3']
```

---

### **Assignment 5: Multiply All Items in a List**
**Concept**: This task covers iterating through lists and performing multiplication operations.

**Question**: Write a Python program to multiply all the items in a list.  
**Python Answer**:
```python
def multiply_list(lst):
    result = 1
    for num in lst:
        result *= num
    return result

# Example usage
numbers = [1, 2, 3, 4]
print(multiply_list(numbers))  # Output: 24
```

---

### **Assignment 6: Get the Smallest Number from a List**
**Concept**: This involves finding the smallest value in a list using the `min()` function or loops.

**Question**: Write a Python program to get the smallest number from a list.  
**Python Answer**:
```python
def get_smallest(lst):
    return min(lst)

# Example usage
numbers = [5, 3, 8, 1, 9]
print(get_smallest(numbers))  # Output: 1
```

---

### **Assignment 7: Extract 3rd to 9th Characters from a Long String**
**Concept**: This assignment focuses on string slicing to extract a specific portion of a string.

**Question**: Write a Python program to extract the 3rd to 9th characters from a long string.  
**Python Answer**:
```python
def extract_chars(s):
    return s[2:9]  # Slicing from index 2 to 8 (3rd to 9th characters)

# Example usage
long_string = "This is a long string"
print(extract_chars(long_string))  # Output: "is is a"
```

---

### **Assignment 8: Replace Every Alternate Word in a Paragraph**
**Concept**: This task involves string manipulation, specifically replacing alternate words using list indexing.

**Question**: Write a program to replace every alternate word in a paragraph with the word "replaced".  
**Python Answer**:
```python
def replace_alternate_words(paragraph):
    words = paragraph.split()
    for i in range(1, len(words), 2):
        words[i] = 'replaced'
    return " ".join(words)

# Example usage
paragraph = "This is an example paragraph to demonstrate alternate word replacement."
print(replace_alternate_words(paragraph))
# Output: "This replaced an replaced paragraph replaced demonstrate replaced replacement."
```

---

### **Assignment 1: Calculator for Basic Operations with Functions**
**Concept**: Using functions for modularizing code that performs arithmetic operations based on user input.

**Question**: Create a calculator for addition, subtraction, multiplication, and division.  
**Python Answer**:
```python
def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b != 0:
        return a / b
    else:
        return "Cannot divide by zero"

while True:
    choice = input("Choose operation (+, -, *, /): ")
    num1 = float(input("Enter first number: "))
    num2 = float(input("Enter second number: "))
    
    if choice == '+':
        print("Result:", add(num1, num2))
    elif choice == '-':
        print("Result:", subtract(num1, num2))
    elif choice == '*':
        print("Result:", multiply(num1, num2))
    elif choice == '/':
        print("Result:", divide(num1, num2))
    
    repeat = input("Do you want to continue? (Yes/No): ").lower()
    if repeat == 'no':
        break
```

---
### **Assignment 2: Repeat Specific Elements within a Tuple**
**Concept**: This assignment involves working with tuples and demonstrating repetition of specific elements using functions.

**Question**: Write a program that performs the following tasks:  
- Prompt the user to enter a tuple of elements (mixed types allowed).
- Convert the input string to a tuple of elements.
- Prompt the user for an element to repeat and the number of times to repeat it.
- Create a new tuple where the specified element is repeated the given number of times, with the rest of the elements unchanged.

**Python Answer**:
```python
def repeat_element_in_tuple(tup, element, times):
    new_tup = tuple(item if item != element else element * times for item in tup)
    return new_tup

# Example usage
elements = input("Enter tuple elements separated by commas: ").split(", ")
tup = tuple(elements)
element_to_repeat = input("Enter the element to repeat: ")
repeat_times = int(input("Enter how many times to repeat it: "))

new_tuple = repeat_element_in_tuple(tup, element_to_repeat, repeat_times)
print("Original tuple:", tup)
print("New tuple:", new_tuple)
```

---

### **Assignment 1: Voting System for Favorite Movies**
**Concept**: This assignment deals with dictionaries and allows users to manage votes for a list of movies.

**Question**: Implement a function `manage_votes()` that manages votes for a list of movies with the following operations:
- Add a new movie with 0 initial votes.
- Vote for a movie.
- Remove a movie from the list.
- Display voting results.
- Find and display the top-voted movie.

**Python Answer**:
```python
def manage_votes():
    votes = {}
    
    while True:
        print("\n1. Add Movie\n2. Vote for Movie\n3. Remove Movie\n4. Display Voting Results\n5. Find Top Movie\n6. Exit")
        choice = int(input("Enter your choice: "))
        
        if choice == 1:
            movie = input("Enter the movie name: ")
            votes[movie] = 0
            print(f"Added {movie} with 0 votes.")
        
        elif choice == 2:
            movie = input("Enter the movie name to vote for: ")
            if movie in votes:
                votes[movie] += 1
                print(f"Voted for {movie}.")
            else:
                print(f"{movie} not found.")
        
        elif choice == 3:
            movie = input("Enter the movie name to remove: ")
            if movie in votes:
                del votes[movie]
                print(f"Removed {movie}.")
            else:
                print(f"{movie} not found.")
        
        elif choice == 4:
            for movie, vote_count in votes.items():
                print(f"{movie}: {vote_count} votes")
        
        elif choice == 5:
            if votes:
                top_movie = max(votes, key=votes.get)
                print(f"Top voted movie: {top_movie} with {votes[top_movie]} votes.")
            else:
                print("No movies available.")
        
        elif choice == 6:
            break

# Example usage
manage_votes()
```

---

### **Assignment 1: Convert Celsius to Fahrenheit**
**Concept**: This task covers using lambda functions and the `map()` function to convert temperatures from Celsius to Fahrenheit.

**Question**: Use a lambda function with `map()` to convert a list of temperatures from Celsius to Fahrenheit.  
**Python Answer**:
```python
celsius_temperatures = [0, 20, 37, 100]
fahrenheit_temperatures = list(map(lambda c: (c * 9/5) + 32, celsius_temperatures))

print(fahrenheit_temperatures)  # Output: [32.0, 68.0, 98.6, 212.0]
```



### **Assignment 2: Add Two Lists Element-wise**
**Concept**: This assignment covers element-wise operations on lists using lambda functions and `map()`.

**Question**: Use a lambda function with `map()` to add corresponding elements from two lists.  
**Python Answer**:
```python
list1 = [1, 2, 3]
list2 = [4, 5, 6]
summed_list = list(map(lambda x, y: x + y, list1, list2))

print(summed_list)  # Output: [5, 7, 9]
```

---

### **Assignment 3: Capitalize Words in a List**
**Concept**: This task involves using lambda functions to manipulate strings, specifically capitalizing the first letter of each word.

**Question**: Use a lambda function with `map()` to capitalize the first letter of each word in a list.  
**Python Answer**:
```python
words = ['apple', 'banana', 'cherry']
capitalized_words = list(map(lambda word: word.capitalize(), words))

print(capitalized_words)  # Output: ['Apple', 'Banana', 'Cherry']
```


## **Assignment 4: Find the Length of Strings**
**Concept**: Using lambda functions with `map()` to find the length of each string in a list.

**Question**: Use a lambda function with `map()` to find the length of each string in a list.  
**Python Answer**:
```python
strings = ['hello', 'world', 'python']
lengths = list(map(lambda word: len(word), strings))

print(lengths)  # Output: [5, 5, 6]
```



### **Assignment 5: Daily Temperature Tracker**
**Concept**: This assignment demonstrates working with dictionaries, where the user can update temperature data and calculate averages.

**Question**: Create a dictionary to store and manipulate daily temperature data for a week. The program should:
- Allow the user to update the temperature for any day.
- Calculate the average temperature for the week.

**Python Answer**:
```python
def update_temperature(data, day, temp):
    data[day] = temp

def calculate_average_temperature(data):
    return sum(data.values()) / len(data)

# Example usage
temperature_data = {
    'Monday': 30, 'Tuesday': 32, 'Wednesday': 29,
    'Thursday': 31, 'Friday': 30, 'Saturday': 28, 'Sunday': 27
}

# Update temperature
update_temperature(temperature_data, 'Wednesday', 33)

# Calculate average temperature
average_temp = calculate_average_temperature(temperature_data)
print(f"Average temperature: {average_temp:.2f}°C")
```

---

### **Assignment 6: Bird Species Observation Tracker**
**Concept**: This assignment demonstrates using dictionaries to track occurrences and perform operations on the data.

**Question**: Create a dictionary to track the number of sightings of different bird species.  
**Python Answer**:
```python
bird_sightings = {'sparrow': 10, 'eagle': 5, 'hawk': 7}

# Add a new species
bird_sightings['parrot'] = 3

# Update sightings for an existing species
bird_sightings['eagle'] += 2

# Find the bird with the highest number of sightings
top_bird = max(bird_sightings, key=bird_sightings.get)
print(f"The bird with the highest sightings is '{top_bird}' with {bird_sightings[top_bird]} sightings.")
```

---



Here’s the structured assignment along with the answers for each task:

---

### Assignment 1: Replace a Keyword in a Text File
**Task:** Search for all occurrences of the keyword 'after', replace it with 'before’. Save the modified content back to the file. Create functions wherever appropriate.

**Answer:**

```python
def replace_keyword_in_file(filename, old_keyword, new_keyword):
    try:
        with open(filename, 'r') as file:
            content = file.read()
        
        modified_content = content.replace(old_keyword, new_keyword)
        
        with open(filename, 'w') as file:
            file.write(modified_content)
        
        print("Keyword replacement completed successfully.")
    
    except FileNotFoundError:
        print("Error: The file does not exist.")

# Usage
replace_keyword_in_file('sample.txt', 'after', 'before')
```

---

### Assignments

#### Assignment 1: Temperature Converter
**Input from user:** 
- Temperature value and unit 
- Temperature unit to convert to

**Functions:** 
- `celsius_to_fahrenheit(celsius)`
- `fahrenheit_to_celsius(fahrenheit)`
- `celsius_to_kelvin(celsius)`

**Employ exception handling for checking numeric values. Include: `finally` and `else` blocks.**

**Answer:**

```python
def celsius_to_fahrenheit(celsius):
    return (celsius * 9/5) + 32

def fahrenheit_to_celsius(fahrenheit):
    return (fahrenheit - 32) * 5/9

def celsius_to_kelvin(celsius):
    return celsius + 273.15

def temperature_converter():
    try:
        temp_value = float(input("Enter the temperature value: "))
        unit = input("Enter the current temperature unit (C/F): ").upper()
        target_unit = input("Enter the temperature unit to convert to (C/F/K): ").upper()
        
        if unit == 'C':
            if target_unit == 'F':
                result = celsius_to_fahrenheit(temp_value)
                print(f"{temp_value}°C = {result:.2f}°F")
            elif target_unit == 'K':
                result = celsius_to_kelvin(temp_value)
                print(f"{temp_value}°C = {result:.2f}K")
            else:
                print("Invalid target unit.")
        
        elif unit == 'F':
            if target_unit == 'C':
                result = fahrenheit_to_celsius(temp_value)
                print(f"{temp_value}°F = {result:.2f}°C")
            else:
                print("Invalid target unit.")
        
        else:
            print("Invalid current unit.")
    
    except ValueError:
        print("Please enter a numeric value for the temperature.")
    
    finally:
        print("Temperature conversion process finished.")

# Usage
temperature_converter()
```

---

### Assignment 2: Handle File Not Found Exception

**Answer:** (Incorporated in the previous answer regarding file handling.)

---

### Assignments

#### Assignment 1: Create a Class that Simulates a Simple Bank Account
**Class Name:** `BankAccount` 

**Attributes:** 
- Rate of interest
- Bank name
- `account_holder` (string)
- `balance` (float, initialized to 0.0)

**Methods:**
- `deposit(amount)`: Adds the given amount to the balance.
- `withdraw(amount)`: Deducts the given amount from the balance if sufficient funds are available; otherwise, print "Insufficient balance."
- `check_balance()`: Prints the current balance.

**Create an account for a user (e.g., `account1 = BankAccount("Alice")`), perform deposits, withdrawals, and check the balance.**

**Answer:**

```python
class BankAccount:
    def __init__(self, account_holder):
        self.bank_name = "MyBank"
        self.account_holder = account_holder
        self.balance = 0.0
        self.interest_rate = 4.9  # Default interest rate

    def deposit(self, amount):
        self.balance += amount
        print(f"Deposited: ${amount:.2f}")

    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
            print(f"Withdrew: ${amount:.2f}")
        else:
            print("Insufficient balance.")

    def check_balance(self):
        print(f"Current balance: ${self.balance:.2f}")

# Usage
account1 = BankAccount("Alice")
account1.deposit(500)
account1.withdraw(200)
account1.check_balance()
```

---

### Assignments

#### Parent Class: `Bank_Account`
- It should initialize with a default `interest_rate` of 4.9%.

**Implement the method:** `display_interest_rate()` to print the regular interest rate.

**Attribute:** `interest_rate`: A class-level attribute, which is set to 4.9 for regular citizens.

#### Child Class: `Senior_Citizen` (inherits from `Bank_Account`)
- **Override Attribute:** `interest_rate`: This is set to 5.9 for senior citizens.
- **Methods:**
  - `display_interest_rate()`: This method overrides the parent method to print the interest rate for senior citizens.
  - `get_customer_details()`: This method will accept and display customer details such as name and age.

**Write a script that:**
- Creates an instance of the `Bank_Account` class and displays the interest rate.
- Creates an instance of the `Senior_Citizen` class, displays the interest rate, and also displays the interest rate for regular citizens using `super()`.

**Answer:**

```python
class Bank_Account:
    interest_rate = 4.9  # Class-level attribute for regular citizens

    def display_interest_rate(self):
        print(f"Interest Rate for Regular Citizens: {self.interest_rate}%")

class Senior_Citizen(Bank_Account):
    interest_rate = 5.9  # Overriding interest rate for senior citizens

    def display_interest_rate(self):
        print(f"Interest Rate for Senior Citizens: {self.interest_rate}%")

    def get_customer_details(self, name, age):
        print(f"Customer Name: {name}, Age: {age}")

# Usage
regular_account = Bank_Account()
regular_account.display_interest_rate()

senior_account = Senior_Citizen()
senior_account.display_interest_rate()
super(Senior_Citizen, senior_account).display_interest_rate()  # Display regular citizen rate
senior_account.get_customer_details("Bob", 65)
```

---

### Assignments

#### Assignment 1: Smart Home Devices Management
- **Base abstract class:** `SmartDevice`
- **Class variables:** `_name` (string), `_status`
- **Abstract methods:** `turn_on()`, `turn_off()`
- **Non-abstract method:** `device_info()`
  
#### Subclass: `SmartLight`
- Inherit from the `SmartDevice` class.
- Implement `turn_on()` and `turn_off()` methods to set `_status` to 'on' and return "Smart light is now on."
- Add a method `set_brightness(level)` that accepts a brightness level (integer from 0 to 100) and returns a string, e.g., "Brightness set to 70%."
- Use the `super()` function to initialize the inherited protected instance variables in the constructor.

**Answer:**

```python
from abc import ABC, abstractmethod

class SmartDevice(ABC):
    def __init__(self, name):
        self._name = name
        self._status = 'off'

    @abstractmethod
    def turn_on(self):
        pass

    @abstractmethod
    def turn_off(self):
        pass

    def device_info(self):
        return f"Device: {self._name}, Status: {self._status}"

class SmartLight(SmartDevice):
    def turn_on(self):
        self._status = 'on'
        return "Smart light is now on."

    def turn_off(self):
        self._status = 'off'
        return "Smart light is now off."

    def set_brightness(self, level):
        if 0 <= level <= 100:
            return f"Brightness set to {level}%."
        else:
            return "Brightness level must be between 0 and 100."

# Usage
smart_light = SmartLight("Living Room Light")
print(smart_light.turn_on())
print(smart_light.set_brightness(70))
print(smart_light.device_info())
```

---

### Assignments

#### Assignment 1: Extract all phone numbers in the format (XXX) XXX-XXXX from a text.

**Answer:**

```python
import re

def extract_phone_numbers(text):
    pattern = r'\(\d{3}\) \d{3}-\d{4}'
    return re.findall(pattern, text)

# Usage
sample_text = "Contact us at (123) 456-7890 or (987) 654-3210."
phone_numbers = extract_phone_numbers(sample_text)
print(phone_numbers)
```

---

#### Assignment 2: Find all hashtags in a social media post (e.g., #Python).

**Challenge 1:** Ensure that hashtags are case-insensitive, meaning #Python and #python should be counted as the same hashtag.

**Challenge 2:** Exclude any hashtags that are shorter than 4 characters (e.g., #AI should be excluded).

**Answer:**

```python
def extract_hashtags(text):
    pattern = r'#[A-Za-z]{4,}'
    hashtags = re.findall(pattern, text)
    return list(set([hashtag.lower() for hashtag in hashtags]))  # Remove duplicates and make case insensitive

# Usage
social_media_post = "

I love #Python, #coding, and #AI. #DataScience is great!"
hashtags = extract_hashtags(social_media_post)
print(hashtags)
```

--- 

Feel free to reach out if you need any further clarifications or assistance!