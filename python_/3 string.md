# Strings in Python

## Overview
Strings are sequences of characters used to represent text. They can be created using single, double, or triple quotes.

## Properties
- **Immutable**: Strings cannot be changed after creation. Operations return new strings.


## String Creation
- **Single Quotes**: `'quote'`
- **Double Quotes**: `"double quote"`
- **Triple Quotes**: `"""triple quotes"""` (useful for multi-line strings)

## String Indexing
- **Access Characters**: Use indexing to access individual characters.
  ```python
  str = "Hello"
  char = str[1]  # 'e'
  ```

## String Slicing
- **Extract Substrings**: Use slicing to get a substring from the string.
  ```python
  substring = str[1:4]  # 'ell'
  ```

## String Concatenation
- **Combine Strings**: Use the `+` operator to concatenate strings.
  ```python
  combined = "Hello" + " " + "World"  # 'Hello World'
  ```

## String Repetition
- **Repeat Strings**: Use the `*` operator to repeat a string.
  ```python
  repeated = "Hi! " * 3  # 'Hi! Hi! Hi! '
  ```

## String Length
- **Get Length**: Use `len()` to find the length of a string.
  ```python
  length = len(str)  # 5
  ```

## String Membership
- **Check Presence**: Use `in` or `not in` to check for substring presence.
  ```python
  exists = "H" in str  # True
  ```

## String Methods
- **Common Methods**:
  - `upper()`: Converts to uppercase.
    ```python
    str.upper()  # 'HELLO'
    ```
  - `lower()`: Converts to lowercase.
    ```python
    str.lower()  # 'hello'
    ```
  - `capitalize()`: Capitalizes the first letter.
    ```python
    str.capitalize()  # 'Hello'
    ```
  - `title()`: Capitalizes the first letter of each word.
    ```python
    str.title()  # 'Hello'
    ```


# String Operations in Python

## 1. Stripping Whitespace
- **`strip()`**: Removes leading and trailing whitespace.
  ```python
  text = "  Hello  "
  stripped = text.strip()  # 'Hello'
  ```
- **`lstrip()`**: Removes leading whitespace.
  ```python
  left_stripped = text.lstrip()  # 'Hello  '
  ```
- **`rstrip()`**: Removes trailing whitespace.
  ```python
  right_stripped = text.rstrip()  # '  Hello'
  ```

## 2. Finding and Replacing
- **`find(sub)`**: Returns the index of the first occurrence of `sub`, or -1 if not found.
  ```python
  index = "Hello".find("l")  # 2
  ```
- **`replace(old, new)`**: Replaces all occurrences of `old` with `new`.
  ```python
  new_text = "Hello".replace("l", "p")  # 'Heppo'
  ```

## 3. Splitting and Joining
- **`split(delimiter)`**: Splits the string into a list based on the delimiter.
  ```python
  words = "Hello World".split()  # ['Hello', 'World']
  ```
- **`join(iterable)`**: Joins elements of an iterable into a single string, using the string as a separator.
  ```python
  sentence = " ".join(['Hello', 'World'])  # 'Hello World'
  ```

## 4. Checking String Properties
- **`startswith(prefix)`**: Checks if the string starts with the specified prefix.
  ```python
  is_start = "Hello".startswith("He")  # True
  ```
- **`endswith(suffix)`**: Checks if the string ends with the specified suffix.
  ```python
  is_end = "Hello".endswith("lo")  # True
  ```
- **`isalpha()`**: Returns True if all characters are alphabetic.
- **`isdigit()`**: Returns True if all characters are digits.
- **`isalnum()`**: Returns True if all characters are alphanumeric.

## 5. String Formatting
- **f-Strings**: Format strings using `{}` for variable interpolation.
  ```python
  name = "Alice"
  greeting = f"Hello, {name}!"  # 'Hello, Alice!'
  ```
- **`format()`**: Another method for formatting strings.
  ```python
  formatted = "Hello, {}".format(name)  # 'Hello, Alice!'
  ```
- **`%` operator**: Old-style formatting.
  ```python
  formatted = "Hello, %s" % name  # 'Hello, Alice!'
  ```

## 6. Escaping Characters
- **Backslash (`\`)**: Used to escape special characters within strings.
  ```python
  escaped = "He said, \"Hello!\""  # 'He said, "Hello!"'
  ```

