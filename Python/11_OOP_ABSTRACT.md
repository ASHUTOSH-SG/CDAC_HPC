
# Abstract Classes in Python

## Definition
An abstract class is a class that contains one or more abstract methods. It cannot be instantiated directly and serves as a blueprint for its subclasses, enforcing a contract that ensures certain methods are implemented.

## Key Features
- **Abstract Methods**: Methods that are declared but contain no implementation. They must be overridden in subclasses.
- **Decorator**: Abstract methods are marked with the `@abstractmethod` decorator.
- **Importing**: To use abstract classes, you need to import the `abc` module.

## Usage

### Example of an Abstract Class
```python
from abc import ABC, abstractmethod

class Animal(ABC):  # Inherit from ABC
    @abstractmethod
    def sound(self):  # Abstract method
        pass

class Dog(Animal):
    def sound(self):  # Implementing the abstract method
        return "Bark"

class Cat(Animal):
    def sound(self):  # Implementing the abstract method
        return "Meow"

# Cannot instantiate an abstract class
# animal = Animal()  # Raises TypeError

# Instantiating subclasses
dog = Dog()
cat = Cat()
print(dog.sound())  # Output: Bark
print(cat.sound())  # Output: Meow
```

## Summary
Abstract classes in Python provide a way to define common interfaces for a group of related classes while ensuring that specific methods are implemented in those subclasses. This promotes code consistency and enforces a design contract.
