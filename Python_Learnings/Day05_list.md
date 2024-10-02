

### **Lists**  
A versatile data structure that stores an ordered collection of items:
- **Mutable**: Can change after creation.
- **Can hold elements of different data types**.
- **Allows duplicate data**.
- **Maintains order of insertion**.

---

### **List Operations**  
**File: listOperations.py**

- **List is denoted by**:  
  `empty_list = []`

- **Accessing list Elements**:  
  - **Indexing**: `my_list[index]`  
  - **Slicing a list**: `my_list[startInd:endInd]`

- **Modifying List**:  
  - `my_list[index] = new_value`

- **Adding Elements**:  
  - `append()`
  - `insert()`
  - `extend()`

- **Removing Elements**:  
  - `remove()`
  - `pop()`
  - `clear()`

- **Copy List**:  
  - `copy()`

- **Concatenation**:  
  - `'+' operator`

- **Repetition**:  
  - `'*' operator`

- **Membership**:  
  - `'in', 'not in'`

- **Nested Lists**:  
  - `nested_list = [1, [2, 3], [4, 5, 6]]`

- **List Methods**:  
  - `sort()`
  - `reverse()`
  - `index()`
  - `count()`

---

### **Hands-On Assignments**

#### **Assignment 1:**  
**Create a program that generates and stores all prime numbers up to a given number in a list.**

**Input**:  
Prompt the user to enter a positive integer `n`.  

**Logic**:  
Write a logic that checks if a number is prime.  
Use a loop to generate all prime numbers up to `n` and store them in a list.  

**Output**:  
Display the list of prime numbers.

**Solution**:
```python
n = int(input("Enter a positive integer: "))
primes = []

for num in range(2, n + 1):
    is_prime = True
    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            is_prime = False
            break
    if is_prime:
        primes.append(num)

print("Prime numbers up to", n, ":", primes)
```

---

#### **Assignment 2:**  
**Write a program that implements a basic to-do list where users can add, remove, and view tasks.**

**Input**:  
Allow the user to add tasks to the to-do list.  
Allow the user to remove tasks by specifying the task name.  
Allow the user to view the current list of tasks.  

**Logic**:  
Use a list to store the tasks.  
Implement a loop that continuously prompts the user to choose an action (add, remove, view, or exit).  

**Output**:  
Display the updated to-do list after each operation.

**Solution**:
```python
tasks = []

while True:
    action = input("Choose an action: add, remove, view, or exit: ").lower()
    
    if action == "add":
        task = input("Enter the task: ")
        tasks.append(task)
        print("Task added.")
        
    elif action == "remove":
        task = input("Enter the task to remove: ")
        if task in tasks:
            tasks.remove(task)
            print("Task removed.")
        else:
            print("Task not found.")
            
    elif action == "view":
        print("Current tasks:", tasks)
        
    elif action == "exit":
        print("Exiting the to-do list.")
        break
        
    else:
        print("Invalid action. Please choose again.")
```

---

#### **Assignment 3:**  
**Create a program that checks if two strings are anagrams (two strings that contain the same characters in a different order).**

**Input**:  
Prompt the user to enter two strings.  

**Logic**:  
Remove spaces and convert both strings to lowercase.  
Sort the characters in both strings and compare them.  

**Output**:  
Display whether the strings are anagrams.

**Solution**:
```python
str1 = input("Enter the first string: ").replace(" ", "").lower()
str2 = input("Enter the second string: ").replace(" ", "").lower()

if sorted(str1) == sorted(str2):
    print("The strings are anagrams.")
else:
    print("The strings are not anagrams.")
```

---

### **Homework Assignments**

#### **Assignment 1:**  
**Try the following string operations:**  
- **Removing Leading Characters**: `lstrip(chars)`  
- **Removing Trailing Characters**: `rstrip(chars)`  
- **Joining a List into a String with a Space**: `" ".join(listname)`  
- **Joining a List into a String with a Custom Separator**: `"#".join(listname)`

**Example Solution:**
```python
# Example list
example_list = ['Hello', 'world', 'Python', 'is', 'great']

# Removing Leading Characters
leading_removed = '!!!Hello!!!'.lstrip('!')
print("Removing Leading Characters:", leading_removed)

# Removing Trailing Characters
trailing_removed = '!!!Hello!!!'.rstrip('!')
print("Removing Trailing Characters:", trailing_removed)

# Joining a List into a String with a Space
joined_space = " ".join(example_list)
print("Joining with Space:", joined_space)

# Joining a List into a String with a Custom Separator
joined_hash = "#".join(example_list)
print("Joining with Custom Separator:", joined_hash)
```

---

#### **Assignment 2:**  
**Write a program that asks the user how many days are in a particular month, and what day of the week the month begins on (0 for Monday, 1 for Tuesday, etc.), and then prints a calendar for that month.**

**Example Solution:**
```python
def print_calendar(days, start_day):
    days_of_week = ["Mon", "Tue", "Wed", "Thu", "Fri", "Sat", "Sun"]
    
    # Print header
    print(" ".join(days_of_week))
    
    # Print initial spaces
    print("    " * start_day, end="")
    
    for day in range(1, days + 1):
        print(f"{day:>3}", end=" ")
        if (day + start_day) % 7 == 0:
            print()  # New line after each week
    print()  # New line at the end of the calendar

days_in_month = int(input("Enter the number of days in the month: "))
starting_day = int(input("Enter the starting day of the week (0 for Mon, 1 for Tue, etc.): "))

print_calendar(days_in_month, starting_day)
```

---

#### **Assignment 3:**  
**Reverse a list in Python.**

**Solution:**
```python
# Example list
my_list = [1, 2, 3, 4, 5]

# Reversing the list
reversed_list = my_list[::-1]
print("Reversed List:", reversed_list)
```

---

#### **Assignment 4:**  
**Concatenate two lists index-wise.**

**Solution:**
```python
list1 = [1, 2, 3]
list2 = ['a', 'b', 'c']

# Concatenating index-wise
concatenated_list = [f"{x}{y}" for x, y in zip(list1, list2)]
print("Concatenated List:", concatenated_list)
```

---

#### **Assignment 5:**  
**Write a Python program to multiply all the items in a list.**

**Solution:**
```python
from functools import reduce

numbers = [1, 2, 3, 4]
product = reduce(lambda x, y: x * y, numbers)
print("Product of all items in the list:", product)
```

---

#### **Assignment 6:**  
**Write a Python program to get the smallest number from a list.**

**Solution:**
```python
numbers = [5, 2, 8, 1, 4]
smallest_number = min(numbers)
print("Smallest number in the list:", smallest_number)
```

---

#### **Assignment 7:**  
**Write a Python program to extract the 3rd to 9th characters from a long string.**

**Solution:**
```python
long_string = "This is an example of a long string."
extracted_characters = long_string[2:9]  # 3rd to 9th characters (index 2 to 8)
print("Extracted characters:", extracted_characters)
```

---

#### **Assignment 8:**  
**Replace Every Alternate Word in a Paragraph.**

**Input**:  
A single string paragraph that represents a paragraph of text.  

**Output**:  
A new string where every alternate word in the input paragraph is replaced with the word 'replaced'.  

**Logic**:  
- Use the `split()` method to divide the paragraph into a list of words.  
- **Replacing Alternate Words**:  
  Iterate through the list of words. Use the index of each word to

 determine if it is an alternate word. Replace every second word (i.e., words at odd indices) with the word 'replaced'.  
- **Joining Words**:  
  Combine the list of modified words back into a single string using the `join()` method, ensuring that words are separated by spaces. Print the new paragraph.

**Solution:**
```python
paragraph = input("Enter a paragraph: ")
words = paragraph.split()

for i in range(len(words)):
    if i % 2 == 1:  # Replace alternate words
        words[i] = 'replaced'

new_paragraph = " ".join(words)
print("Modified Paragraph:", new_paragraph)
```

---

### **Homework Assignments (Continued)**

#### **Assignment 3:**  
**Develop a Python program to extract all unique words and print them in alphabetical order.**

**Input**:  
A paragraph containing multiple lines of text.  

**Logic**:  
- Read the paragraph, split words, and store them in a list.  
- Convert the list to a set to remove duplicates, then sort the set alphabetically.  

**Output**:  
Display the unique words on console.

**Solution:**
```python
paragraph = input("Enter a paragraph: ")
words = paragraph.split()
unique_words = sorted(set(words))
print("Unique words in alphabetical order:", unique_words)
```

---

