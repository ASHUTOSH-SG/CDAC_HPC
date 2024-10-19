
# Polymorphism in Python

## Definition
Polymorphism is the ability of a method to take on many forms. It allows methods to be defined in different ways depending on the object invoking them.

## Types of Polymorphism

### 1. Overriding
- **Definition**: Subclasses can modify or extend the behavior of inherited methods from parent classes.
- **Benefit**: Helps avoid redundant code by leveraging inherited methods, allowing for customized behavior in subclasses.

### Example of Overriding
```python
class Animal:
    def sound(self):
        return "Some sound"

class Dog(Animal):
    def sound(self):  # Overriding the inherited method
        return "Bark"

class Cat(Animal):
    def sound(self):  # Overriding the inherited method
        return "Meow"

# Using polymorphism
animals = [Dog(), Cat()]
for animal in animals:
    print(animal.sound())  # Output: Bark, Meow
```

### 2. Overloading
- **Note**: Method overloading (same method name with different parameters) is not supported directly in Python. Instead, default arguments or variable-length arguments can be used to achieve similar behavior.

### Example of Default Arguments
```python
class MathOperations:
    def add(self, a, b, c=0):  # Default argument for overloading
        return a + b + c

math = MathOperations()
print(math.add(2, 3))       # Output: 5
print(math.add(2, 3, 4))    # Output: 9
```

## Summary
Polymorphism is a powerful feature in Python that enhances flexibility and maintainability in code by allowing methods to be redefined in subclasses and enabling more dynamic method calls.



# `super()` in Python

## Definition
The `super()` function is used to call a method from a parent class within a subclass. It provides a way to access inherited methods that have been overridden in the subclass.

## Key Features
- **Method Resolution Order (MRO)**: `super()` follows the method resolution order, allowing it to find the next method in line to be executed from the parent class hierarchy.

## Usage

### Example of Using `super()`
```python
class Parent:
    def greet(self):
        return "Hello from Parent!"

class Child(Parent):
    def greet(self):
        parent_greeting = super().greet()  # Call the parent class method
        return f"{parent_greeting} And hello from Child!"

# Creating an instance of Child
child_instance = Child()
print(child_instance.greet())  
# Output: Hello from Parent! And hello from Child!
```

### MRO Example
To demonstrate the method resolution order:
```python
class A:
    def method(self):
        return "Method from A"

class B(A):
    def method(self):
        return super().method() + " and Method from B"

class C(A):
    def method(self):
        return super().method() + " and Method from C"

class D(B, C):
    def method(self):
        return super().method() + " and Method from D"

d_instance = D()
print(d_instance.method())  
# Output: Method from A and Method from C and Method from B and Method from D
```

## Summary
The `super()` function is essential for leveraging inheritance in Python, allowing subclasses to access and extend the functionality of parent class methods while maintaining the integrity of the method resolution order.
