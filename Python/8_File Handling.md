
# File Handling in Python

## Overview
File handling allows you to read from and write to files, enabling data storage and retrieval.

## Opening a File
Use the `open()` function with the desired mode:

- **Modes**:
  - `'r'`: Read mode.
  - `'w'`: Write mode (creates or truncates a file).
  - `'a'`: Append mode.
  - `'b'`: Binary mode.

### Example
```python
file = open("example.txt", "w")  # Open file for writing
```

## Closing a File
Always close a file to free resources.
```python
file.close()  # Close the file
```

## Checking if a File Exists
Use `os.path.exists()` to check file existence.
```python
import os
exists = os.path.exists("example.txt")  # Returns True or False
```

## Writing to a File
- **Write a String**:
```python
file = open("example.txt", "w")
file.write("Hello, World!")  # Write a string
```
- **Write Multiple Strings**:
```python
lines = ["Line 1\n", "Line 2\n"]
file.writelines(lines)  # Write a list of strings
```

## Reading a File
- **Read the Entire File**:
```python
file = open("example.txt", "r")
content = file.read()  # Read the whole file
```
- **Read One Line**:
```python
line = file.readline()  # Read the next line
```
- **Read All Lines**:
```python
lines = file.readlines()  # Read all lines into a list
```

## Summary
File handling in Python involves opening, reading, writing, and closing files using various modes. Proper file management ensures efficient data handling and resource utilization.



# Working with CSV Files in Python

## Overview
The `csv` module in Python provides functionality to read from and write to CSV files, making it easy to handle tabular data.

## Importing the CSV Module
```python
import csv
```

## Methods in the `csv` Module

### 1. `csv.reader()`
Reads a CSV file and returns a reader object, which can be iterated over to access rows.

#### Example
```python
with open("example.csv", "r") as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)  # Prints each row as a list
```

### 2. `csv.DictReader()`
Reads a CSV file and maps the data into a dictionary where the keys are taken from the first row of the file.

#### Example
```python
with open("example.csv", "r") as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(row)  # Prints each row as a dictionary
```

### 3. `csv.writer()`
Creates a writer object to write data to a CSV file.

#### Example
```python
data = [
    ["Name", "Age", "City"],
    ["Alice", 30, "New York"],
    ["Bob", 25, "Los Angeles"]
]

with open("example.csv", "w", newline='') as file:
    writer = csv.writer(file)
    writer.writerows(data)  # Writes multiple rows
```

### 4. `csv.DictWriter()`
Creates a writer object that maps dictionaries to CSV rows.

#### Example
```python
data = [
    {"Name": "Alice", "Age": 30, "City": "New York"},
    {"Name": "Bob", "Age": 25, "City": "Los Angeles"}
]

with open("example_dict.csv", "w", newline='') as file:
    fieldnames = ["Name", "Age", "City"]
    writer = csv.DictWriter(file, fieldnames=fieldnames)
    writer.writeheader()  # Write header row
    writer.writerows(data)  # Writes multiple rows
```

## Summary
The `csv` module simplifies working with CSV files in Python through various methods for reading and writing data, enabling easy manipulation of tabular information.
