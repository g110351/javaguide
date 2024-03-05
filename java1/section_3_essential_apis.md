# Essential APIs

## Overview
Essential APIs in Java SE 11 provide developers with a rich set of tools and libraries to build robust and efficient applications. Understanding and utilizing these APIs is crucial for mastering Java development.

## APIs Covered
1. java.lang Package
2. java.util Package
3. java.io Package
4. java.nio Package
5. java.net Package
6. java.time Package
7. java.util.concurrent Package
8. java.util.stream Package
9. java.lang.reflect Package
10. java.security Package

## Detailed Explanations

### java.lang Package
The java.lang package provides fundamental classes that are automatically imported into every Java program. It includes classes like Object, String, Integer, Double, and more.

```java
String message = "Hello, Java!";
int number = Integer.parseInt("42");
```

### java.util Package
The java.util package contains utility classes and data structures essential for everyday programming tasks. It includes classes like ArrayList, HashMap, LinkedList, and Collections.

```java
List<String> names = new ArrayList<>();
names.add("Alice");
names.add("Bob");
```

### java.io Package
The java.io package provides classes for input and output operations, including reading from and writing to files. It includes classes like FileInputStream, FileOutputStream, BufferedReader, and BufferedWriter.

```java
try (BufferedReader reader = new BufferedReader(new FileReader("input.txt"))) {
    String line = reader.readLine();
    System.out.println(line);
} catch (IOException e) {
    e.printStackTrace();
}
```

### java.nio Package
The java.nio package offers support for non-blocking I/O operations and buffer management. It includes classes like ByteBuffer, Channel, Selector, and Path.

```java
Path filePath = Paths.get("data.txt");
ByteBuffer buffer = ByteBuffer.allocate(1024);
```

### java.net Package
The java.net package provides classes for networking operations, such as creating network connections and handling URLs. It includes classes like URL, HttpURLConnection, and Socket.

```java
URL url = new URL("https://www.example.com");
HttpURLConnection connection = (HttpURLConnection) url.openConnection();
```

### java.time Package
The java.time package introduces new date and time classes that offer improved functionality over the legacy java.util.Date and java.util.Calendar classes. It includes classes like LocalDate, LocalTime, LocalDateTime, and ZonedDateTime.

```java
LocalDate today = LocalDate.now();
LocalTime now = LocalTime.now();
```

### java.util.concurrent Package
The java.util.concurrent package provides classes for concurrent programming, including thread management, synchronization, and executor services. It includes classes like Executor, ThreadPoolExecutor, and Future.

```java
ExecutorService executor = Executors.newFixedThreadPool(4);
executor.submit(() -> System.out.println("Task executed"));
executor.shutdown();
```

### java.util.stream Package
The java.util.stream package introduces the Stream API for functional-style operations on collections. It enables developers to perform operations like filtering, mapping, and reducing elements in a collection.

```java
List<Integer> numbers = Arrays.asList(1, 2, 3, 4, 5);
int sum = numbers.stream().filter(n -> n % 2 == 0).mapToInt(n -> n).sum();
```

### java.lang.reflect Package
The java.lang.reflect package provides classes and interfaces for advanced reflection capabilities, allowing developers to inspect and manipulate classes, methods, and fields at runtime. It includes classes like Class, Method, Field, and Constructor.

```java
Class<?> clazz = MyClass.class;
Method[] methods = clazz.getDeclaredMethods();
```

### java.security Package
The java.security package offers classes and interfaces for implementing security features in Java applications. It includes classes like MessageDigest, KeyPairGenerator, SecureRandom, and Signature.

```java
MessageDigest digest = MessageDigest.getInstance("SHA-256");
byte[] hash = digest.digest("Hello, Java!".getBytes());
```

Explore these essential APIs to enhance your Java programming skills and build powerful applications.

