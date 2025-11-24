# Ex.No:3(E) INNER CLASS

## QUESTION:

Write a Java program to create an inner class and access it from the outer class.

Input
Manoj
<br>
Result
Hello, Manoj! This message is from the Inner Class.

## AIM:

To write a Java program that demonstrates the creation of an inner class and accessing its method through the outer class.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create an outer class containing an inner class.
4. Define a method inside the inner class to display a message.
5. In the main method, create an object of the outer class and use it to create an object of the inner class.
6. Call the inner class method to display the message.
7. Stop the program.

## PROGRAM:

```
/*
Program to implement a InnerClass using Java
Developed by: H AARON 
RegisterNumber: 212223040001
*/
```

## SOURCE CODE:

```
import java.util.*;
class Outer {
    
    class Inner {
        void display(String name) {
            System.out.println("Hello, "+name+"! This message is from the Inner Class.");
        }
    }
}

class prog {
    public static void main(String args[]) {
        Scanner sc = new Scanner(System.in);
        Outer out = new Outer();
        Outer.Inner obj = out.new Inner();
        obj.display(sc.nextLine());
    }
}
```

## OUTPUT:
<img width="1044" height="214" alt="Screenshot 2025-11-24 at 1 45 06 PM" src="https://github.com/user-attachments/assets/c3a80eba-ee83-4bc7-afff-39411b79eb92" />

## RESULT:

Thus, the Java program demonstrating the use of an inner class and accessing it through the outer class was successfully executed.


