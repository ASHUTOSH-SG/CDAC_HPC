# Lists in Python

## Overview
Lists are versatile data structures that store an ordered collection of items.

## Key Characteristics

- **Mutable**: Lists can be modified after creation (e.g., items can be added, removed, or changed).
- **Heterogeneous**: Can hold elements of different data types (e.g., integers, strings, objects).
- **Duplicates**: Allows duplicate items, meaning the same value can appear multiple times.
- **Order**: Maintains the order of insertion, so the order of elements is preserved.

## Example
```python
my_list = [1, "apple", 3.14, "banana", 1]  # A list with mixed data types and duplicates
```

# List Operations in Python

## Basic List Creation
- **Creation**: 
  ```python
  empty_list = []
  ```

## Accessing List Elements
- **Indexing**: Access elements using an index.
  ```python
  element = my_list[index]
  ```
- **Slicing**: Extract a sublist using slicing.
  ```python
  sublist = my_list[startInd:endInd]
  ```

## Modifying Lists
- **Modifying an Element**: Change the value at a specific index.
  ```python
  my_list[index] = new_value
  ```

## Adding Elements
- **`append(value)`**: Adds an element to the end of the list.
  ```python
  my_list.append(4)
  ```
- **`insert(index, value)`**: Inserts an element at a specific index.
  ```python
  my_list.insert(1, "banana")
  ```
- **`extend(iterable)`**: Adds multiple elements from an iterable (e.g., another list).
  ```python
  my_list.extend([5, 6])
  ```

## Removing Elements
- **`remove(value)`**: Removes the first occurrence of a value.
  ```python
  my_list.remove("banana")
  ```
- **`pop(index)`**: Removes and returns the element at the specified index (or the last element if no index is specified).
  ```python
  last_element = my_list.pop()
  ```
- **`clear()`**: Removes all elements from the list.
  ```python
  my_list.clear()
  ```

## Copying and Concatenation
- **`copy()`**: Creates a shallow copy of the list.
  ```python
  new_list = my_list.copy()
  ```
- **Concatenation**: Use the `+` operator to combine lists.
  ```python
  combined = my_list + [7, 8]
  ```
- **Repetition**: Use the `*` operator to repeat the list.
  ```python
  repeated = my_list * 2
  ```

## Membership
- **Check Membership**: Use `in` and `not in` to check for the presence of an element.
  ```python
  exists = 3 in my_list  # True or False
  ```

## Nested Lists
- **Create Nested Lists**: Lists can contain other lists.
  ```python
  nested_list = [1, [2, 3], [4, 5, 6]]
  ```

## List Methods
- **`sort()`**: Sorts the list in ascending order.
  ```python
  my_list.sort()
  ```
- **`reverse()`**: Reverses the order of elements in the list.
  ```python
  my_list.reverse()
  ```
- **`index(value)`**: Returns the index of the first occurrence of a value.
  ```python
  index_of_value = my_list.index(2)
  ```
- **`count(value)`**: Returns the number of occurrences of a value.
  ```python
  count_of_value = my_list.count(1)
  ```



# Working with Lists in Python

# Create a list
```
my_list = [1, "apple", 3.14, "banana", 1]
```

# Accessing elements
```
print("First element:", my_list[0])          # Output: 1
print("Sliced list:", my_list[1:4])          # Output: ['apple', 3.14, 'banana']
```

# Modifying an element
```
my_list[2] = "orange"
print("Modified list:", my_list)              # Output: [1, 'apple', 'orange', 'banana', 1]
```

# Adding elements
```
my_list.append(4)
print("After appending 4:", my_list)          # Output: [1, 'apple', 'orange', 'banana', 1, 4]
my_list.insert(1, "grape")
print("After inserting 'grape':", my_list)    # Output: [1, 'grape', 'apple', 'orange', 'banana', 1, 4]
my_list.extend([5, 6])
print("After extending with [5, 6]:", my_list) # Output: [1, 'grape', 'apple', 'orange', 'banana', 1, 4, 5, 6]
```

# Removing elements
```
my_list.remove("banana")
print("After removing 'banana':", my_list)    # Output: [1, 'grape', 'apple', 'orange', 1, 4, 5, 6]
last_element = my_list.pop()
print("After popping last element:", my_list, "| Popped:", last_element)  # Output: [1, 'grape', 'apple', 'orange', 1, 4, 5] | Popped: 6
```
# Copying the list
```
new_list = my_list.copy()
print("Copied list:", new_list)                # Output: [1, 'grape', 'apple', 'orange', 1, 4, 5]
```
# Concatenation and repetition
```
combined = my_list + [7, 8]
print("Concatenated list:", combined)          # Output: [1, 'grape', 'apple', 'orange', 1, 4, 5, 7, 8]
repeated = my_list * 2
print("Repeated list:", repeated)               # Output: [1, 'grape', 'apple', 'orange', 1, 4, 5, 1, 'grape', 'apple', 'orange', 1, 4, 5]
```
# Checking membership
```
exists = 3 in my_list
print("Is 3 in my_list?", exists)              # Output: False
```
# Nested list
```
nested_list = [1, [2, 3], [4, 5, 6]]
print("Nested list:", nested_list)              # Output: [1, [2, 3], [4, 5, 6]]
```

# List methods
```
my_list.sort()
print("Sorted list:", my_list)                  # Output: [1, 1, 4, 'apple', 'grape', 'orange']
my_list.reverse()
print("Reversed list:", my_list)                # Output: ['orange', 'grape', 'apple', 4, 1, 1]
index_of_value = my_list.index('apple')
print("Index of 'apple':", index_of_value)      # Output: 2
count_of_value = my_list.count(1)
print("Count of 1:", count_of_value)            # Output: 2
```