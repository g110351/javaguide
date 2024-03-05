# Lambdas

## Overview
Lambdas are a powerful feature introduced in Java SE 8 that allows you to treat functionality as a method argument, essentially creating anonymous functions. Understanding lambdas is crucial for writing concise and expressive code in Java SE 11.

## Topics Covered
1. Lambda Expressions
2. Functional Interfaces
3. Syntax and Examples
4. Method References
5. Variable Capture and Effectively Final
6. Type Inference
7. Functional Interfaces in Java SE 11

## Detailed Explanations

### Lambda Expressions
Lambda expressions provide a concise way to represent anonymous functions. They consist of parameters, an arrow (->), and a body.

```java
// Syntax: (parameters) -> expression or {statements;}
Runnable task = () -> System.out.println("Hello, Lambda!");
```

### Functional Interfaces
Functional interfaces are interfaces with a single abstract method. Lambdas can be used to implement these interfaces concisely.

```java
@FunctionalInterface
interface Calculator {
    int operate(int a, int b);
}
```

### Syntax and Examples
Lambdas can be used in place of functional interfaces to simplify code and improve readability.

```java
Calculator add = (a, b) -> a + b;
int result = add.operate(10, 5);
```

### Method References
Method references provide a way to refer to methods without invoking them. They can be used as shorthand for lambda expressions.

```java
List<String> names = Arrays.asList("Alice", "Bob", "Charlie");
names.forEach(System.out::println);
```

### Variable Capture and Effectively Final
Lambdas can capture variables from their enclosing scope. However, these variables must be effectively final, meaning they are not reassigned.

```java
int multiplier = 2;
Calculator multiply = (a, b) -> a * b * multiplier;
```

### Type Inference
Java can infer the types of parameters in lambda expressions based on the context in which they are used, reducing the need for explicit type declarations.

```java
Comparator<String> lengthComparator = (s1, s2) -> s1.length() - s2.length();
```

### Functional Interfaces in Java SE 11
Java SE 11 introduced new functional interfaces in the java.util.function package, providing a standardized set of functional interfaces for common use cases.

```java
Predicate<String> isLong = s -> s.length() > 5;
boolean result = isLong.test("JavaLambda");
```

Start leveraging the power of lambdas in your Java development today!
