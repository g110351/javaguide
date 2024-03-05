# I/O Operations

## Overview
In this section, we will delve into Input/Output (I/O) operations in Java, focusing on reading and writing data to files, streams, and other sources.

## Topics Covered
1. File Handling
2. Streams and Readers/Writers
3. Serialization and Deserialization
4. NIO (New I/O) Package
5. Working with Directories

## Detailed Explanations

### File Handling
File handling involves operations related to creating, reading, writing, and deleting files in Java. The java.io.File class is commonly used for file manipulation tasks.

```java
File file = new File("example.txt");
if (file.exists()) {
    // Perform operations
}
```

### Streams and Readers/Writers
Streams are used for reading and writing data sequentially, while Readers and Writers are used for character-based I/O operations. Java provides InputStream, OutputStream, Reader, and Writer classes for handling I/O operations.

```java
try (FileInputStream fis = new FileInputStream("input.txt");
     FileOutputStream fos = new FileOutputStream("output.txt")) {
    int data;
    while ((data = fis.read()) != -1) {
        fos.write(data);
    }
}
```

### Serialization and Deserialization
Serialization is the process of converting objects into a byte stream for storage or transmission, while deserialization is the reverse process of reconstructing objects from the byte stream. Java supports serialization through the Serializable interface and ObjectOutputStream/ObjectInputStream classes.

```java
class Person implements Serializable {
    String name;
    int age;
    // Other fields and methods
}

// Serialization
try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("person.ser"))) {
    oos.writeObject(new Person("Alice", 30));
}

// Deserialization
try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream("person.ser"))) {
    Person person = (Person) ois.readObject();
    System.out.println(person.getName());
}
```

### NIO (New I/O) Package
The java.nio package provides an alternative I/O mechanism introduced in Java 1.4, offering improved performance and scalability for I/O operations. It includes classes like Path, Files, and Channels for efficient file handling.

```java
Path path = Paths.get("data.txt");
List<String> lines = Files.readAllLines(path);
for (String line : lines) {
    System.out.println(line);
}
```

### Working with Directories
Java provides classes like File and Path for working with directories. Operations such as creating directories, listing files, and deleting directories can be performed using these classes.

```java
Path directory = Paths.get("data");
if (!Files.exists(directory)) {
    Files.createDirectory(directory);
}
```

Mastering I/O operations in Java is essential for handling data input and output effectively in your applications.

