# Design Patterns

## Overview
Design patterns are reusable solutions to common problems encountered in software design and development. Understanding and applying design patterns can help improve the structure, flexibility, and maintainability of Java applications.

## Patterns Covered
1. Creational Patterns
   - Singleton Pattern
   - Factory Method Pattern
   - Abstract Factory Pattern
   - Builder Pattern
   - Prototype Pattern

2. Structural Patterns
   - Adapter Pattern
   - Bridge Pattern
   - Composite Pattern
   - Decorator Pattern
   - Facade Pattern
   - Flyweight Pattern
   - Proxy Pattern

3. Behavioral Patterns
   - Chain of Responsibility Pattern
   - Command Pattern
   - Interpreter Pattern
   - Iterator Pattern
   - Mediator Pattern
   - Memento Pattern
   - Observer Pattern
   - State Pattern
   - Strategy Pattern
   - Template Method Pattern
   - Visitor Pattern

## Detailed Explanations

### Singleton Pattern
The Singleton Pattern ensures that a class has only one instance and provides a global point of access to that instance.

```java
public class Singleton {
    private static Singleton instance;

    private Singleton() {
    }

    public static Singleton getInstance() {
        if (instance == null) {
            instance = new Singleton();
        }
        return instance;
    }
}
```

### Factory Method Pattern
The Factory Method Pattern defines an interface for creating objects but allows subclasses to alter the type of objects that will be created.

```java
public interface Product {
    void operation();
}

public class ConcreteProduct implements Product {
    @Override
    public void operation() {
        System.out.println("Performing operation in ConcreteProduct");
    }
}

public interface ProductFactory {
    Product createProduct();
}

public class ConcreteProductFactory implements ProductFactory {
    @Override
    public Product createProduct() {
        return new ConcreteProduct();
    }
}
```

### Observer Pattern
The Observer Pattern defines a one-to-many dependency between objects so that when one object changes state, all its dependents are notified and updated automatically.

```java
public interface Observer {
    void update();
}

public class ConcreteObserver implements Observer {
    @Override
    public void update() {
        System.out.println("ConcreteObserver has been updated");
    }
}

public interface Subject {
    void attach(Observer observer);
    void detach(Observer observer);
    void notifyObservers();
}

public class ConcreteSubject implements Subject {
    private List<Observer> observers = new ArrayList<>();

    @Override
    public void attach(Observer observer) {
        observers.add(observer);
    }

    @Override
    public void detach(Observer observer) {
        observers.remove(observer);
    }

    @Override
    public void notifyObservers() {
        for (Observer observer : observers) {
            observer.update();
        }
    }
}
```

## Real-World Examples
Design patterns are commonly used in various software projects. For example, the Observer Pattern can be seen in GUI frameworks for event handling, the Factory Method Pattern is used in libraries for object creation, and the Decorator Pattern is applied in stream processing libraries.

## Case Studies
Case studies on applying design patterns in real-world scenarios will be provided in this section to demonstrate the practical benefits and applications of design patterns in Java development.

