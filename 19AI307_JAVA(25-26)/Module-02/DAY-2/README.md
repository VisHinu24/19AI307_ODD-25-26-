# Ex.No:2(B) METHODS

## QUESTION:

Create two methods:

1. **double getArea(double r)** → Calculates and returns the area of a circle (should not print anything).
2. **void printArea(double area)** → Prints the calculated area.

The program reads the radius from the user, computes the area using `getArea()`, and prints it using `printArea()`.

Example:

| Input | Result |
| ----- | ------ |
| 2     | 12.56  |

---

## AIM:

To write a Java program that demonstrates the use of methods by calculating and printing the area of a circle using separate functions for computation and output.

---

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Define a method `getArea()` to calculate and return the area of a circle.
4. Define a method `printArea()` to print the area passed to it.
5. In the main method, get user input for radius.
6. Call `getArea()` to compute the area.
7. Call `printArea()` to display the area.
8. End the program.

---

## PROGRAM:

```
/*
Program to implement a Methods using Java
Developed by: H AARON
RegisterNumber: 212223040001
*/
```

---

## SOURCE CODE:

```
import java.util.*;
class prog {
    double getArea(double r) {
        return 3.14*r*r;
    }
    void printArea(double area) {
        System.out.printf("%.2f",area);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        prog obj = new prog();
        double r = sc.nextDouble();
        obj.printArea(obj.getArea(r));
    }
}
```

---

## OUTPUT:
<img width="436" height="215" alt="Screenshot 2025-11-24 at 1 24 49 PM" src="https://github.com/user-attachments/assets/17882dba-73b8-45c8-a2da-4987542fd5d5" />


---

## RESULT:

Thus, the Java program using methods to compute and display the area of a circle was successfully executed and the output was verified.
