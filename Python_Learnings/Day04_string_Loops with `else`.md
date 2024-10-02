
### **Hands-On Assignments**

#### **Assignment 1:**
Ask the user for a number and print those many stars on the console.  
Ask the user for ‘Y’ or ‘N’ to continue:  
- If ‘Y’, ask for another number.  
- Else, exit.

**Solution**:
```python
while True:
    num = int(input("Enter a number: "))
    print("*" * num)
    
    choice = input("Do you want to enter another number? (Y/N): ").upper()
    if choice == 'N':
        break
```

---

### **String Operations**  
**File: stringOperations.py**

- String Creation
- `'quote'`
- `"double quote"`
- `"""triple quotes"""`

- **String Indexing**: `str[index]`
- **String Slicing**: `str[start index : last index]`
- **String Concatenation**: `'+' operator`
- **String Repetition**: `str * 3`
- **String Length**: `len(str)`
- **String Membership**: `'in', 'not in'`

**String Methods**:
- `upper()`
- `lower()`
- `capitalize()`
- `title()`

---

### **More String Operations**  
- **Checking String Properties**:  
  `startswith()`, `endswith()`, `isalpha()`, `isdigit()`, `isalnum()`

- **String Formatting**:  
  f-Strings, `format()`, `% operator`

- **Escaping Characters**:  
  `'\ '`

- **Stripping Whitespace**:  
  `strip()`, `lstrip()`, `rstrip()`

- **Finding and Replacing**:  
  `find()`, `replace()`

- **Splitting and Joining**:  
  `split()`, `join()`

---

### **Hands-On Assignments**

#### **Assignment 1:**
Use the `strip()` function to remove leading/trailing whitespace.

**Solution**:
```python
text = "  Hello, World!  "
print(text.strip())
```

---

#### **Assignment 2:**
Accept 2 strings from the user and concatenate them.  
Calculate the length of the resulting string.

**Solution**:
```python
str1 = input("Enter first string: ")
str2 = input("Enter second string: ")
result = str1 + str2
print(f"Concatenated string: {result}")
print(f"Length of the resulting string: {len(result)}")
```

---

#### **Assignment 3:**
Accept 2 strings from the user and compare them.  
Ask if the user wants to compare more strings. If yes, ask for 2 more strings, else exit.

**Solution**:
```python
while True:
    str1 = input("Enter first string: ")
    str2 = input("Enter second string: ")
    
    if str1 == str2:
        print("Strings are equal.")
    else:
        print("Strings are not equal.")
    
    choice = input("Do you want to compare more strings? (Y/N): ").upper()
    if choice == 'N':
        break
```

---

### **More Hands-On Assignments**

#### **Assignment 5:**
Use `find()` and `replace()` for:  
- Find the first occurrence of a substring – `text.find(substring)`
- Replace all occurrences of a substring – `text.replace(old, new)`
- Replace the first occurrence of a substring – `text.replace(old, new, 1)`

**Solution**:
```python
text = "The quick brown fox jumps over the lazy dog."
print("First occurrence of 'the':", text.find("the"))

new_text = text.replace("the", "a")
print("Replaced all 'the' with 'a':", new_text)

first_replace = text.replace("the", "a", 1)
print("Replaced first occurrence of 'the':", first_replace)
```

---

#### **Assignment 6:**  
Extract the 3rd letter of a string.

**Solution**:
```python
text = input("Enter a string: ")
if len(text) >= 3:
    print(f"The 3rd letter is: {text[2]}")
else:
    print("String is too short.")
```

---

#### **Assignment 7:**  
Extract letters from the 3rd to the 8th index of a string.

**Solution**:
```python
text = input("Enter a string: ")
print(f"Extracted letters (3-8): {text[2:8]}")
```

---

#### **Assignment 8:**  
Remove the 1st and last letter of a string.

**Solution**:
```python
text = input("Enter a string: ")
if len(text) > 2:
    result = text[1:-1]
    print(f"String without first and last letter: {result}")
else:
    print("String is too short.")
```

---

#### **Assignment 9:**  
Accept a string from the user (lowercase) and convert it to uppercase.

**Solution**:
```python
text = input("Enter a lowercase string: ")
print(f"Uppercase version: {text.upper()}")
```

---

### **Hands-On: Splitting a Sentence**

#### **Assignment 9:**  
Use `split()` for:  
- Splitting a string into words – `split()`
- Splitting a string by a custom delimiter – `split(delimiter)`

**Solution**:
```python
text = "Python is fun"
words = text.split()
print(f"Words in the sentence: {words}")

csv_text = "apple,banana,cherry"
fruits = csv_text.split(',')
print(f"Fruits: {fruits}")
```

---

### **Homework**

#### **Assignment 10:**  
Write a program that checks whether a given string is a palindrome (reads the same backward as forward).

**Input**:
- Prompt the user to enter a string.

**Logic**:
- Remove any spaces and convert the string to lowercase.
- Check if the string reads the same forward and backward.

**Output**:
- Display whether the string is a palindrome.

**Solution**:
```python
text = input("Enter a string: ").replace(" ", "").lower()
if text == text[::-1]:
    print("The string is a palindrome.")
else:
    print("The string is not a palindrome.")
```

