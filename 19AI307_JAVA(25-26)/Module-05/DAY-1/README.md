# Ex.No:5(A) INPUTSTREAMREADER

## QUESTION:

Write a program to read user input from the keyboard using **InputStreamReader**.

### Example

| **Input** | **Result**    |
| --------- | ------------- |
| Manoj     | Hello, Manoj! |

## AIM:

To write a Java program that reads a string input from the keyboard using `InputStreamReader` and displays a greeting message.

## ALGORITHM :

1. Start the program.
2. Import the necessary packages `java.util` and `java.io`.
3. Create an `InputStreamReader` object to read user input.
4. Wrap it in a `BufferedReader` to read a line of text.
5. Read the user's name and print a greeting.
6. End the program.

## PROGRAM:

```
/*
Program to implement a InputStreamReader using Java
Developed by: H AARON 
RegisterNumber:  212223040001 
*/
```

## SOURCE CODE:

```java
import java.util.*;
import java.io.*;

class prog {
    public static void main(String args[]) throws IOException {
        Scanner sc = new Scanner(System.in);
        InputStreamReader isr = new InputStreamReader(System.in);
        BufferedReader br = new BufferedReader(isr);
        String name = br.readLine();
        System.out.println("Hello, " + name + "!");
    }
}
```

## OUTPUT:
<img width="473" height="266" alt="Screenshot 2025-11-24 at 2 06 57 PM" src="https://github.com/user-attachments/assets/1185f86e-bc37-4966-a795-4a95c5515ec8" />

## RESULT:

Thus, the Java program using `InputStreamReader` to read user input was successfully executed.
