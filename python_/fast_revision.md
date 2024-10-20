### Assignment 1: Remove repetitive characters from a string
**Question**: Implement a function that removes repetitive characters from a string.  
**Description**: For example, if the input is "laptop", the output should be "lapto" (removing the repeated 'p').

**Python Answer**:
```python
def remove_repetitive_chars(s):
    result = ""
    for char in s:
        if char not in result:
            result += char
    return result

# Example
print(remove_repetitive_chars("laptop"))  # Output: "lapto"
```

---

### Assignment 2: Masking PII
**Question**: Implement a function `mask_sensitive_info(info, info_type)` that masks email and credit card information.  
**Description**: For emails, mask characters except the first and last in the local part (before the '@'). For credit cards, mask all but the last four digits.

**Python Answer**:
```python
def mask_sensitive_info(info, info_type):
    if info_type == "email":
        local, domain = info.split('@')
        masked = local[0] + '*' * (len(local) - 2) + local[-1]
        return f"{masked}@{domain}"
    elif info_type == "credit_card":
        return '*' * 12 + info[-4:]
    else:
        raise ValueError("Invalid info type")

# Example
print(mask_sensitive_info("Mayura.kumari@xyz.com", "email"))  # Output: "m***i@xyz.com"
print(mask_sensitive_info("1234 5678 9101 1121", "credit_card"))  # Output: "**** **** **** 1121"
```

---

### Assignment 3: Reverse a list
**Question**: Reverse a given list.  
**Description**: For example, reversing `[100, 200, 300, 400, 500]` should output `[500, 400, 300, 200, 100]`.

**Python Answer**:
```python
def reverse_list(lst):
    return lst[::-1]

# Example
print(reverse_list([100, 200, 300, 400, 500]))  # Output: [500, 400, 300, 200, 100]
```

---

### Assignment 4: Find the largest and smallest number in a list
**Question**: Find the largest and smallest number in a user input list.  
**Description**: Use list operations to achieve this.

**Python Answer**:
```python
def find_min_max(lst):
    return min(lst), max(lst)

# Example
numbers = [int(x) for x in input("Enter numbers separated by space: ").split()]
print(find_min_max(numbers))  # Output: (smallest, largest)
```

---

### Assignment 5: Music Playlist Manager
**Question**: Implement a playlist manager with operations such as adding songs, removing a song, viewing all songs, and slicing the playlist.  
**Description**: Add exception handling for possible error conditions.

**Python Answer**:
```python
playlist = []

def add_songs():
    songs = input("Enter song titles separated by commas: ").split(", ")
    playlist.extend(songs)

def remove_song():
    song = input("Enter song to remove: ")
    try:
        playlist.remove(song)
    except ValueError:
        print("Song not found!")

def view_songs():
    print(", ".join(playlist))

def slice_playlist():
    start = int(input("Enter start index: "))
    end = int(input("Enter end index: "))
    print(playlist[start:end])

# Example usage
add_songs()
view_songs()
remove_song()
view_songs()
slice_playlist()
```

---

### Assignment 6: Tuples
**Question**: Create a tuple `shopping_cart` and perform operations such as printing, accessing elements, concatenating, unpacking, counting, and finding the index.  
**Description**: Practice with tuple operations.

**Python Answer**:
```python
shopping_cart = ('laptop', 'headphones', 'keyboard', 'mouse')

# Print the tuple
print(shopping_cart)

# Access and print the first and last items
print(shopping_cart[0])
print(shopping_cart[-1])

# Concatenate with another tuple
new_cart = shopping_cart + ('tablet', 'smartphone')
print(new_cart)

# Unpack the tuple
item1, item2, item3, item4 = shopping_cart
print(item1, item2, item3, item4)

# Count and index methods
print(shopping_cart.count('mouse'))
print(shopping_cart.index('keyboard'))
```

---

### Assignment 7: Dictionary operations
**Question**: Given a dictionary of students and their marks, perform operations like counting students, modifying, removing entries, and sorting.  
**Description**: Modify and manipulate dictionary data.

**Python Answer**:
```python
students = {'Mayura': 89, 'Pravin': 92, 'Ketaki': 95, 'Chinmay': 99}

# Total number of students
print(len(students))

# Change Pravin's marks
students['Pravin'] = 94

# Remove Ketaki
students.pop('Ketaki')

# Sort and print
for student in sorted(students):
    print(f"{student}: {students[student]}")
```

---

### Assignment 8: Translate text by replacing vowels with "abc"
**Question**: Write a function `translate()` that replaces every vowel with "abc".  
**Description**: Given a string, replace vowels.

**Python Answer**:
```python
def translate(text):
    vowels = "aeiouAEIOU"
    return ''.join("abc" if char in vowels else char for char in text)

# Example
print(translate("This is fun"))  # Output: "Thabcs abcs fabcn"
```

---
### Assignment 9: Online Food Management System
**Question**: Create a class `FoodItem` with attributes name, price, and category, and a method to display food item details.  
**Description**: Implement object-oriented programming to manage food items.

**Python Answer**:
```python
class FoodItem:
    def __init__(self, name, price, category):
        self.name = name
        self.price = price
        self.category = category

    def display_info(self):
        print(f"Food Item: {self.name}, Price: {self.price}, Category: {self.category}")

# Example usage
item = FoodItem("Pizza", 12.99, "Main Course")
item.display_info()  # Output: Food Item: Pizza, Price: 12.99, Category: Main Course
```

---

### Assignment 10: Regular Expressions and CSV
**Question**: Extract the `datetime` component from records using regular expressions and split it into date and time components.  
**Description**: Read from and write to a CSV file with updated formats.

**Python Answer**:
```python
import csv
import re

def process_csv(input_file, output_file):
    with open(input_file, 'r') as infile, open(output_file, 'w', newline='') as outfile:
        reader = csv.reader(infile)
        writer = csv.writer(outfile)
        for row in reader:
            for entry in row:
                match = re.search(r'datetime=(\d{4}-\d{2}-\d{2})T(\d{2}:\d{2}:\d{2})', entry)
                if match:
                    date, time = match.groups()
                    new_entry = re.sub(r'datetime=\d{4}-\d{2}-\d{2}T\d{2}:\d{2}:\d{2}', f'date={date}#time={time}', entry)
                    writer.writerow([new_entry])

# Example usage
process_csv('input.csv', 'output.csv')
```

---

### Assignment 11: Capitalize Words in a List
**Question**: Use a lambda function with `map()` to capitalize the first letter of each word in a list.  
**Description**: Given a list of words, return the list with capitalized words.

**Python Answer**:
```python
words = ['apple', 'banana', 'cherry']
capitalized_words = list(map(lambda x: x.capitalize(), words))

# Example
print(capitalized_words)  # Output: ['Apple', 'Banana', 'Cherry']
```

---

### Assignment 12: Find the Length of Strings
**Question**: Use a lambda function with `map()` to find the length of each string in a list.  
**Description**: Given a list of strings, return a list with their lengths.

**Python Answer**:
```python
strings = ['hello', 'world', 'python']
lengths = list(map(lambda x: len(x), strings))

# Example
print(lengths)  # Output: [5, 5, 6]
```

---

### Assignment 13: Build a URL Shortener
**Question**: Define a class `URLShortener` to manage URL shortening, where each original URL is assigned a shortened version.  
**Description**: Implement functionality to add and display shortened URLs.

**Python Answer**:
```python
class URLShortener:
    url_dict = {}
    base_url = "http://short.url/"
    
    def add_url(self, original_url):
        if original_url in self.url_dict:
            print(f"URL already exists: {self.url_dict[original_url]}")
            return self.url_dict[original_url]
        else:
            shortened_url = self.base_url + str(len(self.url_dict) + 1)
            self.url_dict[original_url] = shortened_url
            return shortened_url

# Example usage
shortener = URLShortener()
print(shortener.add_url("https://www.example.com"))  # Output: http://short.url/1
print(shortener.add_url("https://www.python.com"))   # Output: http://short.url/2
```

---
