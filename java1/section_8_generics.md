# Generics

## Overview
Generics in Java provide a way to create classes, interfaces, and methods that operate on objects of various types while providing compile-time type safety. Understanding generics is essential for writing flexible and reusable code in Java SE 11.

## Topics Covered
1. Introduction to Generics
2. Generic Classes and Interfaces
3. Generic Methods
4. Wildcards in Generics
5. Bounded Type Parameters
6. Generic Constraints and Type Inference
7. Erasure and Type Safety
8. Generic Collections

## Detailed Explanations

### Introduction to Generics
Generics allow classes and methods to operate on objects of any type, providing type safety at compile time.

```java
public class Box<T> {
    private T value;

    public void setValue(T value) {
        this.value = value;
    }

    public T getValue() {
        return value;
    }
}
```

### Generic Classes and Interfaces
Generic classes and interfaces can be parameterized with one or more type parameters to create reusable components.

```java
public interface List<T> {
    void add(T element);
    T get(int index);
}
```

### Generic Methods
Generic methods allow type parameters to be declared and used within a method, enabling flexibility in method signatures.

```java
public <T> T findMax(T[] array) {
    T max = array[0];
    for (T element : array) {
        if (element.compareTo(max) > 0) {
            max = element;
        }
    }
    return max;
}
```

### Wildcards in Generics
Wildcards enable flexibility in working with unknown types in generic classes and methods.

```java
public void printList(List<?> list) {
    for (Object element : list) {
        System.out.println(element);
    }
}
```

### Bounded Type Parameters
Bounded type parameters restrict the types that can be used as arguments in generics, providing additional compile-time checks.

```java
public <T extends Comparable<T>> T findMax(T[] array) {
    T max = array[0];
    for (T element : array) {
        if (element.compareTo(max) > 0) {
            max = element;
        }
    }
    return max;
}
```

### Generic Constraints and Type Inference
Constraints and type inference help ensure type safety and enable the compiler to infer types in generic contexts.

```java
List<String> stringList = new ArrayList<>();
stringList.add("Java");
String firstElement = stringList.get(0);
```

### Erasure and Type Safety
Java uses type erasure to implement generics, ensuring backward compatibility while maintaining type safety at runtime.

```java
List<Integer> intList = new ArrayList<>();
intList.add(10);
int value = intList.get(0);
```

### Generic Collections
Java provides generic collections such as List, Set, and Map to store and manipulate elements of specific types in a type-safe manner.

```java
List<String> names = new ArrayList<>();
names.add("Alice");
names.add("Bob");
String first = names.get(0);
```

Mastering generics is crucial for writing flexible and type-safe Java code. Practice using generics in various scenarios to enhance your Java programming skills.

