# Annotations

## Overview
Annotations in Java provide a powerful mechanism for adding metadata and information to Java code. They allow developers to embed additional information that can be used by the compiler or at runtime to perform specific tasks.

## Core Concepts
1. Annotation Syntax
2. Built-in Annotations
3. Custom Annotations
4. Annotation Processors

## Detailed Explanations

### Annotation Syntax
Annotations in Java are defined using the @ symbol followed by the annotation type. They can include elements with default values and can be applied to various program elements like classes, methods, fields, and parameters.

```java
@Deprecated
public class DeprecatedClass {
    // Class implementation
}
```

### Built-in Annotations
Java provides a set of built-in annotations like @Override, @SuppressWarnings, @Deprecated, @FunctionalInterface, etc., which serve different purposes in the codebase.

```java
@Override
public void someMethod() {
    // Method implementation
}
```

### Custom Annotations
Developers can create custom annotations to define their own metadata and use them in their code. Custom annotations can have elements, defaults, and retention policies based on the requirements.

```java
@Retention(RetentionPolicy.RUNTIME)
@Target(ElementType.METHOD)
public @interface CustomAnnotation {
    String value() default "Custom Annotation";
}
```

### Annotation Processors
Annotation processors are tools that process annotations at compile time and generate additional code or perform validations based on the annotations present in the code.

```java
public class CustomAnnotationProcessor extends AbstractProcessor {
    // Processor implementation
}
```

Annotations play a crucial role in modern Java development by enabling developers to express additional information and behaviors directly in the codebase.

