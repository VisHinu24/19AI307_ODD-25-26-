# Ex.No:5(E) MULTITHREADING - SYNCHRONIZATION

## QUESTION:

You are asked to simulate a ticket booking system where multiple users (threads) try to book seats for an event. The system starts with a certain number of available seats. Each thread tries to book a given number of seats. You must ensure the booking is done safely using synchronization, preventing overbooking.

Implement the following:
A class **TicketCounter** with a synchronized method **bookTicket(String name, int seats)**.

* If enough seats are available, confirm the booking.
* If not, print a message indicating failure to book.

### Input Format:

```
<initial_seats>
<number_of_users>
<user_name> <seats_requested>
<user_name> <seats_requested>
```

### Example Input / Output:

| Input                                    | Result                                                                                                                                                |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| 10<br>3<br>Alice 4<br>Bob 5<br>Charlie 3 | Alice successfully booked 4 seats. Remaining: 6<br>Charlie successfully booked 3 seats. Remaining: 3<br>Bob failed to book 5 seats. Only 3 available. |

## AIM:

To develop a Java program that demonstrates multithreading with synchronization by allowing multiple users (threads) to safely book seats without causing race conditions or overbooking.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Read initial seat count and number of users.
4. Create a `TicketCounter` object with the initial seat count.
5. Create and start threads for each user attempting to book seats.
6. Use a synchronized method to ensure safe booking.
7. Wait for all threads to finish execution.
8. Stop the program.

## PROGRAM:

```
/*
Program to implement a Composition Concepts in Java
Developed by: H AARON 
RegisterNumber:  212223040001 
*/
```

## SOURCE CODE:

```
import java.util.*;

class TicketCounter {
    private int availableSeats;

    public TicketCounter(int seats) {
        this.availableSeats = seats;
    }

    public synchronized void bookTicket(String name, int seatsRequested) {
        if (seatsRequested <= availableSeats) {
            System.out.println(name + " successfully booked " + seatsRequested + " seats. Remaining: " + (availableSeats - seatsRequested));
            availableSeats -= seatsRequested;
        } else {
            System.out.println(name + " failed to book " + seatsRequested + " seats. Only " + availableSeats + " available.");
        }
    }
}

public class Main {
    public static void main(String[] args) throws Exception {
        Scanner sc = new Scanner(System.in);
        int initialSeats = sc.nextInt();
        int numUsers = sc.nextInt();

        TicketCounter counter = new TicketCounter(initialSeats);
        Thread[] users = new Thread[numUsers];

        sc.nextLine();

        for (int i = 0; i < numUsers; i++) {
            String name = sc.next();
            int seats = sc.nextInt();
            users[i] = new Thread(() -> counter.bookTicket(name, seats));
            users[i].start();
        }

        for (Thread t : users) {
            t.join();
        }
    }
}
```

## OUTPUT:
<img width="898" height="354" alt="Screenshot 2025-11-24 at 2 10 11 PM" src="https://github.com/user-attachments/assets/d12ce409-687a-4653-84e2-77ee7df7448d" />

## RESULT:

Thus, the Java program that demonstrates multithreading with synchronization for a ticket booking system was successfully executed.
