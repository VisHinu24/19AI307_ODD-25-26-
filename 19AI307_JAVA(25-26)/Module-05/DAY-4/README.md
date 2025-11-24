# Ex.No:5(D) THREAD PRIORITY

## QUESTION:

Write a java program for set the priority and name of the current thread.

Note : Read the threadname from the User

Set the Priority as 2.

### Input / Output Format:

| Input     | Result                                                                         |
| --------- | ------------------------------------------------------------------------------ |
| NewThread | Priority of Thread: 2<br>Name of Thread: NewThread<br>Thread[NewThread,2,main] |

## AIM:

To write a Java program that reads a thread name from the user, assigns it to the current thread, sets its priority to 2, and displays the updated thread details.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Read the thread name from the user.
4. Get the current executing thread.
5. Set the thread’s name and priority to 2.
6. Display the thread priority, name, and thread details.
7. Stop the program.

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
import java.util.Scanner;
public class Main{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String threadName = sc.nextLine();

        Thread t = Thread.currentThread();
        t.setName(threadName);
        t.setPriority(2);

        System.out.println("Priority of Thread: " + t.getPriority());
        System.out.println("Name of Thread: " + t.getName());
        System.out.println(t);
    }
}
```

## OUTPUT:
<img width="687" height="262" alt="Screenshot 2025-11-24 at 2 13 02 PM" src="https://github.com/user-attachments/assets/a710afc2-c9e9-4352-b018-427d0363fc8e" />

## RESULT:

Thus, the Java program to set and display the priority and name of the current thread was successfully executed.
