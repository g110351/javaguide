# Java SE 11 Features

## Overview
Java SE 11 introduced several new features and enhancements to the Java platform, providing developers with improved tools and capabilities for building robust and efficient applications.

## Features Covered
1. Local-Variable Syntax for Lambda Parameters
2. HTTP Client API
3. Nest-Based Access Control
4. Dynamic Class-File Constants
5. Epsilon Garbage Collector
6. Flight Recorder
7. Z Garbage Collector
8. Unicode 10 Support
9. TLS 1.3 Support
10. Single-File Source-Code Launch

## Detailed Explanations

### Local-Variable Syntax for Lambda Parameters
Java SE 11 allows the use of var in lambda expressions to declare local variables with inferred types.

```java
(var x, var y) -> x + y
```

### HTTP Client API
The new HTTP Client API provides a modern and flexible way to make HTTP requests and handle responses.

```java
HttpClient client = HttpClient.newHttpClient();
HttpRequest request = HttpRequest.newBuilder()
    .uri(URI.create("https://www.example.com"))
    .GET()
    .build();
HttpResponse<String> response = client.send(request, HttpResponse.BodyHandlers.ofString());
```

### Nest-Based Access Control
Nest-based access control simplifies access to private members of nested classes and interfaces.

```java
class Outer {
    private int outerVar;

    class Inner {
        private int innerVar;

        void accessOuter() {
            outerVar = 10;
        }
    }
}
```

### Dynamic Class-File Constants
Dynamic class-file constants allow the loading of constants at runtime, improving performance and flexibility.

```java
class Constants {
    static final int MAX_SIZE = 100;
    static final int DYNAMIC_SIZE = Integer.getInteger("dynamic.size");
}
```

### Epsilon Garbage Collector
The Epsilon GC is a no-op garbage collector that handles memory allocation without performing any actual garbage collection.

```java
java -XX:+UseEpsilonGC MyApp
```

### Flight Recorder
Flight Recorder provides low-overhead profiling and diagnostics for Java applications, capturing detailed runtime information.

```java
java -XX:+UnlockCommercialFeatures -XX:+FlightRecorder MyApp
```

### Z Garbage Collector
The Z GC is a scalable garbage collector designed for low-latency and high-throughput applications.

```java
java -XX:+UseZGC MyApp
```

### Unicode 10 Support
Java SE 11 adds support for Unicode 10.0.0, including new characters and scripts.

### TLS 1.3 Support
Transport Layer Security (TLS) 1.3 is supported in Java SE 11, offering improved security and performance for network communication.

### Single-File Source-Code Launch
Java SE 11 allows the execution of a single Java source file directly without the need for compilation.

```java
java HelloWorld.java
```

## Practice Questions
1. How does the HTTP Client API improve handling of HTTP requests in Java SE 11?
2. Explain the concept of nest-based access control and its benefits.
3. What is the purpose of the Epsilon Garbage Collector in Java SE 11?

## Mock Exam Question
...(about 12 lines omitted)...
