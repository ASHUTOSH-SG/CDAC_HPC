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
def mask(info, info_type):
    if info_type == "email":  # If the info type is 'email'
        local, domain = info.split("@")  
        # Split the email into local part and domain
        # Mask the local part by showing only the first character, 
        #and replacing the rest with '*'
        masked = local[0] + '*' * (len(local) - 1)
        return f"{masked}@{domain}"  # Return the masked local part and keep the domain unchanged
    elif info_type == "credit_card":  # If the info type is 'credit_card'
        # Mask the first 12 digits with '*' and keep the last 4 digits visible
        return '*' * 12 + info[-4:]
    else:
        raise ValueError("invalid input")  # Raise an error if the input type is neither 'email' nor 'credit_card'

# Testing the function with an email and credit card input
print(mask("ashutosh@gmail.com", "email"))  # Expected output: a*******@gmail.com
print(mask("1234 5678 9101 1121", "credit_card"))  # Expected output: ************1121

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
# Initialize an empty playlist
playlist = []

# Function to add songs to the playlist
def add_songs():
    # Ask the user to input song titles separated by commas, split them by ", " to get a list of songs
    songs = input("Enter song titles separated by commas: ").split(", ")
    # Extend the current playlist with the list of new songs
    playlist.extend(songs)

# Function to remove a song from the playlist
def remove_song():
    # Ask the user for the song they want to remove
    song = input("Enter song to remove: ")
    try:
        # Attempt to remove the song from the playlist
        playlist.remove(song)
    except ValueError:
        # If the song is not found, inform the user
        print("Song not found!")

# Function to view the current playlist
def view_songs():
    # Print the playlist to show all songs in it
    print(playlist)

# Function to display a slice of the playlist
def slice_playlist():
    # Get the start index for slicing from the user
    start = int(input("Enter start index: "))
    # Get the end index for slicing from the user
    end = int(input("Enter end index: "))
    # Print the playlist items between the start and end indices
    print(playlist[start:end])

# Example usage

add_songs()  # Prompts the user to enter songs to add to the playlist
view_songs()  # Displays the current playlist
remove_song()  # Prompts the user to enter a song to remove from the playlist
view_songs()  # Displays the updated playlist after removal
slice_playlist()  # Prompts the user for a start and end index, then shows the sliced playlist


# other like extend method
# append("Song 1"): Adds "Song 1" to the playlist.
# insert(1, "Song 2"): Inserts "Song 2" at index 1.
# + ["Song 3"]: Concatenates ["Song 3"] to the playlist.
# *= 2: Repeats the entire playlist twice.
# List comprehension: Adds "(Remix)" to each song in the playlist.
# += ["Song 4", "Song 5"]: Adds two more songs to the playlist.
# extend(["Song 6", "Song 7"]): Adds even more songs to the playlist

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
#count
print(shopping_cart.count('mouse'))
#index
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
    vowels = "aeiouAEIOU"  # Define vowels
    result = ""  # Initialize an empty string to build the result
    
    # Iterate through each character in the input text
    for char in text:
        if char in vowels:
            result += "abc"  # Replace vowel with "abc"
        else:
            result += char  # Keep the character unchanged
            
    return result  # Return the final translated string

# Example usage
print(translate("This is fun"))  # Output: "Thabcs abcs fabcn"

```

---
### Assignment 9: Online Food Management System
**Question**: Create a class `FoodItem` with attributes name, price, and category, and a method to display food item details.  
**Description**: Implement object-oriented programming to manage food items.

**Python Answer**:
```python
class FoodItem:
    # Initializer method to create a new instance of FoodItem
    def __init__(self, name, price, category):
        self.name = name          # Set the name attribute of the food item
        self.price = price        # Set the price attribute of the food item
        self.category = category  # Set the category attribute of the food item

    # Method to display the information about the food item
    def display_info(self):
        # Print the details of the food item in a formatted string
        print(f"Food Item: {self.name}, Price: {self.price}, Category: {self.category}")

# Example usage of the FoodItem class
item = FoodItem("Pizza", 12.99, "Main Course")  
# Create a new FoodItem instance with name, price, and category
item.display_info()  
# Call the display_info method to print: Food Item: Pizza, Price: 12.99, Category: Main Course
e


# OOP Concepts:
# Class and Object: FoodItem is a class; item is an instance representing a specific food item.
# Encapsulation: Combines attributes and methods into a single unit, protecting data.
# Attributes and Methods: Stores item details and defines behavior (e.g., display_info).
# Abstraction: Hides complexity while providing a simple interface.
# Reusability: Allows creating multiple food items easily.
# Summary:
# The FoodItem class utilizes OOP principles to represent food items with organized and reusable code.

```

---

### Assignment 10: Regular Expressions and CSV
**Question**: Assignment 10: 
• Read a csv file which has a records in the format : 
#unitid=1#temp=38#datetime=2024-09-21T15:30:00
• Create a regular expression for extracting datetime component 
• Split datetime component into date and time components for each record 
in each row. 
• Create a new csv file with the format 
#unitid=1#temp=38#date=2024-09-21#time=15:30:00
Note: Use CSV methods to read and write to CSV file.  
**Description**: Read from and write to a CSV file with updated formats.

**Python Answer**:
```python
import csv
import re

# Step 1: Create the input CSV file
with open('input.csv', 'w', newline='') as file:
    writer = csv.writer(file)
    writer.writerow(['#unitid=1#temp=38#datetime=2024-09-21T15:30:00'])
    writer.writerow(['#unitid=2#temp=40#datetime=2024-09-22T16:45:00'])
    writer.writerow(['#unitid=3#temp=37#datetime=2024-09-23T14:15:00'])

# Step 2: Process the CSV file
def process_csv(input_file, output_file):
    # Regular expression to extract datetime
    datetime_pattern = r'datetime=(\d{4}-\d{2}-\d{2})T(\d{2}:\d{2}:\d{2})'
    
    with open(input_file, 'r') as infile, open(output_file, 'w', newline='') as outfile:
        reader = csv.reader(infile)
        writer = csv.writer(outfile)
        
        for row in reader:
            for entry in row:
                # Use regex to find the datetime pattern
                match = re.search(datetime_pattern, entry)
                if match:
                    date, time = match.groups()  # Extract date and time
                    # Replace datetime with date and time in the required format
                    new_entry = re.sub(datetime_pattern, f'date={date}#time={time}', entry)
                    writer.writerow([new_entry])  # Write the modified entry to output CSV

# Run the process
process_csv('input.csv', 'output.csv')

```

---

### Assignment 11: Capitalize Words in a List
**Question**: Use a lambda function with `map()` to capitalize the first letter of each word in a list.  
**Description**: Given a list of words, return the list with capitalized words.

**Python Answer**:
```python
# Step 1: Create a list of words
words = ['apple', 'banana', 'cherry']

# Step 2: Use map with a lambda function to capitalize the first letter of each word
# - 'map()' applies the lambda function to each element in 'words'.
# - The lambda function takes one argument 'x' (each word) and calls the 'capitalize()' method on it.
# - 'capitalize()' returns the word with the first character in uppercase and the rest in lowercase.
capitalized_words = list(map(lambda x: x.capitalize(), words))

# Example output
# - Print the list of capitalized words.
# - The expected output is ['Apple', 'Banana', 'Cherry'].
print(capitalized_words)  # Output: ['Apple', 'Banana', 'Cherry']

```

---

### Assignment 12: Find the Length of Strings
**Question**: Use a lambda function with `map()` to find the length of each string in a list.  
**Description**: Given a list of strings, return a list with their lengths.

**Python Answer**:
```python
# Step 1: Create a list of strings
strings = ['hello', 'world', 'python']

# Step 2: Use map with a lambda function to find lengths of each string
# - 'map()' applies the lambda function to each element in 'strings'.
# - The lambda function takes one argument 'x' and returns the length of 'x' using 'len(x)'.
lengths = list(map(lambda x: len(x), strings))

# Example output
# - Print the list of lengths for each string in 'strings'.
# - The expected output is [5, 5, 6], corresponding to the lengths of "hello", "world", and "python".
print(lengths)  # Output: [5, 5, 6]

```

---

### Assignment 13: Build a URL Shortener
**Question**: Define a class `URLShortener` to manage URL shortening, where each original URL is assigned a shortened version.  
**Description**: Implement functionality to add and display shortened URLs.

**Python Answer**:
```python
class URLShortener:
    # Class variable to store the mapping of original URLs to shortened URLs
    url_dict = {}
    # Base URL for the shortened URLs
    base_url = "http://short.url/"
    
    def add_url(self, original_url):
        # Check if the original URL is already in the dictionary
        if original_url in self.url_dict:
            # If it exists, print the corresponding shortened URL
            print(f"URL already exists: {self.url_dict[original_url]}")
            return self.url_dict[original_url]  # Return the existing shortened URL
        else:
            # If it doesn't exist, create a new shortened URL
            # The new shortened URL is generated based on the current number of entries in the dictionary
            shortened_url = self.base_url + str(len(self.url_dict) + 1)
            # Store the mapping of the original URL to the shortened URL in the dictionary
            self.url_dict[original_url] = shortened_url
            return shortened_url  # Return the newly created shortened URL

# Example usage
shortener = URLShortener()  # Create an instance of URLShortener
# Add a URL and print the shortened version
print(shortener.add_url("https://www.example.com"))  # Output: http://short.url/1
# Add another URL and print the shortened version
print(shortener.add_url("https://www.python.com"))   # Output: http://short.url/2

```

---
