# Core Java Concepts

## Overview
In this section, we will cover fundamental concepts of Java programming that form the building blocks for mastering Java SE 11.

## Topics Covered
1. Variables and Data Types
2. Operators
3. Control Flow Statements
4. Methods and Functions
5. Object-Oriented Programming (OOP) Principles
6. Inheritance and Polymorphism
7. Encapsulation and Abstraction
8. Interfaces and Abstract Classes
9. Packages and Modules
10. Exception Handling Basics

## Detailed Explanations

### Variables and Data Types
Variables are used to store data in a program. Java supports various data types such as int, double, boolean, and String.

```java
int age = 30;
double price = 19.99;
boolean isJavaFun = true;
String message = "Hello, Java!";
```

### Operators
Operators are symbols that perform operations on operands. Java includes arithmetic, relational, logical, and assignment operators.

```java
int sum = 10 + 5;
boolean isEqual = (5 == 5);
int result = (isTrue && isFalse) ? 1 : 0;
```

### Control Flow Statements
Control flow statements determine the order in which statements are executed. Java supports if-else, switch-case, while, do-while, and for loops.

```java
if (condition) {
    // code block
} else {
    // code block
}

switch (value) {
    case 1:
        // code block
        break;
    default:
        // code block
}

while (condition) {
    // code block
}

for (int i = 0; i < 5; i++) {
    // code block
}
```

### Methods and Functions
Methods are reusable blocks of code that perform specific tasks. They can have parameters and return values.

```java
public int add(int a, int b) {
    return a + b;
}
```

### Object-Oriented Programming (OOP) Principles
OOP is a programming paradigm based on the concept of objects. It includes principles like encapsulation, inheritance, and polymorphism.

### Inheritance and Polymorphism
Inheritance allows a class to inherit properties and behavior from another class. Polymorphism enables objects to be treated as instances of their parent class.

### Encapsulation and Abstraction
Encapsulation hides the internal state of an object and restricts access to it. Abstraction focuses on essential characteristics while hiding implementation details.

### Interfaces and Abstract Classes
Interfaces define a contract for classes to implement specific methods. Abstract classes provide partial implementation and cannot be instantiated.

### Packages and Modules
Packages organize classes into namespaces to avoid naming conflicts. Modules provide a higher level of encapsulation and dependency management.

### Exception Handling Basics
Exception handling allows the program to respond to unexpected events gracefully. It includes try-catch blocks to handle exceptions.

## Practice Questions
1. What is the difference between a class and an object in Java?
2. Explain the concept of method overloading with an example.
3. How does Java support multiple inheritance through interfaces?

## Mock Exam Question
Which of the following statements is true about Java variables?
A) Variables in Java must be explicitly declared with a data type.
B) Java variables can be declared without initializing them.
C) Once a variable is declared final, its value cannot be changed.
D) Java variables can have the same name within the same scope.

## Real-World Example
Consider a banking application where different account types are modeled using classes and inheritance to manage transactions efficiently.

## Case Study
Explore how a retail management system utilizes Java's OOP principles to handle inventory, sales, and customer data effectively.

