# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to calculate the **power** of a given number.

Example:

| Input  | Result                                 |
| ------ | -------------------------------------- |
| 3<br>2 | 3.0 raised to the power of 2.0 is: 9.0 |

---

## AIM:

To write a Java program that reads the base and exponent values from the user and uses the `Math.pow()` function to compute the power.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Read the base and exponent values as double inputs.
4. Use the `Math.pow()` function to compute the power.
5. Display the result in the required format.
6. End the program.

---

## PROGRAM:

```
/*
Program to implement a Strings and Math Function using Java
Developed by: H AARON
RegisterNumber: 212223040001
*/
```

---

## SOURCE CODE:

```
import java.util.Scanner;

public class PowerCalculator {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        double base = sc.nextDouble();
        double exponent = sc.nextDouble();

        double result = Math.pow(base, exponent);

        System.out.println(base + " raised to the power of " + exponent + " is: " + result);
    }
}
```

---

## OUTPUT:
<img width="848" height="221" alt="Screenshot 2025-11-24 at 1 21 02 PM" src="https://github.com/user-attachments/assets/20f2ca02-9f13-4018-9736-5f5eedae09ef" />

---

## RESULT:

Thus, the Java program using `Math.pow()` to calculate the power of a number was successfully executed and the output was verified.
