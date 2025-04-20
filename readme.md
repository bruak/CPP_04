# CPP Module 04

This repository contains the exercises for CPP Module 04, focusing on C++ polymorphism, abstract classes, and interfaces.

## Overview

This module explores subtype polymorphism, abstract classes, and interfaces in C++. The exercises revolve around implementing an animal class hierarchy that demonstrates how virtual methods, pure virtual methods, and deep copy concepts work in C++.

## Exercises

### Exercise 00: Polymorphism

An introduction to polymorphism in C++ through a basic animal class hierarchy.

#### Features:
- Base class `Animal` with virtual methods
- Derived classes `Cat` and `Dog` with overridden methods
- `WrongAnimal` and `WrongCat` classes to demonstrate incorrect polymorphism without virtual methods
- Proper memory management with appropriate destructors

#### Implementation Details:
- Virtual methods to enable method overriding in derived classes
- Orthodox Canonical Form implementation for all classes
- Demonstration of runtime polymorphism using base class pointers

### Exercise 01: I don't want to set the world on fire

Extends the previous exercise by adding a `Brain` class and implementing deep copies.

#### Features:
- `Brain` class with an array of ideas
- Deep copying for `Cat` and `Dog` classes
- Memory allocation and proper cleanup
- Testing for memory leaks

#### Implementation Details:
- Proper dynamic memory allocation for `Brain` objects
- Deep copy implementation in copy constructors and assignment operators
- Test cases to verify correct memory management
- Demonstration of the difference between shallow and deep copies

### Exercise 02: Abstract class

Further extends the hierarchy by making the `Animal` class abstract.

#### Features:
- Abstract `Animal` base class with pure virtual methods
- Implementation of pure virtual methods in derived classes
- Prevention of instantiating the abstract base class

#### Implementation Details:
- Pure virtual method `makeSound()` in the `Animal` class
- Concrete implementations of `makeSound()` in derived classes
- Test cases to verify that abstract classes cannot be instantiated

## Class Hierarchy

```
              Animal (abstract in ex02)
               /     \
              /       \
           Cat        Dog
          /            \
     Brain             Brain

      WrongAnimal
          |
      WrongCat
```

## Compilation

Each exercise comes with a Makefile that supports the following commands:
- `make`: Compile the program
- `make clean`: Remove object files
- `make fclean`: Remove object files and executable
- `make re`: Recompile the entire program

## Requirements

- C++ compiler with C++98 standard support
- Linux/macOS environment
- All code must compile with the following flags:
```
c++ -Wall -Wextra -Werror -std=c++98
```

## Technical Details

### Polymorphism

Polymorphism allows objects of different types to be treated as objects of a common base type. Key concepts demonstrated in these exercises include:

- Virtual functions enable runtime polymorphism
- Override of virtual functions in derived classes
- Virtual destructors ensure proper cleanup of derived objects

### Deep vs. Shallow Copy

A deep copy creates new copies of dynamically allocated objects, while a shallow copy only copies the pointers. In Exercise 01, we implement:

- Deep copying in copy constructors
- Deep copying in assignment operators
- Proper memory management to avoid memory leaks and double free issues

### Abstract Classes

An abstract class cannot be instantiated and serves as an interface for derived classes. In Exercise 02:

- The `Animal` class becomes abstract by declaring the `makeSound()` method as pure virtual
- Derived classes must implement all pure virtual methods
- Abstract classes can have concrete methods alongside pure virtual ones

## Notes

These exercises demonstrate essential C++ OOP concepts such as:
- Class hierarchies and relationships
- Runtime polymorphism with virtual functions
- Memory management with deep copying
- Interface design with abstract classes
- The importance of virtual destructors in base classes