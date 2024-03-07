# Collections Framework

## Overview
In this section, we will explore the Collections Framework in Java, which provides a set of interfaces and classes for working with collections of objects.

## Topics Covered
1. Introduction to Collections
2. Collection Interface
3. List Interface
4. Set Interface
5. Map Interface

## Detailed Explanations

### Introduction to Collections
The Collections Framework in Java provides a unified architecture for manipulating and storing groups of objects. It includes interfaces such as Collection, List, Set, and Map, along with their respective implementations.

```java
List<String> myList = new ArrayList<>();
myList.add("Apple");
myList.add("Banana");
```

### Collection Interface
The Collection interface is the root interface in the Collections Framework hierarchy. It defines common methods for working with collections, such as adding, removing, and iterating over elements.

```java
Collection<String> collection = new ArrayList<>();
collection.add("Apple");
collection.add("Banana");
System.out.println(collection.size()); // Output: 2
```

### List Interface
The List interface extends the Collection interface and represents an ordered collection of elements. It allows duplicate elements and provides methods for positional access and manipulation.

```java
List<String> list = new ArrayList<>();
list.add("Apple");
list.add("Banana");
list.add("Apple");
System.out.println(list.get(0)); // Output: Apple
```

### Set Interface
The Set interface extends the Collection interface and represents a collection of unique elements. It does not allow duplicate elements and provides methods for set operations such as union, intersection, and difference.

```java
Set<String> set = new HashSet<>();
set.add("Apple");
set.add("Banana");
set.add("Apple"); // Ignored, as it's a duplicate
System.out.println(set.size()); // Output: 2
```

### Map Interface
The Map interface represents a mapping between keys and values. It does not extend the Collection interface but is an integral part of the Collections Framework. Maps do not allow duplicate keys.

```java
Map<String, Integer> map = new HashMap<>();
map.put("Apple", 10);
map.put("Banana", 5);
System.out.println(map.get("Apple")); // Output: 10
```

Understanding the Collections Framework is crucial for effective data manipulation and organization in Java applications.
