# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:

Aliens scan DNA numbers and classify them based on specific rules:

* If the DNA number is divisible by 2 **and** ends in 4 → **Accepted**
* If the DNA number is divisible by 2 but ends in any digit other than 4 → **Suspect**
* If the DNA number is odd → **Rejected**

The program reads a single integer and prints one of the following based on the rules:
**Accepted**, **Suspect**, or **Rejected**.

---

## AIM:

To write a Java program that reads a DNA number and uses nested conditional statements to classify it as Accepted, Suspect, or Rejected based on divisibility and last digit.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Read an integer input from the user.
4. Check if the number is divisible by 2.
5. If it is divisible, check if the last digit is 4.
6. Print **Accepted** if it ends in 4; otherwise, print **Suspect**.
7. If the number is odd, print **Rejected**.
8. End the program.

---

## PROGRAM:

```
/*
Program to implement a conditional statement using Java
Developed by: H AARON
RegisterNumber: 212223040001
*/
```

---

## SOURCE CODE:

```
import java.util.*;

public class Main {
    public static void main(String args[]) {
        int n;
        Scanner sc = new Scanner(System.in);
        n = sc.nextInt();
        if(n%2==0) {
            if(n%10==4) System.out.println("Accepted");
            else System.out.println("Suspect");
        }
        else System.out.println("Rejected");
        
        sc.close();
    }
}
```

---

## OUTPUT:
<img width="820" height="279" alt="Screenshot 2025-11-24 at 1 08 59 PM" src="https://github.com/user-attachments/assets/940505e2-f028-4183-9f31-f5761f1ca531" />

---

## RESULT:

Thus, the Java program to classify DNA numbers using conditional statements was successfully executed and the output was verified.
