# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:

You are writing a Java program where you read a string input. If the input is "init", you create an object and call its method. If it's "null", no object is created. Your program crashes with a NullPointerException when "null" is entered.

## AIM:

To write a Java program that demonstrates exception handling by catching a NullPointerException when an object is not initialized.

## ALGORITHM :

1. Start the program.
2. Import the necessary package 'java.util'.
3. Read a string input from the user.
4. Declare an object reference and assign it null.
5. Create an object only if the user enters "init".
6. Attempt to call a method inside a try block.
7. Catch NullPointerException and display an appropriate message.
8. End the program.

## PROGRAM:

```
/*
Program to implement a Exception Handling using Java
Developed by: H AARON
RegisterNumber: 212223040001
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

class Example {
    void display() {
        System.out.println("Object exists");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        
        Example ex = null;

        if(str.equalsIgnoreCase("init")) {
            ex = new Example();
        } 
        
        try {
            ex.display();
        } catch (NullPointerException e) {
            System.out.println("Object is null");
        }
    }
}
```

## OUTPUT:
<img width="571" height="208" alt="Screenshot 2025-11-24 at 1 51 47 PM" src="https://github.com/user-attachments/assets/bda29941-8fd1-4218-a8cb-8cd02183ea49" />

## RESULT:

Thus, the Java program to demonstrate exception handling using NullPointerException was successfully implemented.
