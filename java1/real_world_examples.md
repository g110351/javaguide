# Real-World Examples

## Example 1: Building a Banking Application
In this example, we will demonstrate how to create a simple banking application using Java SE 11. The application will allow users to perform basic banking operations such as deposit, withdrawal, and balance inquiry.

```java
public class BankAccount {
    private String accountNumber;
    private double balance;

    public BankAccount(String accountNumber, double initialBalance) {
        this.accountNumber = accountNumber;
        this.balance = initialBalance;
    }

    public void deposit(double amount) {
        balance += amount;
    }

    public void withdraw(double amount) {
        if (balance >= amount) {
            balance -= amount;
        } else {
            System.out.println("Insufficient funds");
        }
    }

    public double getBalance() {
        return balance;
    }
}

public class BankingApplication {
    public static void main(String[] args) {
        BankAccount account = new BankAccount("123456789", 1000.0);
        account.deposit(500.0);
        account.withdraw(200.0);
        System.out.println("Current Balance: " + account.getBalance());
    }
}
```

## Example 2: Implementing a Chat Application
In this example, we will showcase how to build a simple chat application using Java SE 11. The application will allow multiple users to exchange messages in real-time using sockets for communication.

```java
// Server side
public class ChatServer {
    public static void main(String[] args) {
        // Server implementation
    }
}

// Client side
public class ChatClient {
    public static void main(String[] args) {
        // Client implementation
    }
}
```

## Example 3: Developing a Task Scheduler
In this example, we will illustrate how to create a task scheduler application in Java SE 11. The application will enable users to schedule and execute tasks at specified intervals using Java's concurrency utilities.

```java
import java.util.concurrent.Executors;
import java.util.concurrent.ScheduledExecutorService;
import java.util.concurrent.TimeUnit;

public class TaskScheduler {
    public static void main(String[] args) {
        ScheduledExecutorService executor = Executors.newScheduledThreadPool(1);
        executor.scheduleAtFixedRate(() -> {
            // Task implementation
        }, 0, 1, TimeUnit.MINUTES);
    }
}
```

These real-world examples demonstrate practical applications of Java SE 11 concepts in building diverse types of applications. By understanding and implementing such examples, developers can enhance their Java programming skills and proficiency.
