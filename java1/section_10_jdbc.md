# JDBC

## Overview
Java Database Connectivity (JDBC) is a standard Java API for connecting and interacting with relational databases. Understanding JDBC is essential for developing database-driven applications in Java.

## Core Concepts
1. JDBC Drivers
2. Connection Establishment
3. Statement Execution
4. ResultSet Handling
5. Transaction Management

## Detailed Explanations

### JDBC Drivers
JDBC drivers facilitate communication between Java applications and databases. There are four types of JDBC drivers: Type 1 (JDBC-ODBC bridge), Type 2 (Native API), Type 3 (Network Protocol), and Type 4 (Thin Driver).

```java
Class.forName("com.mysql.cj.jdbc.Driver");
Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/mydatabase", "username", "password");
```

### Connection Establishment
Establishing a connection to a database involves specifying the database URL, username, and password. The Connection interface represents a connection session with the database.

```java
Connection connection = DriverManager.getConnection("jdbc:mysql://localhost:3306/mydatabase", "username", "password");
```

### Statement Execution
Executing SQL statements in JDBC involves creating Statement or PreparedStatement objects. Statements can be used to execute queries, updates, and other SQL commands.

```java
Statement statement = connection.createStatement();
ResultSet resultSet = statement.executeQuery("SELECT * FROM users");
```

### ResultSet Handling
A ResultSet object represents the result set of a SQL query. Developers can iterate over the ResultSet to retrieve data from the database.

```java
while (resultSet.next()) {
    String name = resultSet.getString("name");
    int age = resultSet.getInt("age");
    System.out.println("Name: " + name + ", Age: " + age);
}
```

### Transaction Management
JDBC supports transaction management for ensuring data consistency in database operations. Transactions can be committed or rolled back based on the outcome of database operations.

```java
connection.setAutoCommit(false);
// Perform database operations
connection.commit();
```

### Best Practices
- Use PreparedStatement to prevent SQL injection attacks.
- Close resources (Connection, Statement, ResultSet) in a finally block.
- Handle exceptions gracefully and log errors for debugging.

Start leveraging JDBC to interact with databases effectively in your Java applications.

