# Reflection

## Overview
Reflection in Java is a powerful feature that allows programs to inspect and manipulate classes, methods, fields, and other components of a Java program at runtime. It provides a way to obtain information about the structure of classes and their members, as well as to invoke methods dynamically.

## Core Concepts
1. Class Reflection
2. Method Reflection
3. Field Reflection
4. Constructor Reflection
5. Dynamic Invocation

## Detailed Explanations

### Class Reflection
The `Class` class in Java represents classes and interfaces at runtime. It provides methods to examine the runtime properties of a class, such as its name, superclass, implemented interfaces, constructors, methods, and fields.

```java
Class<?> clazz = MyClass.class;
String className = clazz.getName();
Class<?> superClass = clazz.getSuperclass();
Constructor<?>[] constructors = clazz.getConstructors();
Method[] methods = clazz.getMethods();
Field[] fields = clazz.getDeclaredFields();
```

### Method Reflection
Method reflection allows you to inspect and invoke methods dynamically. You can obtain information about a method's name, return type, parameter types, modifiers, and annotations.

```java
Method method = clazz.getMethod("methodName", parameterTypes);
Object result = method.invoke(instance, arguments);
```

### Field Reflection
Field reflection enables you to access and modify fields of a class dynamically. You can retrieve information about a field's name, type, modifiers, and annotations.

```java
Field field = clazz.getDeclaredField("fieldName");
field.setAccessible(true);
Object value = field.get(instance);
field.set(instance, newValue);
```

### Constructor Reflection
Constructor reflection allows you to create new instances of a class dynamically by invoking constructors. You can obtain information about a constructor's parameter types, modifiers, and annotations.

```java
Constructor<?> constructor = clazz.getConstructor(parameterTypes);
Object newInstance = constructor.newInstance(arguments);
```

### Dynamic Invocation
Reflection enables dynamic invocation of methods and constructors, allowing you to call methods and create objects based on runtime information.

```java
Method method = clazz.getMethod("methodName", parameterTypes);
Object result = method.invoke(instance, arguments);

Constructor<?> constructor = clazz.getConstructor(parameterTypes);
Object newInstance = constructor.newInstance(arguments);
```

Reflection should be used judiciously due to its potential performance overhead and complexity. It is commonly employed in frameworks, libraries, and tools that require runtime introspection and manipulation of Java classes.

