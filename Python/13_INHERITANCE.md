
# Python Inheritance

## Definition
Inheritance is a fundamental concept in object-oriented programming that allows one class (child or subclass) to inherit attributes and methods from another class (parent or superclass). This promotes code reusability and establishes a hierarchical relationship between classes.

## Key Features
- **Code Reusability**: Inherited attributes and methods can be reused in subclasses, reducing code duplication.
- **Method Overriding**: Subclasses can modify or extend the behavior of methods inherited from the parent class.
- **Polymorphism**: Inheritance allows for polymorphic behavior, where a method can be used in different contexts depending on the object.

## Types of Inheritance

### 1. Single Inheritance
A subclass inherits from a single superclass.

```python
class Parent:
    def greet(self):
        return "Hello!"

class Child(Parent):
    def farewell(self):
        return "Goodbye!"

child = Child()
print(child.greet())  # Output: Hello!
```

### 2. Multiple Inheritance
A subclass inherits from multiple superclasses.

```python
class Father:
    def skills(self):
        return "Gardening"

class Mother:
    def skills(self):
        return "Cooking"

class Child(Father, Mother):
    pass

child = Child()
print(child.skills())  # Output: Gardening (MRO determines which method is called)
```

### 3. Multilevel Inheritance
A subclass inherits from a superclass, which in turn inherits from another superclass.

```python
class Grandparent:
    def heritage(self):
        return "Family Heritage"

class Parent(Grandparent):
    def values(self):
        return "Family Values"

class Child(Parent):
    def beliefs(self):
        return "Personal Beliefs"

child = Child()
print(child.heritage())  # Output: Family Heritage
```

### 4. Hierarchical Inheritance
Multiple subclasses inherit from a single superclass.

```python
class Animal:
    def sound(self):
        return "Some sound"

class Dog(Animal):
    def sound(self):
        return "Bark"

class Cat(Animal):
    def sound(self):
        return "Meow"

dog = Dog()
cat = Cat()
print(dog.sound())  # Output: Bark
print(cat.sound())  # Output: Meow
```

### 5. Hybrid Inheritance
A combination of two or more types of inheritance.

```python
class A:
    def method_A(self):
        return "Method A"

class B(A):
    def method_B(self):
        return "Method B"

class C(A):
    def method_C(self):
        return "Method C"

class D(B, C):
    def method_D(self):
        return "Method D"

d = D()
print(d.method_A())  # Output: Method A
print(d.method_B())  # Output: Method B
print(d.method_C())  # Output: Method C
```

## Method Resolution Order (MRO)
MRO determines the order in which base classes are searched when executing a method. Python uses the C3 linearization algorithm to create a consistent order.

### Example of MRO
```python
class A:
    pass

class B(A):
    pass

class C(A):
    pass

class D(B, C):
    pass

print(D.__mro__)
# Output: (<class '__main__.D'>, <class '__main__.B'>, <class '__main__.C'>, <class '__main__.A'>, <class 'object'>)
```

## Summary
Inheritance in Python enhances code organization, reusability, and maintainability. Understanding the different types of inheritance and how to leverage them effectively is essential for designing robust object-oriented systems.
