

### **Installing Python**
1. **Which of the following is the official website to download Python?**  
   a) www.python.com  
   b) www.python.org  
   c) www.python.net  
   d) www.python.io  
   **Answer**: b) www.python.org  
   **Explanation**: Python is officially available for download at www.python.org.

2. **Which of the following commands is used to check the Python version in the terminal?**  
   a) `python --version`  
   b) `python -v`  
   c) `version python`  
   d) `python version`  
   **Answer**: a) `python --version`  
   **Explanation**: The `--version` flag is used to check the installed Python version.

---

### **Introduction to Python**
3. **Python was developed by which of the following?**  
   a) Guido van Rossum  
   b) James Gosling  
   c) Dennis Ritchie  
   d) Bjarne Stroustrup  
   **Answer**: a) Guido van Rossum  
   **Explanation**: Python was created by Guido van Rossum in 1991.

4. **Which of the following is not a feature of Python?**  
   a) Easy to learn and use  
   b) Dynamically typed  
   c) Platform-dependent  
   d) Open-source  
   **Answer**: c) Platform-dependent  
   **Explanation**: Python is platform-independent, meaning it can run on multiple platforms.

---

### **Basic Syntax**
5. **Which symbol is used to start a comment in Python?**  
   a) `//`  
   b) `#`  
   c) `/*`  
   d) `<!--`  
   **Answer**: b) `#`  
   **Explanation**: Comments in Python begin with the `#` symbol.

6. **Which of the following is the correct way to print "Hello, World!" in Python?**  
   a) `print "Hello, World!"`  
   b) `echo "Hello, World!"`  
   c) `print("Hello, World!")`  
   d) `cout << "Hello, World!";`  
   **Answer**: c) `print("Hello, World!")`  
   **Explanation**: The `print()` function is used to display output in Python.

---

### **Data Types, Variables, Operators**
7. **Which of the following is a mutable data type in Python?**  
   a) Tuple  
   b) String  
   c) List  
   d) Integer  
   **Answer**: c) List  
   **Explanation**: Lists in Python are mutable, meaning their contents can be changed after creation.

8. **What is the output of `10 / 3` in Python?**  
   a) 3  
   b) 3.33  
   c) 3.0  
   d) None of the above  
   **Answer**: b) 3.33  
   **Explanation**: The `/` operator performs floating-point division.

9. **Which operator is used to calculate the remainder in Python?**  
   a) `/`  
   b) `*`  
   c) `%`  
   d) `//`  
   **Answer**: c) `%`  
   **Explanation**: The `%` operator is used to calculate the remainder of a division.

---

### **Input/Output**
10. **What is the correct syntax to take input from the user in Python 3?**  
    a) `input()`  
    b) `raw_input()`  
    c) `scan()`  
    d) `read()`  
    **Answer**: a) `input()`  
    **Explanation**: The `input()` function is used to read input from the user in Python 3.

11. **What will the following code output?**  
    ```python
    name = input("Enter your name: ")
    print("Hello", name)
    ```  
    a) Enter your name:  
    b) Error  
    c) Hello (user input)  
    d) None of the above  
    **Answer**: c) Hello (user input)  
    **Explanation**: The code reads the input and prints it with "Hello".

---

### **Declaring Variables and Data Types**
12. **Which of the following is the correct way to declare a variable in Python?**  
    a) `int x = 10`  
    b) `x := 10`  
    c) `x = 10`  
    d) `declare x = 10`  
    **Answer**: c) `x = 10`  
    **Explanation**: Variables in Python are declared by assigning values using `=`.

13. **Which data type is used to store True or False values?**  
    a) Int  
    b) Float  
    c) Str  
    d) Bool  
    **Answer**: d) Bool  
    **Explanation**: The `bool` type is used for storing boolean values.

---

### **Your First Python Program**
14. **What will the following code output?**  
    ```python
    print("Python is fun!")
    ```  
    a) Python is fun!  
    b) "Python is fun!"  
    c) Error  
    d) None of the above  
    **Answer**: a) Python is fun!  
    **Explanation**: The `print()` function outputs the text exactly as given, without quotes.

15. **What happens if you run a Python script without saving it first?**  
    a) It runs without saving  
    b) It throws an error  
    c) It is automatically saved in memory  
    d) None of the above  
    **Answer**: b) It throws an error  
    **Explanation**: Python scripts need to be saved with a `.py` extension to execute properly.

---

### **Flow of Control (Modules, Branching)**
16. **Which keyword is used to import modules in Python?**  
    a) `import`  
    b) `include`  
    c) `require`  
    d) `module`  
    **Answer**: a) `import`  
    **Explanation**: The `import` keyword is used to bring external modules into a Python program.

17. **What is the output of the following code?**  
    ```python
    x = 10
    if x > 5:
        print("Greater")
    else:
        print("Smaller")
    ```  
    a) Smaller  
    b) Greater  
    c) Error  
    d) None of the above  
    **Answer**: b) Greater  
    **Explanation**: Since `x = 10` is greater than 5, the `if` condition is satisfied.

18. **Which of the following is correct syntax for a nested if-else statement in Python?**  
    a)  
    ```python
    if condition1:
        if condition2:
            statement
        else:
            statement
    ```  
    b)  
    ```python
    if condition1:
    else:
        if condition2:
            statement
    ```  
    c) Both a and b  
    d) None of the above  
    **Answer**: a)  
    **Explanation**: Nested `if-else` requires proper indentation in Python.

---

### **Looping: For, While**
19. **What is the output of the following code?**  
    ```python
    for i in range(3):
        print(i)
    ```  
    a) 0 1 2  
    b) 1 2 3  
    c) 0 1 2 3  
    d) Error  
    **Answer**: a) 0 1 2  
    **Explanation**: The `range(3)` generates numbers from 0 to 2 (exclusive of 3).

20. **Which of the following is an infinite loop?**  
    a)  
    ```python
    while True:
        print("Looping")
    ```  
    b)  
    ```python
    for i in range(5):
        print(i)
    ```  
    c)  
    ```python
    while False:
        print("Never prints")
    ```  
    d) None of the above  
    **Answer**: a)  
    **Explanation**: The `while True` loop runs indefinitely unless explicitly broken.

---

### **Nested Loops**
21. **What is the output of the following code?**  
    ```python
    for i in range(2):
        for j in range(2):
            print(i, j)
    ```  
    a) 0 0 1 1  
    b) 0 1 1 0  
    c) 0 0 0 1 1 0 1 1  
    d) 0 0 0 1 1 0 1 1  
    **Answer**: d) 0 0 0 1 1 0 1 1  
    **Explanation**: The nested loop iterates over each pair `(i, j)` in the ranges.

22. **How many times will the inner loop execute in the following code?**  
    ```python
    for i in range(3):
        for j in range(4):
            print(i, j)
    ```  
    a) 3  
    b) 4  
    c) 7  
    d) 12  
    **Answer**: d) 12  
    **Explanation**: The outer loop runs 3 times, and the inner loop runs 4 times for each iteration, totaling 3 × 4 = 12.

---

### **Control Structure**
23. **Which of the following is not a control structure in Python?**  
    a) Looping  
    b) Branching  
    c) Sequencing  
    d) Arrays  
    **Answer**: d) Arrays  
    **Explanation**: Control structures manage the flow of a program and do not include arrays.

24. **What will the following code do?**  
    ```python
    if True:
        print("Executed")
    ```  
    a) It will print "Executed"  
    b) It will throw an error  
    c) It will do nothing  
    d) None of the above  
    **Answer**: a) It will print "Executed"  
    **Explanation**: The condition is `True`, so the `if` block is executed.

---

### **Uses of Break & Continue**
25. **What is the purpose of the `break` statement in Python?**  
    a) Skips to the next iteration of the loop  
    b) Exits the loop entirely  
    c) Stops the program  
    d) None of the above  
    **Answer**: b) Exits the loop entirely  
    **Explanation**: The `break` statement terminates the loop and transfers control to the statement following the loop.

26. **What will the following code do?**  
    ```python
    for i in range(5):
        if i == 3:
            continue
        print(i)
    ```  
    a) 0 1 2 4  
    b) 0 1 2 3 4  
    c) 0 1 4  
    d) Error  
    **Answer**: a) 0 1 2 4  
    **Explanation**: The `continue` statement skips the iteration when `i == 3`.

---

### **More Questions from Session 1 Syllabus**

---

### **Installing Python**
27. **Which of the following IDEs is commonly used for Python development?**  
    a) IntelliJ IDEA  
    b) PyCharm  
    c) Eclipse  
    d) NetBeans  
    **Answer**: b) PyCharm  
    **Explanation**: PyCharm is a popular IDE specifically designed for Python development.

28. **What is the extension of a Python file?**  
    a) `.py`  
    b) `.pyth`  
    c) `.python`  
    d) `.pyn`  
    **Answer**: a) `.py`  
    **Explanation**: Python files are saved with the `.py` extension.

---

### **Introduction to Python**
29. **Which of the following statements is correct about Python?**  
    a) Python is a high-level programming language.  
    b) Python supports both procedural and object-oriented programming.  
    c) Python has dynamic typing.  
    d) All of the above.  
    **Answer**: d) All of the above.  
    **Explanation**: Python is a versatile, high-level language supporting multiple paradigms and dynamic typing.

30. **Which of the following is not a valid Python keyword?**  
    a) `try`  
    b) `class`  
    c) `goto`  
    d) `lambda`  
    **Answer**: c) `goto`  
    **Explanation**: Python does not support the `goto` statement.

---

### **Basic Syntax**
31. **Which of the following is valid in Python?**  
    a) `x = 10 y = 20`  
    b) `x, y = 10, 20`  
    c) `int x = 10; y = 20;`  
    d) None of the above  
    **Answer**: b) `x, y = 10, 20`  
    **Explanation**: Python supports unpacking assignment syntax for multiple variables.

32. **What is the output of the following code?**  
    ```python
    print("Hello", "World", sep="-")
    ```  
    a) Hello World  
    b) Hello-World  
    c) Hello- World  
    d) Hello, World  
    **Answer**: b) Hello-World  
    **Explanation**: The `sep` argument specifies the separator between values in the `print()` function.

---

### **Data Types, Variables, Operators**
33. **Which of the following data types is immutable in Python?**  
    a) List  
    b) Dictionary  
    c) Set  
    d) Tuple  
    **Answer**: d) Tuple  
    **Explanation**: Tuples are immutable, meaning their elements cannot be modified.

34. **What is the result of the following operation?**  
    ```python
    print(2 ** 3)
    ```  
    a) 6  
    b) 8  
    c) 9  
    d) 12  
    **Answer**: b) 8  
    **Explanation**: The `**` operator performs exponentiation, so `2 ** 3 = 2 × 2 × 2 = 8`.

35. **Which of the following is not a Python operator?**  
    a) `is`  
    b) `in`  
    c) `between`  
    d) `not`  
    **Answer**: c) `between`  
    **Explanation**: Python does not have a `between` operator.

---

### **Input/Output**
36. **Which of the following will take integer input from the user?**  
    a) `x = input()`  
    b) `x = int(input())`  
    c) `x = raw_input()`  
    d) None of the above  
    **Answer**: b) `x = int(input())`  
    **Explanation**: The `int()` function converts the string input from `input()` into an integer.

37. **What will the following code print?**  
    ```python
    name = input("Enter your name: ")
    age = int(input("Enter your age: "))
    print(f"{name} is {age} years old")
    ```  
    User inputs: `John` and `25`.  
    a) John is 25 years old  
    b) Error  
    c) Name: John, Age: 25  
    d) None of the above  
    **Answer**: a) John is 25 years old  
    **Explanation**: The `f-string` in Python interpolates the variables into the string.

---

### **Looping**
38. **What is the output of the following code?**  
    ```python
    for i in range(5, 1, -1):
        print(i, end=", ")
    ```  
    a) 5, 4, 3, 2,  
    b) 5, 4, 3, 2, 1,  
    c) 1, 2, 3, 4, 5,  
    d) Error  
    **Answer**: a) 5, 4, 3, 2,  
    **Explanation**: The `range(5, 1, -1)` generates numbers from 5 to 2 (inclusive) in reverse order.

39. **Which loop is better for iterating over a sequence in Python?**  
    a) For  
    b) While  
    c) Both are equally good  
    d) None of the above  
    **Answer**: a) For  
    **Explanation**: The `for` loop is specifically designed for iterating over sequences.

---

### **Break & Continue**
40. **What is the purpose of the `continue` statement?**  
    a) Terminates the loop  
    b) Skips the rest of the current iteration and goes to the next iteration  
    c) Exits the program  
    d) None of the above  
    **Answer**: b) Skips the rest of the current iteration and goes to the next iteration  
    **Explanation**: The `continue` statement skips the remaining code in the loop for the current iteration.

41. **What is the output of the following code?**  
    ```python
    for i in range(5):
        if i == 3:
            break
        print(i)
    ```  
    a) 0 1 2  
    b) 0 1 2 3  
    c) Error  
    d) None of the above  
    **Answer**: a) 0 1 2  
    **Explanation**: The `break` statement exits the loop when `i == 3`.

---### **More Questions from Session 1 Syllabus**

---

### **Flow of Control (Modules, Branching)**
42. **Which module in Python is used to work with the operating system?**  
    a) `sys`  
    b) `os`  
    c) `platform`  
    d) `time`  
    **Answer**: b) `os`  
    **Explanation**: The `os` module provides functions to interact with the operating system, such as creating directories or fetching environment variables.

43. **What is the output of the following code?**  
    ```python
    x = 10
    if x > 5:
        print("Greater")
    elif x == 5:
        print("Equal")
    else:
        print("Smaller")
    ```  
    a) Greater  
    b) Equal  
    c) Smaller  
    d) Error  
    **Answer**: a) Greater  
    **Explanation**: The condition `x > 5` is true, so "Greater" is printed.

44. **Which of the following is a valid conditional expression in Python?**  
    a) `x > y and z < 5`  
    b) `x or y == 10`  
    c) `not x and y`  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: All options are valid because Python supports logical operators such as `and`, `or`, and `not`.

---

### **If, If-Else, Nested If-Else**
45. **What will the following code print?**  
    ```python
    x = 3
    y = 5
    if x < y:
        if x % 2 == 0:
            print("Even and Smaller")
        else:
            print("Odd and Smaller")
    else:
        print("Greater")
    ```  
    a) Even and Smaller  
    b) Odd and Smaller  
    c) Greater  
    d) None of the above  
    **Answer**: b) Odd and Smaller  
    **Explanation**: Since `x = 3` and `3 < 5`, the nested condition checks if `3 % 2 == 0`, which is false, so "Odd and Smaller" is printed.

46. **Which of the following will result in a syntax error?**  
    a) `if x > y:`  
    b) `if (x > y)`  
    c) `if x > y`  
    d) `if x > y then:`  
    **Answer**: d) `if x > y then:`  
    **Explanation**: Python does not use the keyword `then` in conditional statements.

---

### **Looping (For, While, Nested Loops)**
47. **What is the output of the following code?**  
    ```python
    for i in range(2):
        for j in range(2):
            print(i, j)
    ```  
    a) 0 0  
       0 1  
       1 0  
       1 1  
    b) 0 1  
       1 0  
       1 1  
    c) 0 0  
       0 1  
       1 0  
    d) None of the above  
    **Answer**: a) 0 0  
                   0 1  
                   1 0  
                   1 1  
    **Explanation**: The nested loop iterates over all combinations of `i` and `j` in their respective ranges.

48. **Which of the following loop structures always executes at least once?**  
    a) `for`  
    b) `while`  
    c) `do-while`  
    d) None of the above  
    **Answer**: c) `do-while`  
    **Explanation**: Python does not have a `do-while` loop, but in languages where it exists, it guarantees at least one execution.

---

### **Control Structure**
49. **What is the purpose of the `pass` statement in Python?**  
    a) To skip the rest of a loop iteration  
    b) To exit from a loop or function  
    c) To act as a placeholder where code will eventually go  
    d) None of the above  
    **Answer**: c) To act as a placeholder where code will eventually go  
    **Explanation**: The `pass` statement is used to create minimal implementations without causing errors.

50. **What is the output of the following code?**  
    ```python
    for i in range(3):
        pass
    print("Done")
    ```  
    a) Done  
    b) Error  
    c) None  
    d) Nothing is printed  
    **Answer**: a) Done  
    **Explanation**: The `pass` statement does nothing, allowing the loop to execute without errors, and "Done" is printed.

---

### **50 MCQs for Session 2**  
#### (Pass, Strings and Tuples, Accessing Strings, Basic Operations, Assigning Multiple Values at Once, Formatting Strings, String Slices)

---

### **Pass Statement**
1. **What does the `pass` statement do in Python?**  
    a) Terminates the program execution  
    b) Skips the current iteration  
    c) Acts as a placeholder for code that will be added later  
    d) Throws an exception  
    **Answer**: c) Acts as a placeholder for code that will be added later  
    **Explanation**: The `pass` statement does nothing and is used as a placeholder.

2. **Which of the following is a valid use of `pass`?**  
    ```python
    def function():
        pass
    ```  
    a) Valid  
    b) Invalid  
    **Answer**: a) Valid  
    **Explanation**: The `pass` statement allows the function to exist without raising an error.

3. **What is the output of the following code?**  
    ```python
    for i in range(3):
        if i == 1:
            pass
        print(i)
    ```  
    a) 0 1 2  
    b) 0 2  
    c) 0 1  
    d) Error  
    **Answer**: a) 0 1 2  
    **Explanation**: The `pass` statement does nothing, so all values are printed.

---

### **Strings and Tuples**
4. **Which of the following is an immutable data type in Python?**  
    a) List  
    b) Dictionary  
    c) Tuple  
    d) Set  
    **Answer**: c) Tuple  
    **Explanation**: Tuples cannot be modified after creation, unlike lists or dictionaries.

5. **Which of the following correctly creates a tuple?**  
    a) `t = 1, 2, 3`  
    b) `t = (1, 2, 3)`  
    c) `t = tuple([1, 2, 3])`  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: Tuples can be created using commas, parentheses, or the `tuple()` constructor.

6. **What is the output of the following code?**  
    ```python
    t = (1, 2, 3)
    t[1] = 5
    ```  
    a) `(1, 5, 3)`  
    b) Error  
    c) `(1, 2, 3)`  
    d) `(1, 5)`  
    **Answer**: b) Error  
    **Explanation**: Tuples are immutable, so their elements cannot be reassigned.

---

### **Accessing Strings**
7. **What is the output of the following code?**  
    ```python
    s = "Python"
    print(s[2])
    ```  
    a) `y`  
    b) `t`  
    c) `o`  
    d) Error  
    **Answer**: b) `t`  
    **Explanation**: Indexing starts at 0, so `s[2]` refers to the third character.

8. **How would you access the last character of a string `s`?**  
    a) `s[len(s)]`  
    b) `s[-1]`  
    c) `s[len(s)-1]`  
    d) Both b and c  
    **Answer**: d) Both b and c  
    **Explanation**: Negative indexing (`-1`) and `len(s)-1` both give the last character.

---

### **Basic Operations**
9. **What is the output of the following code?**  
    ```python
    s = "Hello"
    print(s * 2)
    ```  
    a) `HelloHello`  
    b) `Hello2`  
    c) `Error`  
    d) `Hello Hello`  
    **Answer**: a) `HelloHello`  
    **Explanation**: The `*` operator repeats the string.

10. **Which of the following will concatenate two strings `a` and `b`?**  
    a) `a + b`  
    b) `a . b`  
    c) `a , b`  
    d) None of the above  
    **Answer**: a) `a + b`  
    **Explanation**: The `+` operator concatenates strings.

---

### **Assigning Multiple Values at Once**
11. **What does the following code do?**  
    ```python
    x, y, z = 1, 2, 3
    ```  
    a) Assigns 1 to x, 2 to y, 3 to z  
    b) Assigns (1, 2, 3) to x  
    c) Causes an error  
    d) None of the above  
    **Answer**: a) Assigns 1 to x, 2 to y, 3 to z  
    **Explanation**: Multiple variables can be assigned in one line.

12. **What happens if the number of variables does not match the number of values?**  
    a) Assigns `None` to missing variables  
    b) Causes an error  
    c) Ignores extra values  
    d) None of the above  
    **Answer**: b) Causes an error  
    **Explanation**: The number of variables and values must match.

---

### **Formatting Strings**
13. **What is the output of the following code?**  
    ```python
    name = "John"
    age = 25
    print(f"My name is {name} and I am {age} years old.")
    ```  
    a) `My name is John and I am 25 years old.`  
    b) `Error`  
    c) `My name is {name} and I am {age} years old.`  
    d) None of the above  
    **Answer**: a) `My name is John and I am 25 years old.`  
    **Explanation**: f-strings allow inline variable substitution.

14. **Which method formats a string using placeholders?**  
    a) `str.replace()`  
    b) `str.format()`  
    c) `str.join()`  
    d) None of the above  
    **Answer**: b) `str.format()`  
    **Explanation**: The `format()` method allows placeholder substitution.

---

### **String Slices**
15. **What is the output of the following code?**  
    ```python
    s = "abcdef"
    print(s[1:4])
    ```  
    a) `abc`  
    b) `bcd`  
    c) `bcde`  
    d) Error  
    **Answer**: b) `bcd`  
    **Explanation**: The slice includes the start index and excludes the stop index.

16. **What happens if the start index in a slice is omitted?**  
    a) Assumes 0  
    b) Assumes 1  
    c) Causes an error  
    d) None of the above  
    **Answer**: a) Assumes 0  
    **Explanation**: Omitting the start index begins the slice at the start of the string.

---
### **Continued MCQs for Session 2**  

---

### **String Slices (continued)**  
17. **What does the following slice return?**  
    ```python
    s = "Python"
    print(s[:3])
    ```  
    a) `Pyt`  
    b) `hon`  
    c) `tho`  
    d) Error  
    **Answer**: a) `Pyt`  
    **Explanation**: When the start index is omitted, the slice starts from the beginning of the string.

18. **What is the output of the following slice?**  
    ```python
    s = "abcdef"
    print(s[2:])
    ```  
    a) `cdef`  
    b) `abc`  
    c) `ef`  
    d) Error  
    **Answer**: a) `cdef`  
    **Explanation**: Omitting the stop index continues the slice to the end of the string.

19. **How do you reverse a string using slicing?**  
    a) `s[::-1]`  
    b) `s[1:-1]`  
    c) `reversed(s)`  
    d) `s.reverse()`  
    **Answer**: a) `s[::-1]`  
    **Explanation**: The slice `[::-1]` reverses the string.

20. **What is the output of the following code?**  
    ```python
    s = "hello"
    print(s[::2])
    ```  
    a) `hello`  
    b) `hlo`  
    c) `hl`  
    d) `el`  
    **Answer**: b) `hlo`  
    **Explanation**: The step `2` skips every second character.

---

### **Strings - Basic Operations**  
21. **What is the result of `"Python" + "Rocks"`?**  
    a) `PythonRocks`  
    b) `Python Rocks`  
    c) `Python, Rocks`  
    d) Error  
    **Answer**: a) `PythonRocks`  
    **Explanation**: The `+` operator concatenates strings without adding spaces.

22. **What does `"Python" * 3` return?**  
    a) `PythonPythonPython`  
    b) `Python*3`  
    c) Error  
    d) `Python 3`  
    **Answer**: a) `PythonPythonPython`  
    **Explanation**: The `*` operator repeats the string the specified number of times.

23. **Which operator checks if a substring exists within a string?**  
    a) `in`  
    b) `has`  
    c) `exists`  
    d) `contains`  
    **Answer**: a) `in`  
    **Explanation**: The `in` operator checks membership within strings.

---

### **String Methods**  
24. **What does the `upper()` method do?**  
    a) Converts the string to lowercase  
    b) Converts the string to uppercase  
    c) Removes whitespace  
    d) None of the above  
    **Answer**: b) Converts the string to uppercase  
    **Explanation**: The `upper()` method converts all characters to uppercase.

25. **What is the output of the following code?**  
    ```python
    s = "Python"
    print(s.lower())
    ```  
    a) `python`  
    b) `PYTHON`  
    c) `Python`  
    d) Error  
    **Answer**: a) `python`  
    **Explanation**: The `lower()` method converts all characters to lowercase.

26. **Which method removes leading and trailing whitespace?**  
    a) `strip()`  
    b) `trim()`  
    c) `lstrip()`  
    d) `rstrip()`  
    **Answer**: a) `strip()`  
    **Explanation**: The `strip()` method removes both leading and trailing whitespace.

27. **What does the `find()` method return if the substring is not found?**  
    a) `-1`  
    b) `None`  
    c) `False`  
    d) Error  
    **Answer**: a) `-1`  
    **Explanation**: The `find()` method returns `-1` if the substring does not exist in the string.

28. **What does `replace("a", "b")` do?**  
    a) Replaces all instances of `b` with `a`  
    b) Replaces all instances of `a` with `b`  
    c) Removes `a` from the string  
    d) Throws an error  
    **Answer**: b) Replaces all instances of `a` with `b`  
    **Explanation**: The `replace()` method substitutes one substring for another.

---

### **Tuples - Basic Operations**  
29. **What is the output of the following code?**  
    ```python
    t = (1, 2, 3)
    print(len(t))
    ```  
    a) `2`  
    b) `3`  
    c) `4`  
    d) Error  
    **Answer**: b) `3`  
    **Explanation**: The `len()` function returns the number of elements in a tuple.

30. **What does the following code return?**  
    ```python
    t = (1, 2, 3)
    print(t + (4,))
    ```  
    a) `(1, 2, 3)`  
    b) `(1, 2, 3, 4)`  
    c) Error  
    d) `(4,)`  
    **Answer**: b) `(1, 2, 3, 4)`  
    **Explanation**: Tuples can be concatenated using the `+` operator.

---

### **Assigning Multiple Values at Once**  
31. **What does the following code return?**  
    ```python
    x, y = 5, 10
    print(x, y)
    ```  
    a) `10 5`  
    b) `5 10`  
    c) `Error`  
    d) None  
    **Answer**: b) `5 10`  
    **Explanation**: Multiple variables can be assigned values in a single statement.

---

### **Edge Cases and Applications**  
32. **What is the output of the following code?**  
    ```python
    s = "hello world"
    print(s[11])
    ```  
    a) `Error`  
    b) `d`  
    c) `hello`  
    d) None  
    **Answer**: a) `Error`  
    **Explanation**: Index 11 is out of range since the string's last index is 10.

33. **What happens if you attempt to modify a tuple?**  
    a) The change is allowed  
    b) The change is ignored  
    c) An error is raised  
    d) None of the above  
    **Answer**: c) An error is raised  
    **Explanation**: Tuples are immutable and cannot be changed.

34. **Which of the following will create an empty tuple?**  
    a) `t = ()`  
    b) `t = tuple()`  
    c) Both a and b  
    d) None of the above  
    **Answer**: c) Both a and b  
    **Explanation**: Both methods are valid for creating an empty tuple.

---

### **Continued MCQs for Session 2**

---

### **Tuples - Accessing Elements**

35. **What is the output of the following code?**  
    ```python
    t = (10, 20, 30, 40)
    print(t[1:3])
    ```  
    a) `(20, 30)`  
    b) `(10, 20)`  
    c) `(30, 40)`  
    d) `Error`  
    **Answer**: a) `(20, 30)`  
    **Explanation**: Slicing in tuples works the same as in strings, where `t[1:3]` includes elements from index 1 up to (but not including) index 3.

36. **What will happen if you execute the following code?**  
    ```python
    t = (1, 2, 3)
    t[1] = 5
    ```  
    a) `(1, 5, 3)`  
    b) `Error`  
    c) `(1, 2, 3)`  
    d) None  
    **Answer**: b) `Error`  
    **Explanation**: Tuples are immutable, so elements cannot be modified.

37. **Which of the following methods does not work with tuples?**  
    a) `index()`  
    b) `count()`  
    c) `append()`  
    d) None of the above  
    **Answer**: c) `append()`  
    **Explanation**: Tuples do not support methods that modify their contents, such as `append()` or `remove()`.

---

### **Assigning Multiple Values at Once**

38. **What is the result of the following code?**  
    ```python
    a, b, c = (1, 2, 3)
    print(a, b, c)
    ```  
    a) `1 2 3`  
    b) `(1, 2, 3)`  
    c) `Error`  
    d) None  
    **Answer**: a) `1 2 3`  
    **Explanation**: Tuple unpacking allows assigning multiple values to multiple variables at once.

39. **What is the result of swapping values using tuple unpacking?**  
    ```python
    x, y = 5, 10
    x, y = y, x
    print(x, y)
    ```  
    a) `5 10`  
    b) `10 5`  
    c) `Error`  
    d) None  
    **Answer**: b) `10 5`  
    **Explanation**: Tuple unpacking swaps values efficiently without needing a temporary variable.

---

### **Strings - Formatting**

40. **What does the `format()` method do in strings?**  
    a) Converts a string to uppercase  
    b) Inserts values into a string  
    c) Finds substrings  
    d) Removes spaces  
    **Answer**: b) Inserts values into a string  
    **Explanation**: The `format()` method replaces placeholders in a string with specified values.

41. **What is the output of the following code?**  
    ```python
    name = "John"
    print("Hello, {}!".format(name))
    ```  
    a) `Hello, John!`  
    b) `Hello, {}!`  
    c) `Error`  
    d) None  
    **Answer**: a) `Hello, John!`  
    **Explanation**: The `format()` method replaces `{}` with the value of `name`.

42. **Which of the following is a valid formatted string?**  
    a) `f"Value: {value}"`  
    b) `format(Value)`  
    c) `"Value: $value"`  
    d) None of the above  
    **Answer**: a) `f"Value: {value}"`  
    **Explanation**: f-strings are used for inline variable formatting in Python 3.6+.

---

### **Advanced Applications**

43. **What does the following code return?**  
    ```python
    s = "hello"
    t = tuple(s)
    print(t)
    ```  
    a) `('hello')`  
    b) `('h', 'e', 'l', 'l', 'o')`  
    c) `['h', 'e', 'l', 'l', 'o']`  
    d) Error  
    **Answer**: b) `('h', 'e', 'l', 'l', 'o')`  
    **Explanation**: Converting a string to a tuple breaks it into individual characters.

44. **What does the following code return?**  
    ```python
    s = "abcdef"
    print(s[::-2])
    ```  
    a) `fdb`  
    b) `fdc`  
    c) `Error`  
    d) `abc`  
    **Answer**: a) `fdb`  
    **Explanation**: The slice `[::-2]` reverses the string and skips every second character.

---

### **Miscellaneous**

45. **What does the following code do?**  
    ```python
    t = ("a", "b", "c")
    t += ("d",)
    print(t)
    ```  
    a) Adds `"d"` to the tuple  
    b) Creates a new tuple with `"d"` appended  
    c) Modifies the original tuple  
    d) Error  
    **Answer**: b) Creates a new tuple with `"d"` appended  
    **Explanation**: Tuples are immutable, so concatenation creates a new tuple.

46. **Which of the following is a valid way to create a tuple?**  
    a) `t = 1, 2, 3`  
    b) `t = (1, 2, 3)`  
    c) `t = tuple([1, 2, 3])`  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: Tuples can be created with or without parentheses or by using the `tuple()` constructor.

47. **Which of the following is NOT a characteristic of tuples?**  
    a) Ordered  
    b) Immutable  
    c) Supports indexing  
    d) Mutable  
    **Answer**: d) Mutable  
    **Explanation**: Tuples are immutable, meaning they cannot be changed after creation.

48. **What is the result of `len(())`?**  
    a) `0`  
    b) `1`  
    c) `Error`  
    d) None  
    **Answer**: a) `0`  
    **Explanation**: The length of an empty tuple is `0`.

49. **What does the following code return?**  
    ```python
    t = (1, 2, 3)
    print(4 in t)
    ```  
    a) `True`  
    b) `False`  
    c) Error  
    d) None  
    **Answer**: b) `False`  
    **Explanation**: The `in` operator checks for membership in the tuple.

50. **Which of the following is a valid tuple?**  
    a) `(1,)`  
    b) `tuple()`  
    c) `(1, 2, 3)`  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: Tuples can be empty, single-valued, or multi-valued.

---

Here are 50 MCQs for **Session 3** on Dictionaries in Python:

---

### **Introducing Dictionaries**

1. **What is the output of the following code?**  
    ```python
    my_dict = {"apple": 1, "banana": 2}
    print(my_dict)
    ```  
    a) `{'apple': 1, 'banana': 2}`  
    b) `['apple', 'banana']`  
    c) `(1, 2)`  
    d) `Error`  
    **Answer**: a) `{'apple': 1, 'banana': 2}`  
    **Explanation**: A dictionary in Python is printed with key-value pairs enclosed in curly braces.

2. **Which of the following is the correct way to define a dictionary?**  
    a) `my_dict = {1: 'apple', 2: 'banana'}`  
    b) `my_dict = ('apple', 1, 'banana', 2)`  
    c) `my_dict = [1, 2, 3]`  
    d) `my_dict = set(1, 2)`  
    **Answer**: a) `my_dict = {1: 'apple', 2: 'banana'}`  
    **Explanation**: Dictionaries are defined using curly braces with key-value pairs separated by a colon.

---

### **Defining Dictionaries**

3. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    print(my_dict["name"])
    ```  
    a) `name`  
    b) `John`  
    c) `30`  
    d) `Error`  
    **Answer**: b) `John`  
    **Explanation**: The dictionary key `"name"` maps to the value `"John"`.

4. **What will happen if you try to access a non-existent key?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    print(my_dict["address"])
    ```  
    a) `None`  
    b) `Error`  
    c) `{}`
    d) `John`  
    **Answer**: b) `Error`  
    **Explanation**: Trying to access a key that does not exist in the dictionary raises a `KeyError`.

5. **How do you define an empty dictionary in Python?**  
    a) `my_dict = {}`  
    b) `my_dict = []`  
    c) `my_dict = ()`  
    d) `my_dict = set()`  
    **Answer**: a) `my_dict = {}`  
    **Explanation**: An empty dictionary is created using empty curly braces `{}`.

---

### **Modifying Dictionaries**

6. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    my_dict["age"] = 35
    print(my_dict)
    ```  
    a) `{"name": "John", "age": 35}`  
    b) `{"name": "John", "age": 30}`  
    c) `{"name": "John", "age": "35"}`  
    d) `Error`  
    **Answer**: a) `{"name": "John", "age": 35}`  
    **Explanation**: The value associated with the key `"age"` is updated from `30` to `35`.

7. **Which of the following methods can be used to add a new key-value pair to an existing dictionary?**  
    a) `my_dict.add("key", "value")`  
    b) `my_dict["key"] = "value"`  
    c) `my_dict.insert("key", "value")`  
    d) `my_dict.append("key", "value")`  
    **Answer**: b) `my_dict["key"] = "value"`  
    **Explanation**: New key-value pairs can be added using the assignment syntax.

8. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    my_dict["age"] = 35
    my_dict["city"] = "New York"
    print(my_dict)
    ```  
    a) `{"name": "John", "age": 30, "city": "New York"}`  
    b) `{"name": "John", "age": 35, "city": "New York"}`  
    c) `{"name": "John", "city": "New York"}`  
    d) `Error`  
    **Answer**: b) `{"name": "John", "age": 35, "city": "New York"}`  
    **Explanation**: The `age` value is updated and a new key `"city"` is added to the dictionary.

9. **What will the following code print?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    my_dict["age"] = my_dict["age"] + 5
    print(my_dict)
    ```  
    a) `{"name": "John", "age": 35}`  
    b) `{"name": "John", "age": 30}`  
    c) `{"name": "John", "age": 5}`  
    d) `Error`  
    **Answer**: a) `{"name": "John", "age": 35}`  
    **Explanation**: The `"age"` value is updated by adding `5` to the previous value.

---

### **Deleting Items from Dictionaries**

10. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    del my_dict["age"]
    print(my_dict)
    ```  
    a) `{"name": "John", "age": 30}`  
    b) `{"name": "John"}`  
    c) `{}`
    d) `Error`  
    **Answer**: b) `{"name": "John"}`  
    **Explanation**: The `del` keyword removes the `"age"` key-value pair from the dictionary.

11. **Which method is used to remove all items from a dictionary?**  
    a) `my_dict.remove()`  
    b) `my_dict.clear()`  
    c) `my_dict.delete()`  
    d) `my_dict.pop()`  
    **Answer**: b) `my_dict.clear()`  
    **Explanation**: The `clear()` method removes all items from a dictionary.

12. **What is the result of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    removed_value = my_dict.pop("name")
    print(removed_value)
    print(my_dict)
    ```  
    a) `John {"age": 30}`  
    b) `John {}`  
    c) `{}`  
    d) `Error`  
    **Answer**: a) `John {"age": 30}`  
    **Explanation**: The `pop()` method removes and returns the value of the key `"name"`.

13. **What happens if you try to delete a non-existent key using `del`?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    del my_dict["address"]
    ```  
    a) `None`  
    b) `Error`  
    c) `KeyError`  
    d) `{}`  
    **Answer**: c) `KeyError`  
    **Explanation**: Trying to delete a non-existent key raises a `KeyError`.

14. **Which method removes the last inserted item from the dictionary?**  
    a) `my_dict.pop()`  
    b) `my_dict.popitem()`  
    c) `my_dict.remove()`  
    d) `my_dict.delete()`  
    **Answer**: b) `my_dict.popitem()`  
    **Explanation**: The `popitem()` method removes and returns the last inserted key-value pair from a dictionary.

---

### **Miscellaneous Dictionary Operations**

15. **What is the result of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30, "city": "New York"}
    print("age" in my_dict)
    ```  
    a) `True`  
    b) `False`  
    c) `Error`  
    d) `None`  
    **Answer**: a) `True`  
    **Explanation**: The `in` operator checks if the key `"age"` exists in the dictionary.

16. **Which of the following will return a list of all dictionary keys?**  
    a) `my_dict.values()`  
    b) `my_dict.items()`  
    c) `my_dict.keys()`  
    d) `my_dict.get()`  
    **Answer**: c) `my_dict.keys()`  
    **Explanation**: The `keys()` method returns a view object containing all keys in the dictionary.

17. **Which method can be used to return a copy of the dictionary?**  
    a) `my_dict.clone()`  
    b) `my_dict.copy()`  
    c) `my_dict.getcopy()`  
    d) `my_dict.duplicate()`  
    **Answer**: b) `my_dict.copy()`  
    **Explanation**: The `copy()` method returns a shallow copy of the dictionary.

---

Here are the remaining MCQs for **Session 3** on Dictionaries:

---

18. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30, "city": "New York"}
    print(my_dict.get("age"))
    ```  
    a) `30`  
    b) `None`  
    c) `Error`  
    d) `30, New York`  
    **Answer**: a) `30`  
    **Explanation**: The `get()` method returns the value for the given key if it exists.

19. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    print(my_dict.get("address", "Not Found"))
    ```  
    a) `Not Found`  
    b) `address`  
    c) `Error`  
    d) `None`  
    **Answer**: a) `Not Found`  
    **Explanation**: The `get()` method returns the default value if the key is not found.

20. **Which of the following methods can be used to check if a dictionary is empty?**  
    a) `my_dict.empty()`  
    b) `my_dict.is_empty()`  
    c) `len(my_dict) == 0`  
    d) `my_dict.size() == 0`  
    **Answer**: c) `len(my_dict) == 0`  
    **Explanation**: The `len()` function can be used to check if the dictionary has no elements.

21. **What does the `items()` method return in a dictionary?**  
    a) List of keys  
    b) List of values  
    c) List of key-value pairs  
    d) None of the above  
    **Answer**: c) List of key-value pairs  
    **Explanation**: The `items()` method returns a view object that displays a list of tuple pairs (key, value).

22. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    my_dict["age"] = my_dict.get("age") + 5
    print(my_dict)
    ```  
    a) `{"name": "John", "age": 35}`  
    b) `{"name": "John", "age": 30}`  
    c) `{"name": "John", "age": 40}`  
    d) `Error`  
    **Answer**: a) `{"name": "John", "age": 35}`  
    **Explanation**: The value associated with the key `"age"` is updated by adding `5`.

23. **What is the result of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    my_dict["address"] = "New York"
    print(len(my_dict))
    ```  
    a) `3`  
    b) `2`  
    c) `1`  
    d) `4`  
    **Answer**: a) `3`  
    **Explanation**: A new key-value pair is added, increasing the length of the dictionary to 3.

24. **What happens if you use `del` on a key that does not exist?**  
    ```python
    my_dict = {"name": "John"}
    del my_dict["age"]
    ```  
    a) It deletes the first key  
    b) It throws a `KeyError`  
    c) It returns `None`  
    d) The dictionary becomes empty  
    **Answer**: b) It throws a `KeyError`  
    **Explanation**: Deleting a non-existent key raises a `KeyError`.

25. **Which method removes a specific key and returns its value?**  
    a) `my_dict.pop()`  
    b) `my_dict.popitem()`  
    c) `my_dict.remove()`  
    d) `my_dict.clear()`  
    **Answer**: a) `my_dict.pop()`  
    **Explanation**: The `pop()` method removes the key-value pair and returns the value.

26. **What is the result of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30, "city": "New York"}
    print(list(my_dict.values()))
    ```  
    a) `["John", 30, "New York"]`  
    b) `["name", "age", "city"]`  
    c) `{"John", 30, "New York"}`  
    d) `None`  
    **Answer**: a) `["John", 30, "New York"]`  
    **Explanation**: The `values()` method returns a view object containing the dictionary's values.

27. **Which of the following operations can be used to merge two dictionaries?**  
    a) `dict1.merge(dict2)`  
    b) `dict1.update(dict2)`  
    c) `dict1.combine(dict2)`  
    d) `dict1.concat(dict2)`  
    **Answer**: b) `dict1.update(dict2)`  
    **Explanation**: The `update()` method merges the second dictionary into the first one.

28. **What is the output of the following code?**  
    ```python
    my_dict = {"a": 1, "b": 2, "c": 3}
    print(len(my_dict))
    ```  
    a) `3`  
    b) `2`  
    c) `1`  
    d) `Error`  
    **Answer**: a) `3`  
    **Explanation**: The `len()` function returns the number of key-value pairs in the dictionary.

29. **Which of the following methods can be used to iterate through all dictionary keys?**  
    a) `for key in my_dict:`  
    b) `for key in my_dict.keys():`  
    c) `for key in my_dict.items():`  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: You can iterate over dictionary keys using `my_dict` or `my_dict.keys()`.

30. **What is the result of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    my_dict["age"] = 40
    my_dict["city"] = "New York"
    print(my_dict)
    ```  
    a) `{"name": "John", "age": 30, "city": "New York"}`  
    b) `{"name": "John", "age": 40, "city": "New York"}`  
    c) `{"name": "John", "age": "40", "city": "New York"}`  
    d) `Error`  
    **Answer**: b) `{"name": "John", "age": 40, "city": "New York"}`  
    **Explanation**: The `"age"` key is updated and the `"city"` key is added.

31. **Which method can be used to check if a dictionary contains a certain key?**  
    a) `my_dict.has_key("key")`  
    b) `key in my_dict`  
    c) `my_dict.contains("key")`  
    d) `my_dict.check("key")`  
    **Answer**: b) `key in my_dict`  
    **Explanation**: The `in` operator checks if a key exists in a dictionary.

32. **What is the result of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    print(my_dict.get("city", "Not Found"))
    ```  
    a) `Not Found`  
    b) `city`  
    c) `Error`  
    d) `None`  
    **Answer**: a) `Not Found`  
    **Explanation**: The `get()` method returns the default value if the key is not found.

33. **Which method is used to remove a dictionary item based on the key?**  
    a) `my_dict.remove(key)`  
    b) `my_dict.delete(key)`  
    c) `my_dict.pop(key)`  
    d) `my_dict.clear(key)`  
    **Answer**: c) `my_dict.pop(key)`  
    **Explanation**: The `pop()` method removes and returns the value of the specified key.

34. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    my_dict["address"] = "New York"
    del my_dict["address"]
    print(my_dict)
    ```  
    a) `{"name": "John", "age": 30}`  
    b) `{"name": "John", "age": "New York"}`  
    c) `{"name": "John"}`  
    d) `Error`  
    **Answer**: a) `{"name": "John", "age": 30}`  
    **Explanation**: The `"address"` key-value pair is added and then deleted.

35. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    my_dict.update({"age": 35, "city": "New York"})
    print(my_dict)
    ```  
    a) `{"name": "John", "age": 35, "city": "New York"}`  
    b) `{"name": "John", "age": 30, "city": "New York"}`  
    c) `{"name": "John", "city": "New York"}`  
    d) `Error`  
    **Answer**: a) `{"name": "John", "age": 35, "city": "New York"}`  
    **Explanation**: The `update()` method merges the second dictionary and updates the value for `"age"`.

---
Here are the remaining MCQs for **Session 3** on Dictionaries:

---

36. **Which of the following is used to remove the last inserted key-value pair from a dictionary?**  
    a) `my_dict.remove()`  
    b) `my_dict.popitem()`  
    c) `my_dict.clear()`  
    d) `my_dict.del()`  
    **Answer**: b) `my_dict.popitem()`  
    **Explanation**: The `popitem()` method removes and returns the last inserted key-value pair from the dictionary.

37. **What is the output of the following code?**  
    ```python
    my_dict = {"name": "John", "age": 30}
    my_dict["city"] = "New York"
    print(my_dict)
    ```  
    a) `{"name": "John", "age": 30}`  
    b) `{"name": "John", "age": 30, "city": "New York"}`  
    c) `{"name": "John", "city": "New York"}`  
    d) `Error`  
    **Answer**: b) `{"name": "John", "age": 30, "city": "New York"}`  
    **Explanation**: A new key-value pair `"city": "New York"` is added to the dictionary.

38. **How can you check if a dictionary contains a particular value?**  
    a) `key in my_dict.values()`  
    b) `my_dict.value() == "value"`  
    c) `my_dict.contains("value")`  
    d) `value in my_dict.keys()`  
    **Answer**: a) `key in my_dict.values()`  
    **Explanation**: You can use the `in` operator to check if a value exists in the dictionary's values.

39. **What is the result of the following code?**  
    ```python
    my_dict = {"a": 1, "b": 2, "c": 3}
    my_dict.update({"b": 4, "d": 5})
    print(my_dict)
    ```  
    a) `{"a": 1, "b": 2, "c": 3, "d": 5}`  
    b) `{"a": 1, "b": 4, "c": 3, "d": 5}`  
    c) `{"a": 1, "b": 4, "c": 3}`  
    d) `Error`  
    **Answer**: b) `{"a": 1, "b": 4, "c": 3, "d": 5}`  
    **Explanation**: The `update()` method updates the value of `"b"` to `4` and adds a new key-value pair `"d": 5`.

40. **What does the `clear()` method do in a dictionary?**  
    a) Removes a single key-value pair  
    b) Removes all key-value pairs  
    c) Clears the dictionary without returning anything  
    d) Both a and b  
    **Answer**: b) Removes all key-value pairs  
    **Explanation**: The `clear()` method removes all items from the dictionary.

41. **What is the result of the following code?**  
    ```python
    my_dict = {"name": "Alice", "age": 25}
    my_dict["name"] = "Bob"
    del my_dict["age"]
    print(my_dict)
    ```  
    a) `{"name": "Bob"}`  
    b) `{"name": "Alice", "age": 25}`  
    c) `{"name": "Bob", "age": 25}`  
    d) `{"name": "Bob"}`  
    **Answer**: a) `{"name": "Bob"}`  
    **Explanation**: The value for `"name"` is updated to `"Bob"`, and the `"age"` key-value pair is deleted.

42. **What will happen if you try to access a dictionary with a key that does not exist, without using `get()` method?**  
    a) It returns `None`  
    b) It raises a `KeyError`  
    c) It returns the default value  
    d) It creates a new key-value pair  
    **Answer**: b) It raises a `KeyError`  
    **Explanation**: Directly accessing a non-existent key raises a `KeyError`.

43. **Which of the following is the correct way to create a dictionary?**  
    a) `my_dict = dict(name="John", age=30)`  
    b) `my_dict = {name: "John", age: 30}`  
    c) `my_dict = ("name": "John", "age": 30)`  
    d) `my_dict = [name="John", age=30]`  
    **Answer**: a) `my_dict = dict(name="John", age=30)`  
    **Explanation**: The correct syntax is using `dict()` constructor for creating a dictionary.

44. **What is the output of the following code?**  
    ```python
    my_dict = {"a": 1, "b": 2, "c": 3}
    del my_dict["b"]
    print(my_dict)
    ```  
    a) `{"a": 1, "b": 2, "c": 3}`  
    b) `{"a": 1, "c": 3}`  
    c) `{"b": 2}`  
    d) `Error`  
    **Answer**: b) `{"a": 1, "c": 3}`  
    **Explanation**: The key `"b"` is deleted, and the remaining dictionary is printed.

45. **Which of the following will add a new item to a dictionary?**  
    a) `my_dict.add("name", "Alice")`  
    b) `my_dict.insert("name", "Alice")`  
    c) `my_dict["name"] = "Alice"`  
    d) `my_dict.additem("name", "Alice")`  
    **Answer**: c) `my_dict["name"] = "Alice"`  
    **Explanation**: You can add a new key-value pair by using the assignment operator.

46. **What does the `fromkeys()` method do in a dictionary?**  
    a) Returns a new dictionary with the same keys but with `None` values  
    b) Returns the number of items in the dictionary  
    c) Returns a dictionary with keys initialized to the specified value  
    d) None of the above  
    **Answer**: c) Returns a dictionary with keys initialized to the specified value  
    **Explanation**: The `fromkeys()` method returns a new dictionary with keys from the provided iterable, with each key having the same value.

47. **What is the output of the following code?**  
    ```python
    my_dict = {"a": 1, "b": 2, "c": 3}
    my_dict["d"] = 4
    print(my_dict["d"])
    ```  
    a) `None`  
    b) `4`  
    c) `Error`  
    d) `{"d": 4}`  
    **Answer**: b) `4`  
    **Explanation**: The value `4` is assigned to the new key `"d"`, and it is printed.

48. **Which of the following will return the list of dictionary keys?**  
    a) `my_dict.keys()`  
    b) `my_dict.getkeys()`  
    c) `my_dict.items()`  
    d) `my_dict.listkeys()`  
    **Answer**: a) `my_dict.keys()`  
    **Explanation**: The `keys()` method returns a view object containing all the keys in the dictionary.

49. **What does the `pop()` method do in a dictionary?**  
    a) Removes all the key-value pairs  
    b) Removes a specific key-value pair and returns the value  
    c) Clears the dictionary  
    d) None of the above  
    **Answer**: b) Removes a specific key-value pair and returns the value  
    **Explanation**: The `pop()` method removes the key-value pair with the specified key and returns its value.

50. **What is the output of the following code?**  
    ```python
    my_dict = {"a": 1, "b": 2}
    print("a" in my_dict)
    ```  
    a) `True`  
    b) `False`  
    c) `Error`  
    d) `None`  
    **Answer**: a) `True`  
    **Explanation**: The `in` operator checks if the key `"a"` is present in the dictionary.

---
Here are 50 MCQs based on **Session 4** on working with lists in Python:

---

1. **Which of the following is the correct syntax to define a list in Python?**  
    a) `list = (1, 2, 3)`  
    b) `list = [1, 2, 3]`  
    c) `list = {1, 2, 3}`  
    d) `list = <1, 2, 3>`  
    **Answer**: b) `list = [1, 2, 3]`  
    **Explanation**: Lists are defined using square brackets `[]`.

2. **How do you retrieve the first element from a list `my_list = [10, 20, 30, 40]`?**  
    a) `my_list[0]`  
    b) `my_list[1]`  
    c) `my_list.first()`  
    d) `my_list[1]`  
    **Answer**: a) `my_list[0]`  
    **Explanation**: List indexing in Python starts at `0`, so the first element is accessed with index `0`.

3. **Which of the following methods adds an element to the end of a list?**  
    a) `append()`  
    b) `insert()`  
    c) `add()`  
    d) `extend()`  
    **Answer**: a) `append()`  
    **Explanation**: The `append()` method adds an element to the end of the list.

4. **What will be the output of the following code?**  
    ```python
    my_list = [10, 20, 30]
    my_list.append(40)
    print(my_list)
    ```  
    a) `[10, 20, 30]`  
    b) `[40, 10, 20, 30]`  
    c) `[10, 20, 30, 40]`  
    d) `Error`  
    **Answer**: c) `[10, 20, 30, 40]`  
    **Explanation**: The `append()` method adds the element `40` to the end of the list.

5. **How do you remove the element `20` from the list `my_list = [10, 20, 30, 40]`?**  
    a) `my_list.remove(20)`  
    b) `my_list.delete(20)`  
    c) `my_list.pop(20)`  
    d) `my_list.remove[20]`  
    **Answer**: a) `my_list.remove(20)`  
    **Explanation**: The `remove()` method removes the first occurrence of the specified value.

6. **What does the `pop()` method do in a list?**  
    a) Removes the first element of the list  
    b) Removes the last element of the list and returns it  
    c) Removes an element at a specific index  
    d) Both b and c  
    **Answer**: d) Both b and c  
    **Explanation**: The `pop()` method removes and returns the element at the specified index, or by default, the last element.

7. **How do you access the last element of the list `my_list = [10, 20, 30, 40]`?**  
    a) `my_list[-1]`  
    b) `my_list[4]`  
    c) `my_list[0]`  
    d) `my_list[last]`  
    **Answer**: a) `my_list[-1]`  
    **Explanation**: Negative indices in Python allow access from the end of the list, with `-1` being the last element.

8. **What will be the output of the following code?**  
    ```python
    my_list = [1, 2, 3, 4]
    my_list.insert(2, 10)
    print(my_list)
    ```  
    a) `[1, 2, 10, 3, 4]`  
    b) `[1, 2, 3, 4, 10]`  
    c) `[10, 1, 2, 3, 4]`  
    d) `[1, 2, 3, 10, 4]`  
    **Answer**: a) `[1, 2, 10, 3, 4]`  
    **Explanation**: The `insert()` method inserts an element at the specified index.

9. **Which method is used to join two lists in Python?**  
    a) `append()`  
    b) `join()`  
    c) `extend()`  
    d) `combine()`  
    **Answer**: c) `extend()`  
    **Explanation**: The `extend()` method adds all elements from one list to another.

10. **What will be the output of the following code?**  
    ```python
    my_list = [1, 2, 3]
    my_list.extend([4, 5])
    print(my_list)
    ```  
    a) `[1, 2, 3, 4, 5]`  
    b) `[1, 2, 3]`  
    c) `[4, 5, 1, 2, 3]`  
    d) `[1, 2, 3, [4, 5]]`  
    **Answer**: a) `[1, 2, 3, 4, 5]`  
    **Explanation**: The `extend()` method adds elements from another list to the end of the current list.

11. **How can you find the length of a list in Python?**  
    a) `len(list)`  
    b) `size(list)`  
    c) `count(list)`  
    d) `length(list)`  
    **Answer**: a) `len(list)`  
    **Explanation**: The `len()` function returns the number of elements in a list.

12. **Which of the following is the correct way to check if an element exists in a list?**  
    a) `element in list`  
    b) `element.exists(list)`  
    c) `list.contains(element)`  
    d) `element.check(list)`  
    **Answer**: a) `element in list`  
    **Explanation**: The `in` operator checks if an element exists in a list.

13. **What is the result of the following code?**  
    ```python
    my_list = [10, 20, 30, 40]
    print(my_list[1:3])
    ```  
    a) `[20, 30]`  
    b) `[10, 20]`  
    c) `[30, 40]`  
    d) `[20, 30, 40]`  
    **Answer**: a) `[20, 30]`  
    **Explanation**: The slice `my_list[1:3]` returns elements from index `1` to `2` (end index is exclusive).

14. **Which of the following will remove all elements from a list?**  
    a) `list.clear()`  
    b) `list.remove_all()`  
    c) `list.delete()`  
    d) `list.empty()`  
    **Answer**: a) `list.clear()`  
    **Explanation**: The `clear()` method removes all elements from the list.

15. **What will be the output of the following code?**  
    ```python
    my_list = [10, 20, 30, 40]
    print(my_list.pop())
    ```  
    a) `40`  
    b) `None`  
    c) `[40]`  
    d) `10`  
    **Answer**: a) `40`  
    **Explanation**: The `pop()` method removes and returns the last element of the list.

16. **Which method is used to count the occurrences of an element in a list?**  
    a) `count()`  
    b) `frequency()`  
    c) `find()`  
    d) `get()`  
    **Answer**: a) `count()`  
    **Explanation**: The `count()` method returns the number of times an element appears in the list.

17. **What does the `del` statement do in a list?**  
    a) Deletes the list entirely  
    b) Deletes an element at a specific index  
    c) Deletes the last element  
    d) Deletes the first element  
    **Answer**: b) Deletes an element at a specific index  
    **Explanation**: The `del` statement can remove an element at a specific index in the list.

18. **What will be the output of the following code?**  
    ```python
    my_list = [1, 2, 3, 4]
    my_list[1:3] = [5, 6]
    print(my_list)
    ```  
    a) `[1, 5, 6, 4]`  
    b) `[1, 5, 6, 3, 4]`  
    c) `[5, 6, 3, 4]`  
    d) `[1, 2, 3, 4, 5, 6]`  
    **Answer**: a) `[1, 5, 6, 4]`  
    **Explanation**: The slice assignment replaces elements at indices `1` and `2` with the values `[5, 6]`.

19. **How do you concatenate two lists `list1 = [1, 2]` and `list2 = [3, 4]`?**  
    a) `list1 + list2`  
    b) `list1.append(list2)`  
    c) `list1.extend(list2)`  
    d) Both a and c  
    **Answer**: d) Both a and c  
    **Explanation**: Both `+` operator and `extend()` method concatenate two lists.

20. **What does the `index()` method do in a list?**  
    a) Returns the first occurrence of an element  
    b) Removes an element at a specific index  
    c) Returns the index of the last occurrence of an element  
    d) Sorts the list  
    **Answer**: a) Returns the first occurrence of an element  
    **Explanation**: The `index()` method returns the index of the first occurrence of the specified element.

---
Here are the remaining questions, continuing from 21 to 50:

---

21. **What will be the output of the following code?**  
    ```python
    my_list = [1, 2, 3]
    my_list += [4, 5]
    print(my_list)
    ```  
    a) `[1, 2, 3, 4, 5]`  
    b) `[4, 5, 1, 2, 3]`  
    c) `[1, 2, 3]`  
    d) `[1, 2, 3, [4, 5]]`  
    **Answer**: a) `[1, 2, 3, 4, 5]`  
    **Explanation**: The `+=` operator adds elements from the second list to the first list.

22. **Which of the following methods is used to reverse the elements of a list?**  
    a) `reverse()`  
    b) `invert()`  
    c) `flip()`  
    d) `backward()`  
    **Answer**: a) `reverse()`  
    **Explanation**: The `reverse()` method reverses the elements of a list in place.

23. **What is the output of the following code?**  
    ```python
    my_list = [1, 2, 3]
    my_list[1] = 10
    print(my_list)
    ```  
    a) `[1, 2, 3]`  
    b) `[1, 10, 3]`  
    c) `[10, 2, 3]`  
    d) `[10, 20, 30]`  
    **Answer**: b) `[1, 10, 3]`  
    **Explanation**: The element at index `1` is modified to `10`.

24. **What does the `list()` function do?**  
    a) Converts a tuple to a list  
    b) Converts a string to a list  
    c) Creates a new list  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: The `list()` function can convert different iterable objects like strings, tuples, etc., to lists.

25. **Which method would you use to find the index of the element `5` in the list `my_list = [1, 2, 3, 4, 5]`?**  
    a) `find(5)`  
    b) `search(5)`  
    c) `my_list.index(5)`  
    d) `my_list.index(5, 0, 3)`  
    **Answer**: c) `my_list.index(5)`  
    **Explanation**: The `index()` method returns the index of the first occurrence of the specified value.

26. **Which of the following is true about the `extend()` method in lists?**  
    a) It adds a single element to the list  
    b) It appends multiple elements to the list  
    c) It clears the list  
    d) It removes the first element  
    **Answer**: b) It appends multiple elements to the list  
    **Explanation**: The `extend()` method adds all elements of an iterable to the list.

27. **What is the result of the following code?**  
    ```python
    my_list = [10, 20, 30]
    my_list = my_list * 2
    print(my_list)
    ```  
    a) `[10, 20, 30, 10, 20, 30]`  
    b) `[20, 30, 10, 20, 30]`  
    c) `[10, 20, 30, 2, 4, 6]`  
    d) `[20, 30]`  
    **Answer**: a) `[10, 20, 30, 10, 20, 30]`  
    **Explanation**: The `*` operator duplicates the list.

28. **How do you combine two lists `list1 = [1, 2]` and `list2 = [3, 4]` without changing the original lists?**  
    a) `list1 + list2`  
    b) `list1.extend(list2)`  
    c) `list1.append(list2)`  
    d) `list1 += list2`  
    **Answer**: a) `list1 + list2`  
    **Explanation**: The `+` operator concatenates the lists without modifying the originals.

29. **Which operator would you use to repeat a list multiple times in Python?**  
    a) `*`  
    b) `+`  
    c) `*=`  
    d) `&`  
    **Answer**: a) `*`  
    **Explanation**: The `*` operator repeats the list a specified number of times.

30. **Which method is used to remove the last item from a list and return it?**  
    a) `remove()`  
    b) `pop()`  
    c) `delete()`  
    d) `clear()`  
    **Answer**: b) `pop()`  
    **Explanation**: The `pop()` method removes and returns the last item from the list.

31. **What is the result of the following code?**  
    ```python
    my_list = [1, 2, 3]
    my_list[1:3] = [4, 5]
    print(my_list)
    ```  
    a) `[1, 4, 5, 3]`  
    b) `[1, 4, 5]`  
    c) `[1, 2, 3, 4, 5]`  
    d) `[4, 5]`  
    **Answer**: b) `[1, 4, 5]`  
    **Explanation**: The slice assignment replaces elements at indices `1` and `2` with `[4, 5]`.

32. **Which of the following will raise an `IndexError`?**  
    a) `my_list[5]` when `my_list = [1, 2, 3]`  
    b) `my_list[-4]` when `my_list = [1, 2, 3]`  
    c) `my_list[2]` when `my_list = [1, 2]`  
    d) `my_list[0]` when `my_list = [1, 2, 3]`  
    **Answer**: a) `my_list[5]` when `my_list = [1, 2, 3]`  
    **Explanation**: Accessing an index that does not exist in the list will raise an `IndexError`.

33. **Which method is used to sort the elements of a list in Python?**  
    a) `sort()`  
    b) `order()`  
    c) `sorted()`  
    d) Both a and c  
    **Answer**: d) Both a and c  
    **Explanation**: The `sort()` method sorts the list in place, while `sorted()` returns a sorted copy.

34. **What is the output of the following code?**  
    ```python
    my_list = [3, 1, 2]
    my_list.sort()
    print(my_list)
    ```  
    a) `[1, 2, 3]`  
    b) `[3, 2, 1]`  
    c) `[2, 1, 3]`  
    d) `[1, 3, 2]`  
    **Answer**: a) `[1, 2, 3]`  
    **Explanation**: The `sort()` method arranges the elements in ascending order.

35. **Which function can you use to create a shallow copy of a list?**  
    a) `copy()`  
    b) `duplicate()`  
    c) `clone()`  
    d) `list.copy()`  
    **Answer**: d) `list.copy()`  
    **Explanation**: The `copy()` method creates a shallow copy of the list.

36. **What will be the result of the following code?**  
    ```python
    my_list = [1, 2, 3, 4]
    my_list[1:2] = [5, 6, 7]
    print(my_list)
    ```  
    a) `[1, 5, 6, 7, 3, 4]`  
    b) `[1, 5, 6, 7, 2, 3, 4]`  
    c) `[1, 5, 6, 7, 4]`  
    d) `[5, 6, 7, 1, 2, 3, 4]`  
    **Answer**: a) `[1, 5, 6, 7, 3, 4]`  
    **Explanation**: The slice `my_list[1:2]` is replaced by `[5, 6, 7]`.

37. **Which of the following will check whether an item exists in a list?**  
    a) `if item in list:`  
    b) `if list.contains(item):`  
    c) `if item.exists(list):`  
    d) `if item.check(list):`  
    **Answer**: a) `if item in list:`  
    **Explanation**: The `in` operator checks if an item exists in a list.

38. **Which of the following is true about Python lists?**  
    a) Lists are immutable  
    b) Lists can contain elements of different types  
    c) Lists can only contain strings  
    d) Lists do not support negative indexing  
    **Answer**: b) Lists can contain elements of different types  
    **Explanation**: Lists in Python are flexible and can hold elements of different types.

39. **What will be the output of the following code?**  
    ```python
    my_list = [1, 2, 3]
    my_list[0] = my_list[0] + 1
    print(my_list)
    ```  
    a) `[2, 2, 3]`  
    b) `[1, 2, 3]`  
    c) `[2, 3, 4]`  
    d) `[1, 2, 3, 4]`  
    **Answer**: a) `[2, 2, 3]`  
    **Explanation**: The first element of the list is incremented by `1`.

40. **Which of the following methods is used to count the occurrences of an item in a list?**  
    a) `count()`  
    b) `search()`  
    c) `frequency()`  
    d) `find()`  
    **Answer**: a) `count()`  
    **Explanation**: The `count()` method counts the number of occurrences of a specified item in a list.

41. **What is the result of the following code?**  
    ```python
    my_list = [1, 2, 3]
    my_list.append([4, 5])
    print(my_list)
    ```  
    a) `[1, 2, 3, 4, 5]`  
    b) `[1, 2, 3, [4, 5]]`  
    c) `[

4, 5, 1, 2, 3]`  
    d) `[1, 2, 3]`  
    **Answer**: b) `[1, 2, 3, [4, 5]]`  
    **Explanation**: The `append()` method adds the list `[4, 5]` as a single element to the list.

42. **Which method is used to insert an item at a specific index in a list?**  
    a) `add()`  
    b) `insert()`  
    c) `insertAt()`  
    d) `place()`  
    **Answer**: b) `insert()`  
    **Explanation**: The `insert()` method adds an item at the specified index.

43. **What does the `clear()` method do?**  
    a) Removes a specific element from the list  
    b) Removes all elements from the list  
    c) Deletes a list  
    d) Reverses the elements of the list  
    **Answer**: b) Removes all elements from the list  
    **Explanation**: The `clear()` method removes all elements from the list, leaving it empty.

44. **What will be the result of the following code?**  
    ```python
    my_list = [2, 4, 6]
    my_list += [8, 10]
    print(my_list)
    ```  
    a) `[2, 4, 6, 8, 10]`  
    b) `[8, 10, 2, 4, 6]`  
    c) `[2, 4, 6, [8, 10]]`  
    d) `[2, 4, 6, 8]`  
    **Answer**: a) `[2, 4, 6, 8, 10]`  
    **Explanation**: The `+=` operator adds elements from the second list to the first.

45. **Which of the following is true for lists in Python?**  
    a) Lists are ordered  
    b) Lists are mutable  
    c) Lists can hold elements of different data types  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: Lists in Python are ordered, mutable, and can contain elements of different data types.

46. **What is the output of the following code?**  
    ```python
    my_list = [1, 2, 3, 4]
    my_list.remove(3)
    print(my_list)
    ```  
    a) `[1, 2, 4]`  
    b) `[2, 3, 4]`  
    c) `[1, 3, 4]`  
    d) `[1, 2, 3]`  
    **Answer**: a) `[1, 2, 4]`  
    **Explanation**: The `remove()` method removes the first occurrence of the specified value.

47. **Which method will remove all elements from a list, but keep the list itself intact?**  
    a) `clear()`  
    b) `remove()`  
    c) `del`  
    d) `pop()`  
    **Answer**: a) `clear()`  
    **Explanation**: The `clear()` method removes all elements from the list but does not delete the list itself.

48. **Which of the following is the correct way to access the last element of a list `my_list = [1, 2, 3]`?**  
    a) `my_list[-1]`  
    b) `my_list[0]`  
    c) `my_list[len(my_list)]`  
    d) `my_list[3]`  
    **Answer**: a) `my_list[-1]`  
    **Explanation**: Negative indexing allows access to elements starting from the end of the list.

49. **What is the output of the following code?**  
    ```python
    my_list = [10, 20, 30]
    print(my_list[::-1])
    ```  
    a) `[30, 20, 10]`  
    b) `[10, 20, 30]`  
    c) `[20, 10]`  
    d) `None`  
    **Answer**: a) `[30, 20, 10]`  
    **Explanation**: The slice `[::-1]` reverses the list.

50. **Which of the following functions is used to find the maximum value in a list?**  
    a) `max()`  
    b) `maximum()`  
    c) `highest()`  
    d) `findmax()`  
    **Answer**: a) `max()`  
    **Explanation**: The `max()` function returns the largest value in the list.

---
Here are the MCQs based on the syllabus for **Session 5 & 6**:

---

### **Function and Methods in Python**

1. **Which of the following is the correct way to define a function in Python?**  
    a) `function myFunction()`  
    b) `def myFunction:`  
    c) `def myFunction()`  
    d) `function myFunction:`  
    **Answer**: c) `def myFunction()`  
    **Explanation**: Functions in Python are defined using the `def` keyword.

2. **How do you call a function named `greet` in Python?**  
    a) `call greet()`  
    b) `greet()`  
    c) `call greet;`  
    d) `greet[]`  
    **Answer**: b) `greet()`  
    **Explanation**: Functions are called by simply using their name followed by parentheses.

3. **What will be the output of the following code?**  
    ```python
    def add(a, b):
        return a + b
    print(add(5, 3))
    ```  
    a) `53`  
    b) `8`  
    c) `Error`  
    d) `None`  
    **Answer**: b) `8`  
    **Explanation**: The function `add` correctly adds `5` and `3` to return `8`.

4. **Which of the following is a type of function in Python?**  
    a) Recursive function  
    b) Anonymous function  
    c) Built-in function  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: Python supports recursive functions, anonymous functions (lambdas), and built-in functions.

5. **How would you pass arguments to a function?**  
    a) Directly in the function body  
    b) Through function parameters  
    c) Using global variables  
    d) Using print() statements  
    **Answer**: b) Through function parameters  
    **Explanation**: Arguments are passed by providing values to the parameters when calling the function.

6. **Which of the following is an example of an anonymous function in Python?**  
    a) `def greet():`  
    b) `lambda x: x + 1`  
    c) `function add(a, b):`  
    d) `return lambda x: x + 1`  
    **Answer**: b) `lambda x: x + 1`  
    **Explanation**: A `lambda` function is a one-liner anonymous function.

7. **What is the scope of a variable defined inside a function?**  
    a) Global  
    b) Local  
    c) Both global and local  
    d) None  
    **Answer**: b) Local  
    **Explanation**: Variables inside a function are local to that function.

8. **Which keyword is used to declare a variable as global inside a function?**  
    a) `global`  
    b) `public`  
    c) `local`  
    d) `extern`  
    **Answer**: a) `global`  
    **Explanation**: The `global` keyword allows modification of global variables inside functions.

9. **What will be the output of the following code?**  
    ```python
    x = 5
    def foo():
        global x
        x = 10
    foo()
    print(x)
    ```  
    a) `5`  
    b) `10`  
    c) `None`  
    d) `Error`  
    **Answer**: b) `10`  
    **Explanation**: The `global` keyword modifies the global variable `x`.

10. **What is the correct way to define optional parameters in a Python function?**  
    a) `def function(arg = 0)`  
    b) `def function[arg = 0]`  
    c) `def function(arg or 0)`  
    d) `function(arg = 0)`  
    **Answer**: a) `def function(arg = 0)`  
    **Explanation**: Optional arguments are defined by providing a default value.

11. **Which of the following is a valid way to call a function with named arguments?**  
    a) `function(arg1 = 2, arg2 = 3)`  
    b) `function(2, 3)`  
    c) `function(arg1: 2, arg2: 3)`  
    d) `function([2, 3])`  
    **Answer**: a) `function(arg1 = 2, arg2 = 3)`  
    **Explanation**: Named arguments are passed by specifying the parameter names.

12. **What is the output of the following code?**  
    ```python
    def print_info(name, age=25):
        print(f"Name: {name}, Age: {age}")
    print_info("Alice")
    ```  
    a) `Name: Alice, Age: 25`  
    b) `Name: Alice, Age: 0`  
    c) `Name: Alice`  
    d) `Error`  
    **Answer**: a) `Name: Alice, Age: 25`  
    **Explanation**: The default value of `age` is used since it’s not provided.

13. **Which built-in function is used to get the type of a variable in Python?**  
    a) `type()`  
    b) `str()`  
    c) `dir()`  
    d) `typeof()`  
    **Answer**: a) `type()`  
    **Explanation**: The `type()` function returns the type of an object.

14. **What does the `str()` function do?**  
    a) Converts an object to a string  
    b) Returns the string length  
    c) Converts a string to a number  
    d) Checks if the object is a string  
    **Answer**: a) Converts an object to a string  
    **Explanation**: The `str()` function converts any object to a string.

15. **What does the `dir()` function return?**  
    a) A list of all attributes of an object  
    b) The directory path of a file  
    c) The type of the object  
    d) The string representation of an object  
    **Answer**: a) A list of all attributes of an object  
    **Explanation**: The `dir()` function returns a list of valid attributes of an object.

---
Here are the remaining MCQs for **Session 5 & 6** (till 50):

---

16. **Which of the following is the correct way to define a function that accepts any number of keyword arguments?**  
    a) `def func(*args)`  
    b) `def func(**args)`  
    c) `def func(arg1, *args)`  
    d) `def func(arg1, **args)`  
    **Answer**: b) `def func(**args)`  
    **Explanation**: `**args` allows the function to accept an arbitrary number of keyword arguments.

17. **What is the result of calling the following function?**  
    ```python
    def multiply(a, b=2):
        return a * b
    print(multiply(3))
    ```  
    a) `6`  
    b) `3`  
    c) `Error`  
    d) `5`  
    **Answer**: a) `6`  
    **Explanation**: Since `b` is optional with a default value of `2`, `multiply(3)` results in `3 * 2 = 6`.

18. **Which function is used to get the length of a string in Python?**  
    a) `len()`  
    b) `size()`  
    c) `length()`  
    d) `str_length()`  
    **Answer**: a) `len()`  
    **Explanation**: The `len()` function returns the length of an object, including strings.

19. **What will be the output of the following code?**  
    ```python
    def sum_nums(a, b=10, c=5):
        return a + b + c
    print(sum_nums(3))
    ```  
    a) `18`  
    b) `8`  
    c) `10`  
    d) `None`  
    **Answer**: a) `18`  
    **Explanation**: The function uses the default values of `b` and `c`, and adds them to `a`.

20. **What type of argument is provided when a function is called with a value explicitly assigned to a parameter?**  
    a) Positional argument  
    b) Keyword argument  
    c) Default argument  
    d) Variable-length argument  
    **Answer**: b) Keyword argument  
    **Explanation**: A keyword argument is specified by explicitly assigning a value to a named parameter.

21. **Which of the following is correct to pass a variable number of positional arguments to a function?**  
    a) `def func(*args)`  
    b) `def func(**args)`  
    c) `def func(arg1, arg2, *args)`  
    d) `def func(arg1, *args)`  
    **Answer**: a) `def func(*args)`  
    **Explanation**: `*args` allows passing any number of positional arguments.

22. **What is the output of the following code?**  
    ```python
    def func(a, b=5, c=10):
        return a + b + c
    print(func(2, c=3))
    ```  
    a) `10`  
    b) `8`  
    c) `5`  
    d) `Error`  
    **Answer**: b) `8`  
    **Explanation**: `a` is `2`, `b` uses the default value `5`, and `c` is explicitly set to `3`.

23. **Which of the following is a valid way to create a function that returns no value?**  
    a) `def func(): return`  
    b) `def func() return None`  
    c) `def func():`  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: A function can return `None` implicitly or explicitly.

24. **What will be the output of the following code?**  
    ```python
    def func(x):
        return lambda y: x + y
    result = func(2)
    print(result(3))
    ```  
    a) `5`  
    b) `23`  
    c) `None`  
    d) `2`  
    **Answer**: a) `5`  
    **Explanation**: The `lambda` function returns `x + y`, so `2 + 3 = 5`.

25. **Which of the following is a function that has no parameters?**  
    a) `def func() {}`  
    b) `def func(a, b):`  
    c) `def func(arg=0):`  
    d) `def func(*args):`  
    **Answer**: a) `def func() {}`  
    **Explanation**: This function takes no parameters.

26. **What does the `return` statement do in a Python function?**  
    a) It terminates the function execution  
    b) It defines the function parameters  
    c) It provides the output of the function  
    d) It creates a function  
    **Answer**: c) It provides the output of the function  
    **Explanation**: The `return` statement sends the function's output back to the caller.

27. **Which of the following functions is used to convert a string to lowercase in Python?**  
    a) `lower()`  
    b) `convert()`  
    c) `str.lower()`  
    d) `string.lower()`  
    **Answer**: a) `lower()`  
    **Explanation**: The `lower()` function converts all characters in a string to lowercase.

28. **What will the following code output?**  
    ```python
    def greet(name):
        print("Hello " + name)
    greet("Alice")
    ```  
    a) `Hello Alice`  
    b) `Hello`  
    c) `Alice`  
    d) `Error`  
    **Answer**: a) `Hello Alice`  
    **Explanation**: The function prints the string `"Hello Alice"`.

29. **Which of the following built-in functions can be used to display the documentation of a function or module in Python?**  
    a) `help()`  
    b) `doc()`  
    c) `dir()`  
    d) `print()`  
    **Answer**: a) `help()`  
    **Explanation**: The `help()` function is used to display documentation for a function or module.

30. **Which of the following is true about a recursive function?**  
    a) It does not call itself  
    b) It calls itself with smaller input to solve a problem  
    c) It always results in an infinite loop  
    d) It requires a loop to operate  
    **Answer**: b) It calls itself with smaller input to solve a problem  
    **Explanation**: Recursive functions solve problems by calling themselves with smaller versions of the problem.

31. **What is the output of the following code?**  
    ```python
    def count_down(n):
        if n <= 0:
            print("Done!")
        else:
            print(n)
            count_down(n - 1)
    count_down(3)
    ```  
    a) `3 2 1 Done!`  
    b) `Done! 3 2 1`  
    c) `3 2 1`  
    d) `Done!`  
    **Answer**: a) `3 2 1 Done!`  
    **Explanation**: The function recursively calls itself, printing the values from 3 to 1, then prints `"Done!"`.

32. **What does the `type()` function do?**  
    a) Returns the data type of the variable  
    b) Converts a variable to a specific type  
    c) Returns the type of the function  
    d) None of the above  
    **Answer**: a) Returns the data type of the variable  
    **Explanation**: The `type()` function returns the type of the given object or variable.

33. **What is the purpose of the `dir()` function?**  
    a) Lists all functions in a module  
    b) Lists the properties and methods of an object  
    c) Lists the current directory  
    d) All of the above  
    **Answer**: b) Lists the properties and methods of an object  
    **Explanation**: The `dir()` function returns the list of attributes and methods of an object.

34. **Which function can be used to check if a string contains only alphabetic characters?**  
    a) `isalnum()`  
    b) `isalpha()`  
    c) `isnumeric()`  
    d) `istitle()`  
    **Answer**: b) `isalpha()`  
    **Explanation**: The `isalpha()` function checks if all characters in a string are alphabetic.

35. **Which of the following is an example of a method call in Python?**  
    a) `print("Hello")`  
    b) `"Hello".lower()`  
    c) `len("Hello")`  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: All of the options are valid examples of method calls in Python.

36. **Which of the following is the correct way to pass multiple arguments to a function?**  
    a) `def function(*args, **kwargs)`  
    b) `def function(arg1, *args)`  
    c) `def function(arg1, **kwargs)`  
    d) All of the above  
    **Answer**: d) All of the above  
    **Explanation**: These are all valid ways to pass multiple arguments in Python.

37. **Which of the following is the correct syntax to call a function with named arguments?**  
    a) `function(arg1, arg2)`  
    b) `function(arg1=1, arg2=2)`  
    c) `function(arg1, arg2=2)`  
    d) `function(arg1=1, 2)`  
    **Answer**: b) `function(arg1=1, arg2=2)`  
    **Explanation**: Named arguments are specified by assigning values to the parameters.

38. **What will the following code output?**  
    ```python
    def greet(name):


        return "Hello " + name
    print(greet("Alice"))
    ```  
    a) `Hello Alice`  
    b) `Hello`  
    c) `Alice`  
    d) `None`  
    **Answer**: a) `Hello Alice`  
    **Explanation**: The function returns the string `"Hello Alice"`.

39. **What is a lambda function?**  
    a) A named function  
    b) An anonymous function defined with the `lambda` keyword  
    c) A function that always returns a value  
    d) A function that can only take one argument  
    **Answer**: b) An anonymous function defined with the `lambda` keyword  
    **Explanation**: A lambda function is an anonymous function defined using the `lambda` keyword.

40. **What will the following code output?**  
    ```python
    def square(x):
        return x * x
    print(square(4))
    ```  
    a) `16`  
    b) `4`  
    c) `8`  
    d) `None`  
    **Answer**: a) `16`  
    **Explanation**: The `square` function squares the input value `4`, resulting in `16`.

41. **Which of the following is the correct way to declare a global variable inside a function?**  
    a) `global x`  
    b) `extern x`  
    c) `static x`  
    d) `global variable`  
    **Answer**: a) `global x`  
    **Explanation**: The `global` keyword allows you to modify a global variable inside a function.

42. **What is the output of the following code?**  
    ```python
    def greet(name="World"):
        print("Hello " + name)
    greet()
    ```  
    a) `Hello World`  
    b) `Hello`  
    c) `Hello None`  
    d) `Error`  
    **Answer**: a) `Hello World`  
    **Explanation**: Since no argument is passed, the default value `"World"` is used.

43. **Which of the following is a valid way to pass a function as an argument in Python?**  
    a) `function(parameter)`  
    b) `function(parameter, func)`  
    c) `function(func=parameter)`  
    d) All of the above  
    **Answer**: b) `function(parameter, func)`  
    **Explanation**: Functions can be passed as arguments in Python.

44. **What is the output of the following code?**  
    ```python
    def square(n):
        return n * n
    print(square(5))
    ```  
    a) `25`  
    b) `10`  
    c) `5`  
    d) `None`  
    **Answer**: a) `25`  
    **Explanation**: The function returns the square of `5`, which is `25`.

45. **What is the default value of `args` in a function definition?**  
    a) `None`  
    b) `0`  
    c) `[]`  
    d) `()`  
    **Answer**: d) `()`  
    **Explanation**: `args` default is an empty tuple `()` in Python.

46. **Which function is used to define a generator function in Python?**  
    a) `yield`  
    b) `return`  
    c) `generate()`  
    d) `next()`  
    **Answer**: a) `yield`  
    **Explanation**: The `yield` keyword is used to define a generator function in Python.

47. **Which of the following is correct for defining a recursive function?**  
    a) It must have a base case  
    b) It never returns  
    c) It cannot call itself  
    d) None of the above  
    **Answer**: a) It must have a base case  
    **Explanation**: A recursive function must have a base case to stop the recursion.

48. **What will be the output of this code?**  
    ```python
    def multiply(x, y=5):
        return x * y
    print(multiply(3))
    ```  
    a) `15`  
    b) `8`  
    c) `None`  
    d) `3`  
    **Answer**: a) `15`  
    **Explanation**: The function multiplies `3` by the default value `5`.

49. **Which of the following is a valid function signature in Python?**  
    a) `def function(x, y=5):`  
    b) `def function(x=5, y):`  
    c) `def function(x, y=5, z):`  
    d) None of the above  
    **Answer**: a) `def function(x, y=5):`  
    **Explanation**: The default value should be provided only for the trailing parameters.

50. **What is the output of the following code?**  
    ```python
    def add(a, b=3):
        return a + b
    print(add(2))
    ```  
    a) `5`  
    b) `2`  
    c) `3`  
    d) `None`  
    **Answer**: a) `5`  
    **Explanation**: The function returns `2 + 3 = 5`.

---

Here are 50 multiple-choice questions (MCQs) based on Session 7 & 8: "Working with Tuples," "Introducing Tuples," "Accessing Tuples," and "Operations on Tuples":

### 1. **What is a tuple in Python?**
   a) A mutable collection  
   b) An immutable collection  
   c) A type of dictionary  
   d) A type of set  
   **Answer**: b) An immutable collection

### 2. **Which of the following is a valid tuple in Python?**
   a) `(1, 2, 3)`  
   b) `{1, 2, 3}`  
   c) `[1, 2, 3]`  
   d) `1, 2, 3`  
   **Answer**: a) `(1, 2, 3)`

### 3. **Which of the following can be used to create an empty tuple?**
   a) `()`  
   b) `[]`  
   c) `{}`  
   d) `None`  
   **Answer**: a) `()`

### 4. **How do you create a tuple with one element?**
   a) `(1)`  
   b) `[1]`  
   c) `(1,)`  
   d) `1,`  
   **Answer**: c) `(1,)`

### 5. **Which operator is used to concatenate two tuples?**
   a) `+`  
   b) `*`  
   c) `-`  
   d) `/`  
   **Answer**: a) `+`

### 6. **Which of the following operations is not supported by tuples?**
   a) Indexing  
   b) Slicing  
   c) Appending  
   d) Concatenation  
   **Answer**: c) Appending

### 7. **How do you access the first element of the tuple `t = (1, 2, 3)`?**
   a) `t[1]`  
   b) `t[0]`  
   c) `t[-1]`  
   d) `t(1)`  
   **Answer**: b) `t[0]`

### 8. **What will be the output of the following code?**  
   ```python
   t = (1, 2, 3)
   print(t[1])
   ```  
   a) `1`  
   b) `2`  
   c) `3`  
   d) `None`  
   **Answer**: b) `2`

### 9. **Which method can be used to find the length of a tuple?**
   a) `length()`  
   b) `len()`  
   c) `size()`  
   d) `count()`  
   **Answer**: b) `len()`

### 10. **Which of the following will cause an error in Python?**
   a) `t[1] = 2`  
   b) `t[1]`  
   c) `t = (1, 2, 3)`  
   d) `t + (4, 5)`  
   **Answer**: a) `t[1] = 2`

### 11. **How do you create a tuple with mixed data types?**
   a) `(1, "a", 3.14)`  
   b) `[1, "a", 3.14]`  
   c) `{1, "a", 3.14}`  
   d) `1, "a", 3.14`  
   **Answer**: a) `(1, "a", 3.14)`

### 12. **What will be the output of the following code?**  
   ```python
   t = (1, 2, 3)
   print(t[2])
   ```  
   a) `3`  
   b) `2`  
   c) `1`  
   d) `None`  
   **Answer**: a) `3`

### 13. **Which of the following is true about tuple concatenation?**
   a) It merges tuples in a new tuple  
   b) It modifies the original tuple  
   c) It does not work for tuples  
   d) It duplicates elements in a tuple  
   **Answer**: a) It merges tuples in a new tuple

### 14. **How do you repeat a tuple in Python?**
   a) Using the `*` operator  
   b) Using the `+` operator  
   c) Using the `repeat()` method  
   d) Using the `append()` method  
   **Answer**: a) Using the `*` operator

### 15. **Which of the following methods can be used to get the index of an element in a tuple?**
   a) `index()`  
   b) `find()`  
   c) `get()`  
   d) `search()`  
   **Answer**: a) `index()`

### 16. **Which of the following statements is true?**
   a) Tuples are mutable  
   b) Tuples can be modified after creation  
   c) Tuples are immutable  
   d) Tuples support the append operation  
   **Answer**: c) Tuples are immutable

### 17. **What will the following code output?**  
   ```python
   t = (1, 2, 3)
   print(t + (4, 5))
   ```  
   a) `(1, 2, 3, 4, 5)`  
   b) `(4, 5)`  
   c) `(1, 2, 3)`  
   d) `None`  
   **Answer**: a) `(1, 2, 3, 4, 5)`

### 18. **Which function is used to convert a list into a tuple?**
   a) `tuple()`  
   b) `list()`  
   c) `convert()`  
   d) `change()`  
   **Answer**: a) `tuple()`

### 19. **How do you access the last element of a tuple `t = (1, 2, 3)`?**
   a) `t[-1]`  
   b) `t[1]`  
   c) `t[0]`  
   d) `t[3]`  
   **Answer**: a) `t[-1]`

### 20. **What is the output of this code?**  
   ```python
   t = (1, 2, 3)
   t += (4, 5)
   print(t)
   ```  
   a) `(1, 2, 3, 4, 5)`  
   b) `(4, 5)`  
   c) `Error`  
   d) `(1, 2, 3)`  
   **Answer**: a) `(1, 2, 3, 4, 5)`

### 21. **Which of the following operations can be performed on tuples?**
   a) Insertion  
   b) Deletion  
   c) Concatenation  
   d) Modification  
   **Answer**: c) Concatenation

### 22. **What will the output of this code be?**  
   ```python
   t = (10, 20, 30)
   print(20 in t)
   ```  
   a) `True`  
   b) `False`  
   c) `Error`  
   d) `None`  
   **Answer**: a) `True`

### 23. **Which of the following methods is used to count the occurrences of an element in a tuple?**
   a) `count()`  
   b) `index()`  
   c) `find()`  
   d) `exists()`  
   **Answer**: a) `count()`

### 24. **What will be the result of this operation?**  
   ```python
   t = (1, 2, 3, 4)
   print(t[1:3])
   ```  
   a) `(2, 3)`  
   b) `(1, 2)`  
   c) `(2, 3, 4)`  
   d) `Error`  
   **Answer**: a) `(2, 3)`

### 25. **What will be the output of the following code?**  
   ```python
   t = (1, 2, 3, 4)
   print(t[:2])
   ```  
   a) `(1, 2)`  
   b) `(3, 4)`  
   c) `(2, 3)`  
   d) `Error`  
   **Answer**: a) `(1, 2)`

### 26. **Which of the following statements is true about tuples and lists?**
   a) Tuples are mutable, while lists are immutable  
   b) Tuples and lists both are immutable  
   c) Tuples are immutable, while lists are mutable  
   d) Neither tuples nor lists are immutable  
   **Answer**: c) Tuples are immutable, while lists are mutable

### 27. **Which operator can be used to repeat the elements of a tuple?**
   a) `+`  
   b) `*`  
   c) `-`  
   d) `/`  
   **Answer**: b) `*`

### 28. **How do you check if a tuple contains a specific element?**
   a) `contains()`  
   b) `search()`  
   c) `in`  
   d) `find()`  
   **Answer**: c) `in`

### 29. **What will be the result of this code?**  
   ```python
   t = (1, 2, 3)
   print(len(t))
   ```  
   a) `3`  
   b) `2`  
   c) `1`  
   d) `None`  
   **Answer**: a) `3`

### 30. **Which of the following is a valid tuple index range?**
   a) `t[1:3]`  
   b) `t[-1:2]`  
   c) `t[1:3, 2:4]`  
   d) `t[::2]`  
   **Answer**: a) `t[1:3]`

### 31. **Which of the following methods can be used to reverse a tuple?**
   a) `reverse()`  
   b) `reverse_tuple()`  
   c) `[::-1]`  
   d) `reversed()`  
   **Answer**: c) `[::-1]`

### 32. **Which of the following is not a valid tuple operation?**
   a) Concatenation  
   b) Indexing  
   c) Appending  
   d) Slicing  
   **Answer**: c) Appending

### 33. **What is the output of this code?**  
   ```python
   t = (1, 2, 3)
   print(3 in t)
   ```  
   a) `True`  
   b) `False`  
   c) `None`  
   d) `Error`  
   **Answer**: a) `True`

### 34. **What is the correct syntax for creating a tuple with mixed data types?**
   a) `tuple = (1, "a", 3.14)`  
   b) `tuple = [1, "a", 3.14]`  
   c) `tuple = {1, "a", 3.14}`  
   d) `tuple = 1, "a", 3.14`  
   **Answer**: a) `tuple = (1, "a", 3.14)`

### 35. **Which of the following is true for tuples?**
   a) Tuples can be modified in place  
   b) Tuples cannot be changed after creation  
   c) Tuples support insertion of new elements  
   d) Tuples support removing elements  
   **Answer**: b) Tuples cannot be changed after creation

### 36. **What is the result of this code?**  
   ```python
   t = (5, 6, 7)
   print(t[-2])
   ```  
   a) `6`  
   b) `7`  
   c) `5`  
   d) `None`  
   **Answer**: a) `6`

### 37. **Which method can be used to repeat the elements of a tuple?**
   a) `repeat()`  
   b) `*` operator  
   c) `append()`  
   d) `concatenate()`  
   **Answer**: b) `*` operator

### 38. **What is the output of this code?**  
   ```python
   t = (1, 2, 3)
   print(t[0:2])
   ```  
   a) `(1, 2)`  
   b) `(2, 3)`  
   c) `(1, 2, 3)`  
   d) `None`  
   **Answer**: a) `(1, 2)`

### 39. **How do you create a tuple with elements of different types?**
   a) `(1, "a", 3.14)`  
   b) `[1, "a", 3.14]`  
   c) `{1, "a", 3.14}`  
   d) `tuple(1, "a", 3.14)`  
   **Answer**: a) `(1, "a", 3.14)`

### 40. **Which of the following is the correct way to access the second element of a tuple?**
   a) `t[1]`  
   b) `t[2]`  
   c) `t[-2]`  
   d) `t[0]`  
   **Answer**: a) `t[1]`

### 41. **What is the default value of `args` in a function definition?**
   a) `None`  
   b) `()`  
   c) `[]`  
   d) `0`  
   **Answer**: b) `()`

### 42. **What does the `count()` method do?**
   a) Counts the number of elements in a tuple  
   b) Counts how many times an element appears in a tuple  
   c) Returns the index of the first occurrence of an element  
   d) Returns the total size of the tuple  
   **Answer**: b) Counts how many times an element appears in a tuple

### 43. **What will be the output of the following code?**  
   ```python
   t = (1, 1, 2, 2, 3)
   print(t.count(2))
   ```  
   a) `2`  
   b) `1`  
   c) `0`  
   d) `None`  
   **Answer**: a) `2`

### 44. **Which of the following methods is used to remove an element from a tuple?**
   a) `remove()`  
   b) `delete()`  
   c) `pop()`  
   d) None  
   **Answer**: d) None

### 45. **What is the result of the operation `t * 2` if `t = (1, 2)`?**
   a) `(1, 2, 1, 2)`  
   b) `(1, 2)`  
   c) `(2, 1)`  
   d) `None`  
   **Answer**: a) `(1, 2, 1, 2)`

### 46. **Which of the following is a valid slicing operation on a tuple `t = (10, 20, 30, 40)`?**
   a) `t[1:3]`  
   b) `t(1:3)`  
   c) `t[3:1]`  
   d) `t{1:3}`  
   **Answer**: a) `t[1:3]`

### 47. **Which of the following is true about tuples in Python?**
   a) Tuples can contain mutable and immutable types  
   b) Tuples can only contain immutable types  
   c) Tuples cannot contain mixed data types  
   d) Tuples cannot contain mutable types  
   **Answer**: a) Tuples can contain mutable and immutable types

### 48. **What will be the output of this code?**  
   ```python
   t = (1, 2, 3)
   t = t + (4,)
   print(t)
   ```  
   a) `(1, 2, 3, 4)`  
   b) `(4, 5)`  
   c) `(1, 2, 3)`  
   d) `None`  
   **Answer**: a) `(1, 2, 3, 4)`

### 49. **Which of the following methods is used to join two tuples?**
   a) `append()`  
   b) `join()`  
   c) `+` operator  
   d) `merge()`  
   **Answer**: c) `+` operator

### 50. **What will be the result of the following code?**  
   ```python
   t = (1, 2, 3)
   t = t * 2
   print(t)
   ```  
   a) `(1, 2, 3, 1, 2, 3)`  
   b) `(1, 2, 3)`  
   c) `None`  
   d) `Error`  
   **Answer**: a) `(1, 2, 3, 1, 2, 3)`
Here are 50 MCQs for **Session 9** on **File Handling**:

### 1. What does the `open()` function do in Python?
a) Creates a new file  
b) Opens a file for reading and writing  
c) Reads data from a file  
d) Deletes a file  

### 2. What is the default mode of the `open()` function when only the file name is provided?
a) 'w'  
b) 'r'  
c) 'a'  
d) 'x'

### 3. Which of the following modes is used for opening a file in binary format in Python?
a) 't'  
b) 'b'  
c) 'r'  
d) 'w'

### 4. What does the `'r'` mode do when used with the `open()` function?
a) Opens a file for reading only  
b) Opens a file for writing only  
c) Opens a file for both reading and writing  
d) Opens a file for appending

### 5. Which function is used to read the entire content of a file at once?
a) `read()`  
b) `readline()`  
c) `readlines()`  
d) `fread()`

### 6. What does the `write()` function do?
a) Reads data from a file  
b) Writes data to a file  
c) Closes a file  
d) Deletes a file

### 7. Which function is used to close a file after opening it?
a) `close()`  
b) `end()`  
c) `exit()`  
d) `quit()`

### 8. What happens when you try to open a non-existent file in 'r' mode?
a) An error occurs  
b) A new empty file is created  
c) The program continues without error  
d) It automatically opens in 'w' mode

### 9. Which of the following is the correct function to check whether a file exists in Python?
a) `os.file_exists()`  
b) `os.check()`  
c) `os.path.exists()`  
d) `os.exists()`

### 10. How do you open a file for writing in Python?
a) `open('file.txt', 'r')`  
b) `open('file.txt', 'w')`  
c) `open('file.txt', 'a')`  
d) `open('file.txt', 'b')`

### 11. What does the `'w'` mode do when used with the `open()` function?
a) Opens a file for writing, creates it if it doesn't exist, and truncates the file if it does  
b) Opens a file for reading only  
c) Opens a file for writing and reading  
d) Opens a file for appending data

### 12. How do you append text to a file in Python?
a) `open('file.txt', 'w')`  
b) `open('file.txt', 'a')`  
c) `open('file.txt', 'r')`  
d) `open('file.txt', 'x')`

### 13. What does the `os` module provide?
a) Access to operating system functionality  
b) Functions for reading files  
c) Functions for reading and writing data  
d) File handling features only

### 14. Which function is used to list the files and directories in the current directory?
a) `os.getfiles()`  
b) `os.listdir()`  
c) `os.filelist()`  
d) `os.dir()`

### 15. What does the `seek()` function do in file handling?
a) Moves the cursor to the beginning of the file  
b) Moves the cursor to a specific position in the file  
c) Reads data from the current cursor position  
d) Closes the file

### 16. How do you read a file line by line in Python?
a) `readline()`  
b) `readlines()`  
c) `open()`, then iterate over the file object  
d) `read()`  

### 17. Which of the following will raise an error while opening a file?
a) `open('file.txt', 'r')`  
b) `open('file.txt', 'w')`  
c) `open('file.txt', 'x')`  
d) `open('file.txt', 'b')`

### 18. Which function allows you to rename a file?
a) `os.rename()`  
b) `os.move()`  
c) `os.update()`  
d) `os.change_name()`

### 19. Which of the following is true about file access permissions in Linux/Unix?
a) Read and write permissions are given to all users by default  
b) Read, write, and execute permissions are given to the owner of the file  
c) No one has permission to read files  
d) Only the root user can read files

### 20. What does the `os.chmod()` function do in Python?
a) Changes file name  
b) Changes file permissions  
c) Copies a file  
d) Deletes a file

### 21. How do you open a file for both reading and writing?
a) `open('file.txt', 'r+')`  
b) `open('file.txt', 'rw')`  
c) `open('file.txt', 'w+')`  
d) `open('file.txt', 'a+')`

### 22. What function is used to read a file into a list of lines?
a) `readlines()`  
b) `read()`  
c) `line_read()`  
d) `read_file()`

### 23. Which of the following statements is used to handle exceptions in file handling?
a) `try-except`  
b) `if-else`  
c) `catch`  
d) `error`

### 24. In Python, how do you check if a directory exists?
a) `os.directory_exists()`  
b) `os.exists()`  
c) `os.path.isdir()`  
d) `os.isdir()`

### 25. How do you remove a file using Python?
a) `os.delete()`  
b) `os.remove()`  
c) `os.rmdir()`  
d) `os.unlink()`

### 26. Which of the following is used to get the current working directory in Python?
a) `os.cwd()`  
b) `os.getcwd()`  
c) `os.current()`  
d) `os.path.getcwd()`

### 27. What is the correct function to check if a file is open or closed?
a) `is_open()`  
b) `file.status()`  
c) `file.closed()`  
d) `file.is_closed()`

### 28. How do you open a file in write-only mode?
a) `open('file.txt', 'r')`  
b) `open('file.txt', 'w')`  
c) `open('file.txt', 'a')`  
d) `open('file.txt', 'x')`

### 29. Which of the following functions is used for reading the entire content of a file?
a) `fread()`  
b) `read()`  
c) `readlines()`  
d) `getline()`

### 30. How do you change the current directory in Python?
a) `os.setcwd()`  
b) `os.chdir()`  
c) `os.move()`  
d) `os.dirchange()`

### 31. Which of the following is not a valid file access permission in Unix/Linux?
a) `read`  
b) `write`  
c) `execute`  
d) `execute_read`

### 32. Which mode is used for exclusive creation of a file in Python?
a) `'x'`  
b) `'r'`  
c) `'w'`  
d) `'a'`

### 33. What is the file pointer's initial position when opening a file in `r` mode?
a) End of file  
b) Beginning of file  
c) Middle of file  
d) Random location

### 34. What is the purpose of the `os.path.join()` function?
a) Deletes a file  
b) Joins two or more path components  
c) Opens a file  
d) Changes file permissions

### 35. Which function is used to check the permissions of a file?
a) `os.check_permissions()`  
b) `os.access()`  
c) `os.get_permissions()`  
d) `os.file_permission()`

### 36. What is the difference between `os.remove()` and `os.rmdir()`?
a) `os.remove()` deletes a file, while `os.rmdir()` deletes an empty directory  
b) Both delete files  
c) `os.remove()` deletes an empty directory, while `os.rmdir()` deletes a file  
d) Both delete directories

### 37. What happens if you try to read a closed file?
a) Returns an empty string  
b) Throws an `OSError`  
c) Throws a `FileNotFoundError`  
d) Program continues without error

### 38. How do you read only the first line of a file?
a) `readline()`  
b) `readlines()`  
c) `fread(1)`  
d) `read(1)`

### 39. Which of the following file operations cannot be done directly with a file object in Python?
a) Read  
b) Write  
c) Rename  
d) Close

### 40. What does the `os.mkdir()` function do?
a) Opens a file  
b) Deletes a directory  
c) Creates a directory  
d) Renames a directory

### 41. Which of the following is a correct way to open a file in append mode?
a) `open('file.txt', 'r')`  
b) `open('file.txt', 'w')`  
c) `open('file.txt', 'a')`  
d) `open('file.txt', 'rw')`

### 42. Which of the following is used to check if a file is a directory or a regular file?
a) `os.isfile()`  
b) `os.isdir()`  
c) `os.isfile()`  
d) `os.file()`

### 43. What is the function to get the size of a file in Python?
a) `os.size()`  
b) `os.filesize()`  
c) `os.path.getsize()`  
d) `os.getsize()`

### 44. Which mode opens a file for writing only, creating the file if it doesn't exist, and truncating the file if it exists?
a) 'r'  
b) 'w'  
c) 'a'  
d) 'x'

### 45. What is the output of `open('file.txt', 'r').read(5)` if the file contains the text "Hello, World!"?
a) `Hello`  
b) `Hello,`  
c) `Hello, World!`  
d) `Hello, W`

### 46. Which Python function is used to read a file in binary mode?
a) `read()`  
b) `readlines()`  
c) `readbinary()`  
d) `open(file, 'rb')`

### 47. How can you check if a file is writable?
a) `os.writable(file)`  
b) `os.access(file, os.W_OK)`  
c) `file.iswritable()`  
d) `file.writable()`

### 48. Which of the following will read the next line from the file `file.txt`?
a) `file.read()`  
b) `file.readline()`  
c) `file.readlines()`  
d) `file.getline()`

### 49. What is the purpose of the `os.path.exists()` function?
a) Check if a directory exists  
b) Check if a file exists  
c) Create a file  
d) List files in a directory

### 50. How do you delete an empty directory in Python?
a) `os.remove()`  
b) `os.delete()`  
c) `os.rmdir()`  
d) `os.remove_dir()`

---
Here are 50 MCQs for **Session 10 & 11** on **Advanced Python: Object-Oriented Python** and **Regular Expressions**:

### 1. What is the primary concept of Object-Oriented Programming (OOP)?
a) Procedural programming  
b) Data abstraction  
c) Organizing code into objects  
d) Handling exceptions

### 2. Which of the following is a core concept of OOP?
a) Abstraction  
b) Encapsulation  
c) Inheritance  
d) All of the above

### 3. What is an object in Python?
a) A function that performs operations  
b) An instance of a class  
c) A built-in Python data type  
d) A type of variable

### 4. What is the purpose of indentation in Python?
a) To define code blocks and maintain readability  
b) To declare a variable  
c) To terminate a statement  
d) To specify data types

### 5. Which of the following is NOT a native data type in Python?
a) String  
b) Integer  
c) Set  
d) Class

### 6. What does the `=` operator do in Python?
a) Assigns a value to a variable  
b) Compares two values  
c) Checks for equality  
d) Assigns a reference to a variable

### 7. What is a class in Python?
a) A type of function  
b) A blueprint for creating objects  
c) A built-in data type  
d) A collection of data

### 8. What is an attribute in Python OOP?
a) A method of a class  
b) A variable associated with an object  
c) A class itself  
d) A type of constructor

### 9. Which of the following defines inheritance in OOP?
a) One class gets the properties and methods of another class  
b) A class can have multiple methods  
c) One class can inherit from multiple classes  
d) A class is composed of multiple objects

### 10. What is overloading in Python?
a) The ability to define multiple methods with the same name  
b) Changing the value of an attribute  
c) The process of hiding data  
d) The ability to extend the functionality of an existing method

### 11. What is method overriding in Python?
a) Defining a method in a derived class with the same name as in the base class  
b) Changing the value of an attribute  
c) Using a constructor to initialize the object  
d) Reusing a method from a parent class

### 12. What does data hiding mean in OOP?
a) Making the implementation details of a class private  
b) Making a method public  
c) Making a class method accessible to the outside world  
d) Reusing a method from a parent class

### 13. How do you create a class in Python?
a) `class MyClass:`  
b) `class MyClass() {}`  
c) `MyClass class:`  
d) `class MyClass()`

### 14. What keyword is used to initialize an object in Python?
a) `init()`  
b) `__init__()`  
c) `initialize()`  
d) `constructor()`

### 15. Which of the following is used to create a new instance of a class in Python?
a) `new MyClass()`  
b) `MyClass.new()`  
c) `MyClass()`  
d) `init(MyClass)`

### 16. What is the use of the `self` parameter in Python?
a) It refers to the current instance of the class  
b) It is used to define a variable  
c) It initializes the class  
d) It stores the method's return value

### 17. How do you access an object's attribute in Python?
a) `object.attribute`  
b) `object->attribute`  
c) `object[attribute]`  
d) `object{attribute}`

### 18. What is the purpose of the `__str__()` method in Python classes?
a) It initializes the class  
b) It returns a string representation of the object  
c) It compares two objects  
d) It overrides the class constructor

### 19. How can you call a method of a parent class from a child class in Python?
a) `super().method()`  
b) `self.parent().method()`  
c) `parent.method()`  
d) `base.method()`

### 20. What is polymorphism in Python?
a) Multiple objects having the same properties  
b) A single class having multiple methods with the same name  
c) One function performing different tasks based on input types  
d) All of the above

### 21. How do you define a regular expression in Python?
a) `regex = /pattern/`  
b) `regex = pattern()`  
c) `regex = "pattern"`  
d) `regex = re.compile("pattern")`

### 22. Which module is used for working with regular expressions in Python?
a) `re`  
b) `regex`  
c) `reg`  
d) `regexp`

### 23. What does the `re.match()` function do in Python?
a) Returns a list of all matches in a string  
b) Checks if the regular expression matches at the start of the string  
c) Searches for a match anywhere in the string  
d) Splits the string based on the pattern

### 24. What is the purpose of the `re.search()` function in Python?
a) Checks if a pattern matches the entire string  
b) Finds the first match of the pattern in the string  
c) Finds all matches of the pattern in the string  
d) Replaces occurrences of the pattern in the string

### 25. Which method in Python's `re` module is used to replace occurrences of a pattern in a string?
a) `re.replace()`  
b) `re.sub()`  
c) `re.substitute()`  
d) `re.update()`

### 26. How do you find all matches of a pattern in a string using regular expressions in Python?
a) `re.search()`  
b) `re.match()`  
c) `re.findall()`  
d) `re.sub()`

### 27. What does the `^` symbol represent in a regular expression?
a) Any character  
b) The start of the string  
c) A digit  
d) A whitespace

### 28. What does the `$` symbol represent in a regular expression?
a) The start of the string  
b) The end of the string  
c) Any character  
d) A digit

### 29. Which of the following regular expressions would match any string containing exactly 3 digits?
a) `\d{3}`  
b) `\d*3`  
c) `\d+3`  
d) `\d{3,5}`

### 30. What does the `\s` symbol represent in regular expressions?
a) A digit  
b) A whitespace character  
c) A word boundary  
d) Any character except whitespace

### 31. How do you compile a regular expression pattern in Python?
a) `re.compile(pattern)`  
b) `re.match(pattern)`  
c) `re.search(pattern)`  
d) `re.compile(pattern, flags)`

### 32. How would you extract all the words from a sentence in Python using regular expressions?
a) `re.findall(r'\w+', sentence)`  
b) `re.match(r'\w+', sentence)`  
c) `re.search(r'\w+', sentence)`  
d) `re.split(r'\w+', sentence)`

### 33. Which of the following is used to match any digit in a regular expression?
a) `\d`  
b) `\w`  
c) `\s`  
d) `\t`

### 34. What does the `re.sub()` function do in Python?
a) Substitutes a matched pattern with a replacement string  
b) Searches for a pattern in the string  
c) Matches a pattern at the beginning of a string  
d) Finds all occurrences of a pattern in the string

### 35. How do you match one or more occurrences of the preceding character in a regular expression?
a) `+`  
b) `*`  
c) `{n,}`  
d) `?`

### 36. Which of the following represents a non-digit character in regular expressions?
a) `\d`  
b) `\D`  
c) `\s`  
d) `\W`

### 37. How would you match the word "Python" in a case-insensitive manner using regular expressions in Python?
a) `re.match(r'python', string, re.I)`  
b) `re.match(r'python', string, re.C)`  
c) `re.match(r'Python', string)`  
d) `re.match(r'python', string, re.CASE_INSENSITIVE)`

### 38. Which function returns the match object in Python regular expressions?
a) `re.match()`  
b) `re.search()`  
c) `re.findall()`  
d) `re.sub()`

### 39. How do you match a specific number of occurrences of a character in regular expressions?
a) `{n}`  
b) `[n]`  
c) `n*`  
d) `+`

### 40. What does the `re.split()` function do?
a) Splits the string by occurrences of the pattern  
b) Splits the string by whitespace characters  
c) Finds the first match of the pattern  
d) Substitutes the pattern in the string

### 41. Which of the following regular expressions will match a word containing only letters?
a) `\w+`  
b) `\d+`  
c) `[a-zA-Z]+`  
d) `\s+`

### 42. How would you define

 a class in Python that inherits from another class?
a) `class ChildClass(BaseClass):`  
b) `class ChildClass extends BaseClass:`  
c) `class ChildClass inherits BaseClass:`  
d) `class ChildClass {}`

### 43. Which of the following methods is called when an object is created from a class in Python?
a) `__create__()`  
b) `__init__()`  
c) `__new__()`  
d) `__build__()`

### 44. What does the `super()` function do in Python?
a) Calls a method from the parent class  
b) Instantiates the current class  
c) Instantiates the base class  
d) Defines a new method in the child class

### 45. Which of the following symbols in regular expressions represents a word boundary?
a) `\b`  
b) `\s`  
c) `\d`  
d) `\W`

### 46. What will `re.findall(r'\d+', 'abc 123 def 456')` return?
a) `['123', '456']`  
b) `['abc', 'def']`  
c) `['123']`  
d) `['abc', '456']`

### 47. What does the `re.I` flag in regular expressions do?
a) Ignores whitespace  
b) Makes the regular expression case-insensitive  
c) Matches at the beginning of a string  
d) Replaces the match

### 48. Which of the following methods can be used to apply a regular expression to a string in Python?
a) `re.apply()`  
b) `re.match()`  
c) `re.execute()`  
d) `re.search()`

### 49. What will the expression `re.match(r'\d{3}', '12345')` return?
a) `None`  
b) `123`  
c) `12345`  
d) `True`

### 50. How do you define a regular expression pattern to match a phone number with the format `(xxx) xxx-xxxx` in Python?
a) `r'\(\d{3}\) \d{3}-\d{4}'`  
b) `r'(xxx) xxx-xxxx'`  
c) `r'\d{3}-\d{3}-\d{4}'`  
d) `r'(xxx) \d{3}-\d{4}'`

---

Here are 50 MCQs for **Session 12 & 13** on **Operations Exception, Exception Handling, Except Clause, Try-Finally Clause, and User Defined Exceptions**:

### 1. What is an exception in Python?
a) A syntax error  
b) A run-time error  
c) A program logic error  
d) A type of variable

### 2. Which Python statement is used to handle exceptions?
a) `throw`  
b) `try`  
c) `raise`  
d) `catch`

### 3. What is the purpose of the `except` clause in Python exception handling?
a) It defines the block of code that may raise an exception  
b) It handles the exception raised in the `try` block  
c) It initializes an exception  
d) It always executes regardless of an exception

### 4. What is the purpose of the `finally` clause in Python?
a) To handle exceptions  
b) To perform clean-up actions, regardless of whether an exception occurred or not  
c) To catch all exceptions  
d) To raise exceptions

### 5. What is the default behavior of Python when an exception is raised and not handled?
a) It terminates the program  
b) It skips the error and continues execution  
c) It re-raises the exception  
d) It asks the user to fix the error

### 6. Which of the following is NOT a built-in exception in Python?
a) `ValueError`  
b) `ZeroDivisionError`  
c) `FileNotFoundError`  
d) `UserNotFoundError`

### 7. Which block of code will always execute, regardless of whether an exception occurred?
a) `try`  
b) `except`  
c) `finally`  
d) `raise`

### 8. What is a user-defined exception in Python?
a) An exception defined by the Python interpreter  
b) An exception raised by the operating system  
c) An exception defined by the programmer to handle specific errors  
d) An exception raised during syntax errors

### 9. How do you raise an exception in Python?
a) `raise ExceptionType`  
b) `throw ExceptionType`  
c) `raise error`  
d) `raise error()`

### 10. Which of the following is the correct syntax for a `try`-`except` block in Python?
a) `try: code; except: code`  
b) `try code except code`  
c) `try: code except: code`  
d) `try code: except code:`

### 11. What happens if no exception occurs in the `try` block?
a) The `except` block is executed  
b) The program terminates  
c) The `finally` block is executed  
d) The `except` block is skipped

### 12. Which exception is raised when a division by zero occurs in Python?
a) `ZeroDivisionError`  
b) `TypeError`  
c) `ValueError`  
d) `IndexError`

### 13. Which of the following can you catch using a `try`-`except` block?
a) Syntax errors  
b) Runtime errors  
c) Compile-time errors  
d) System errors

### 14. What does the `else` clause do in an exception handling block?
a) It handles the exception  
b) It executes if no exception occurs  
c) It raises an exception  
d) It always executes after the `except` block

### 15. What is the correct way to catch a specific exception in Python?
a) `except ValueError as e:`  
b) `catch ValueError:`  
c) `catch (ValueError):`  
d) `catch as ValueError:`

### 16. How do you catch multiple exceptions in a single `except` clause?
a) `except (ValueError, TypeError) as e:`  
b) `except ValueError, TypeError as e:`  
c) `except (ValueError, TypeError):`  
d) `except ValueError or TypeError:`

### 17. What happens when an exception is raised inside a `finally` block?
a) The program will continue normally  
b) The exception is ignored  
c) The exception is re-raised after the `finally` block  
d) The exception is caught by the nearest `except` block

### 18. Can you have multiple `except` blocks for a single `try` block?
a) Yes, you can handle multiple exceptions  
b) No, you can only have one `except` block  
c) Yes, but only for the same exception type  
d) No, only one exception can be raised per block

### 19. How do you access the exception object in Python?
a) `as e`  
b) `with e`  
c) `except e:`  
d) `e.as`

### 20. Which of the following is the correct way to define a user-defined exception in Python?
a) `class MyException(Exception): pass`  
b) `class MyException: pass`  
c) `raise MyException`  
d) `class MyException(Exception): __init__`

### 21. What is the output of the following code?
```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Divided by zero")
finally:
    print("Execution finished")
```
a) "Divided by zero"  
b) "Execution finished"  
c) "Divided by zero" and "Execution finished"  
d) "Execution finished" and error

### 22. What is the result of the following code?
```python
try:
    x = 1 / 0
except TypeError:
    print("Type error")
except ZeroDivisionError:
    print("Division by zero")
```
a) "Type error"  
b) "Division by zero"  
c) Error  
d) Nothing happens

### 23. What is the correct way to raise an exception with a custom message?
a) `raise Exception("Custom message")`  
b) `raise("Custom message")`  
c) `raise "Custom message"`  
d) `raise Exception() with "Custom message"`

### 24. How do you catch all exceptions in Python?
a) `except *:`  
b) `except Exception as e:`  
c) `except:`  
d) `except all:`

### 25. Which method is used to re-raise the current exception in Python?
a) `raise()`  
b) `re_raise()`  
c) `re_raise_exception()`  
d) `raise Exception()`

### 26. Can a `try` block be empty in Python?
a) Yes, if there is an `except` block  
b) No, it must contain code to execute  
c) Yes, if there is a `finally` block  
d) Yes, but the program will not execute

### 27. What does the `with` statement do in Python regarding exceptions?
a) Automatically raises exceptions  
b) Handles exceptions without needing a `try` block  
c) Ensures that resources are cleaned up even if an exception occurs  
d) None of the above

### 28. Which of the following is the correct syntax for a `try`-`except` block with `else` and `finally`?
a) `try: code; except: code; else: code; finally: code`  
b) `try code except code else code finally code`  
c) `try: code except: code else: code finally: code`  
d) `try code except: code; else code finally code`

### 29. Can exceptions be nested in Python?
a) No, only one exception can be raised  
b) Yes, an exception can be raised within another exception block  
c) Yes, but the inner exception must be handled first  
d) No, exceptions must be handled in order

### 30. What type of exception is raised by Python if you try to open a non-existent file?
a) `FileNotFoundError`  
b) `IOError`  
c) `ValueError`  
d) `KeyError`

### 31. What is the purpose of a `finally` block in exception handling?
a) It handles exceptions if no `except` block exists  
b) It executes code that must run regardless of an exception  
c) It cleans up resources before exiting  
d) Both b and c

### 32. How do you handle multiple exceptions with the same `except` clause in Python?
a) By separating the exceptions with a comma  
b) By creating a list of exceptions  
c) By using a tuple of exception classes  
d) By using the `or` operator

### 33. What type of error occurs if you try to use an undefined variable in Python?
a) `NameError`  
b) `ValueError`  
c) `TypeError`  
d) `IndexError`

### 34. What will the following code print?
```python
try:
    int('xyz')
except ValueError:
    print("Value Error occurred")
finally:
    print("Always executed")
```
a) "Value Error occurred"  
b) "Always executed"  
c) "Value Error occurred" and "Always executed"  
d) Error is raised

### 35. Which of the following is the correct way to catch a specific exception in a `try` block?
a) `except SpecificError as e:`  
b) `catch SpecificError:`  
c) `except SpecificError:`  
d) `throw SpecificError`

### 36. Can you use multiple `finally` blocks in Python?
a) Yes, for different exception

 types  
b) No, only one `finally` block can be used  
c) Yes, but only if `except` is used  
d) Yes, but only for nested `try` blocks

### 37. What will happen if you forget to include a `finally` block in Python exception handling?
a) The program will crash  
b) Resources may not be cleaned up  
c) The program will terminate early  
d) The exception will not be caught

### 38. What type of error will be raised if you try to access an undefined dictionary key?
a) `KeyError`  
b) `ValueError`  
c) `IndexError`  
d) `AttributeError`

### 39. What is the default exception class in Python?
a) `Exception`  
b) `BaseException`  
c) `Error`  
d) `RuntimeError`

### 40. How do you catch a `KeyError` when accessing a dictionary in Python?
a) `except KeyError:`  
b) `except DictionaryError:`  
c) `except IndexError:`  
d) `catch KeyError:`

### 41. What happens if a `finally` block raises an exception?
a) The exception is handled by the nearest `except` block  
b) The exception is ignored  
c) The exception is re-raised  
d) The program crashes

### 42. Can a user-defined exception inherit from built-in exceptions in Python?
a) Yes  
b) No  
c) Only from `Exception`  
d) Only from `BaseException`

### 43. What will this code print?
```python
try:
    x = 1 / 0
except ZeroDivisionError as e:
    print("Caught:", e)
finally:
    print("Execution finished")
```
a) "Caught: division by zero"  
b) "Execution finished"  
c) "Caught: division by zero" and "Execution finished"  
d) "Execution finished" and error

### 44. How can you define a custom exception that includes a message?
a) By subclassing `Exception` and passing the message to the constructor  
b) By using `raise Exception("message")`  
c) By overriding the `__str__` method  
d) By using the `message` attribute

### 45. What is the result of this code?
```python
try:
    raise Exception("An error occurred")
except Exception as e:
    print(e)
```
a) "An error occurred"  
b) Error  
c) "Exception"  
d) No output

### 46. What is the purpose of exception handling in Python?
a) To handle errors without terminating the program  
b) To check for syntax errors  
c) To define exception types  
d) To prevent errors from occurring

### 47. Which of the following exceptions is raised when you try to access a non-existent file in Python?
a) `FileNotFoundError`  
b) `IOError`  
c) `OSError`  
d) `ValueError`

### 48. Which statement will NOT raise an exception?
a) `x = int('abc')`  
b) `x = 1 / 0`  
c) `x = len([1, 2, 3])`  
d) `x = open('nonexistent.txt')`

### 49. What will happen if an exception is not caught in Python?
a) The program terminates with a traceback  
b) The program will ignore the error and continue execution  
c) The program will enter an infinite loop  
d) The exception will be logged automatically

### 50. Which exception is raised when you attempt to divide a number by zero in Python?
a) `ZeroDivisionError`  
b) `IndexError`  
c) `NameError`  
d) `ValueError`

---

Here are 50 MCQs for **Session 14 & 15** on **Python Libraries, Servers and Clients Architecture, Writing Plugins in Python, Exploit Analysis Automation Process, Debugging Basics, and Introduction to Machine Learning Packages like NumPy**:

### Python Libraries and Functionality Programming

### 1. Which of the following is a Python library used for data manipulation and analysis?
a) NumPy  
b) Pandas  
c) Matplotlib  
d) Scikit-learn

### 2. What is the primary function of the `os` library in Python?
a) It performs numerical operations  
b) It allows interaction with the operating system  
c) It creates plots and graphs  
d) It handles file manipulation

### 3. How can you install an external library in Python?
a) `install library_name`  
b) `pip install library_name`  
c) `python install library_name`  
d) `library_name install`

### 4. Which of the following libraries is commonly used for data visualization in Python?
a) NumPy  
b) Pandas  
c) Matplotlib  
d) TensorFlow

### 5. What is the main purpose of the `math` library in Python?
a) File handling  
b) Performing mathematical operations  
c) String manipulations  
d) Database interactions

### 6. What does the `requests` library in Python do?
a) Handles machine learning tasks  
b) Interacts with web services and APIs  
c) Performs mathematical calculations  
d) Manages file system operations

### 7. What is the purpose of the `sys` library in Python?
a) It provides functions to work with system-level operations  
b) It handles file I/O  
c) It processes user input  
d) It generates random numbers

### 8. Which Python library is used for scientific computing and numerical analysis?
a) Pandas  
b) NumPy  
c) TensorFlow  
d) Matplotlib

### 9. What function in Python can be used to check if a library is already installed?
a) `library_exists()`  
b) `pip check`  
c) `import library`  
d) `list_installed()`

### 10. Which Python library is used for working with JSON data?
a) `os`  
b) `math`  
c) `json`  
d) `requests`

### 11. How do you import a library in Python?
a) `import library_name`  
b) `use library_name`  
c) `include library_name`  
d) `library_name import`

### 12. What does the `time` library in Python help with?
a) Handling date and time  
b) Performing mathematical operations  
c) String manipulation  
d) Handling external API requests

### 13. Which of the following is a Python library used for web development?
a) Flask  
b) Matplotlib  
c) NumPy  
d) Pandas

### 14. What is the primary purpose of the `tkinter` library in Python?
a) Web scraping  
b) Creating GUI applications  
c) Numerical operations  
d) Working with databases

### 15. Which library would you use to implement machine learning models in Python?
a) Pandas  
b) NumPy  
c) Scikit-learn  
d) Matplotlib

---

### Servers and Clients Architecture

### 16. In a client-server architecture, which entity sends requests for services or resources?
a) Server  
b) Database  
c) Client  
d) Middleware

### 17. What type of communication is used in client-server architecture?
a) One-way communication  
b) Peer-to-peer communication  
c) Two-way communication  
d) Broadcast communication

### 18. Which protocol is commonly used for communication in client-server architecture over the web?
a) SMTP  
b) HTTP  
c) FTP  
d) SNMP

### 19. In a client-server model, which entity provides the requested resources or services?
a) Server  
b) Client  
c) Database  
d) Proxy

### 20. What is the primary purpose of a server in client-server architecture?
a) To send requests to clients  
b) To manage and process client requests  
c) To store client data  
d) To handle user inputs

### 21. What is the role of a client in client-server architecture?
a) To provide data to the server  
b) To respond to requests from the server  
c) To request services or resources from the server  
d) To process requests

### 22. In client-server architecture, what is a common method of communication between the client and the server?
a) Sockets  
b) Variables  
c) Functions  
d) Files

### 23. Which of the following is a key characteristic of client-server architecture?
a) Decentralization  
b) All clients share a common resource  
c) Centralized management of resources  
d) Peer-to-peer communication

### 24. In a distributed client-server model, where are the resources typically stored?
a) On the client side  
b) In the cloud  
c) On the server side  
d) In both client and server

### 25. What is the purpose of a web server in client-server architecture?
a) To store data files  
b) To process client requests and return resources  
c) To serve as a database  
d) To create GUI interfaces for clients

---

### Writing Plugins in Python

### 26. What is a Python plugin?
a) A standalone application  
b) A small program that extends the functionality of an existing application  
c) A type of external library  
d) A function that modifies the operating system

### 27. How can you write a plugin in Python?
a) By creating a script and placing it in the application's plugin directory  
b) By importing built-in libraries only  
c) By compiling Python code into executable files  
d) By modifying the source code of the application

### 28. Which Python function is typically used for initializing plugins in an application?
a) `plugin_init()`  
b) `plugin_start()`  
c) `initialize()`  
d) `setup()`

### 29. In Python, how can plugins be dynamically loaded into an application?
a) Using `import` statements  
b) Using `plugin_loader` module  
c) Using `importlib` module  
d) Using `load_plugin()` function

### 30. What is the main advantage of using plugins in Python?
a) They reduce memory consumption  
b) They allow applications to be easily extended with new features  
c) They improve the performance of an application  
d) They increase the security of an application

---

### Exploit Analysis Automation Process

### 31. What is exploit analysis automation in cybersecurity?
a) Automatically fixing vulnerabilities  
b) Analyzing and automating the exploitation of security flaws  
c) Detecting and blocking network traffic  
d) Creating secure networks

### 32. Which of the following tools is commonly used in exploit analysis automation?
a) Metasploit  
b) Nmap  
c) Wireshark  
d) Docker

### 33. In the context of exploit analysis, what is a "payload"?
a) A command that checks for vulnerabilities  
b) A piece of malicious code that is delivered to a system during an attack  
c) A tool used to scan networks  
d) A type of firewall rule

### 34. What is the role of automation in exploit analysis?
a) To speed up the exploitation of security flaws  
b) To automatically patch vulnerabilities  
c) To increase the detection of malicious traffic  
d) To generate reports on system health

### 35. What is a key step in the exploit analysis automation process?
a) Scanning systems for vulnerabilities  
b) Updating software packages  
c) Writing new source code  
d) Creating network firewalls

---

### Debugging Basics

### 36. What is debugging in Python?
a) Writing comments in code  
b) Testing and fixing bugs in the code  
c) Writing the program  
d) Running the program

### 37. Which of the following tools can be used for debugging Python code?
a) `pytest`  
b) `pdb`  
c) `ipdb`  
d) All of the above

### 38. What does the `pdb` module in Python do?
a) It handles exceptions  
b) It debugs Python programs by providing an interactive shell  
c) It manages memory  
d) It formats output data

### 39. What is the purpose of breakpoints during debugging?
a) To halt the program at a specific point for inspection  
b) To terminate the program when a condition is met  
c) To log data during execution  
d) To measure performance

### 40. In Python, what function is used to trigger the debugger programmatically?
a) `break()`  
b) `debug()`  
c) `pdb.set_trace()`  
d) `traceback()`

---

### Introduction to Machine Learning Packages like NumPy

### 41. What is NumPy used for in Python?
a) Image processing  
b) Scientific computing and numerical operations  
c) Web development  
d) Machine learning model training

### 42. Which of the following is a key feature of NumPy?
a) Support for multi-dimensional arrays  
b) Support for text-based operations  
c) Support for complex file I/O  
d) Built-in machine learning algorithms

### 43. What is the main advantage of using NumPy arrays over Python lists?
a) NumPy arrays are more memory efficient and faster for numerical operations  
b) NumPy arrays can store objects of different types  
c) Python lists can be resized dynamically, but NumPy arrays cannot  
d) NumPy arrays are slower for large datasets

### 44. Which function in NumPy is used to create an array from a Python list?
a) `np.array()`  
b) `np.list

()`  
c) `np.create()`  
d) `np.new()`

### 45. What is the purpose of NumPy's `reshape()` function?
a) To create new arrays  
b) To change the dimensions of an existing array  
c) To calculate the sum of all elements in an array  
d) To merge multiple arrays into one

### 46. How can you install NumPy in Python?
a) `install numpy`  
b) `pip install numpy`  
c) `python -m numpy install`  
d) `numpy install`

### 47. Which of the following functions is used to compute the mean of a NumPy array?
a) `np.mean()`  
b) `np.average()`  
c) `np.sum()`  
d) `np.median()`

### 48. In NumPy, which function is used to perform element-wise addition between two arrays?
a) `np.add()`  
b) `np.concatenate()`  
c) `np.merge()`  
d) `np.stack()`

### 49. Which of the following is a feature of NumPy that makes it suitable for machine learning tasks?
a) Efficient handling of large datasets  
b) Built-in machine learning algorithms  
c) Integration with popular frameworks like TensorFlow  
d) Automatic tuning of models

### 50. Which NumPy function is used to generate random numbers?
a) `np.random.random()`  
b) `np.random.rand()`  
c) `np.random.randn()`  
d) All of the above

---
