# Ex.No:3(D)    INTERFACE

## QUESTION:

Schools use different grading schemes. You need to build a system to plug different strategies.

SimpleGrader: A: 90+, B: 75–89, C: 60–74, F: below 60

StrictGrader: A: 95+, B: 85–94, C: 70–84, F: below 70

Input Format:
marks
graderType
marks: Integer (0–100)

graderType: 1 for SimpleGrader, 2 for StrictGrader

Output Format:
A / B / C / F

For example:

Input	Result
92 1
A

## AIM:

To write a Java program that implements grading strategies using interfaces by defining SimpleGrader and StrictGrader classes that apply different grading rules based on user choice.

## ALGORITHM :

1. Start the program.
2. Import the necessary package 'java.util'.
3. Define an interface grade with an abstract method grader().
4. Implement the interface in SimpleGrader and StrictGrader classes with different grading logic.
5. In the main method, read marks and grader type from the user.
6. Create the corresponding grader object based on user input.
7. Invoke the grader() method to print the grade.
8. Stop the program.

## PROGRAM:

```
/*
Program to implement Interface using Java
Developed by: H AARON 
RegisterNumber: 212223040001
*/
```

## SOURCE CODE:

```
import java.util.Scanner;
interface grade{
    void grader(int marks);
}
class SimpleGrader implements grade{
    public void grader(int marks){
        if(marks>=90)
        System.out.println("A");
        else if(marks>=75 && marks<=89)
        System.out.println("B");
        else if(marks>=60 && marks<=74)
        System.out.println("C");
        else
        System.out.println("F");
    }
}
class StrictGrader implements grade{
    public void grader(int marks){
        if(marks>=95)
        System.out.println("A");
        else if(marks>=85 && marks<=94)
        System.out.println("B");
        else if(marks>=70 && marks<=84)
        System.out.println("C");
        else
        System.out.println("F");
    }
}
public class main{
    public static void main(String args[]){
        Scanner sc = new Scanner(System.in);
        int marks = sc.nextInt();
        int choice = sc.nextInt();
        if(choice==1)
        {
            SimpleGrader obj = new SimpleGrader();
            obj.grader(marks);
        }
        else if(choice==2)
        {
            StrictGrader obj = new StrictGrader();
            obj.grader(marks);
        }
    }
}
```

## OUTPUT:
<img width="465" height="214" alt="Screenshot 2025-11-24 at 1 42 09 PM" src="https://github.com/user-attachments/assets/8e272002-2bc5-4051-86fc-b4cfb552565d" />

## RESULT:

Thus, the Java program using interfaces to implement multiple grading strategies was executed successfully.
