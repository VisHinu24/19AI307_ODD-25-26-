# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:

Lovely is entering a battle arena tournament, but only heroes who meet specific power and skill criteria are allowed inside.

To enter the arena, a hero (Lovely) must satisfy **any one** of these conditions :

1. Her power level is above 80 **and** her rank is above 5
   → `(power > 80 && rank > 5)`

2. She has a magic orb **and** her experience is at least 3 years
   → `(hasMagicOrb == true && experience >= 3)`

**If either of the above conditions is satisfied, she is allowed to enter. Otherwise, she is rejected.**

### Input Format:

* First line: `int power`
* Second line: `int rank`
* Third line: `boolean hasMagicOrb`
* Fourth line: `int experience`

### Output Format:

```
Can Enter Arena: true/false
```

---

## AIM:

To write a Java program that reads a hero's attributes and evaluates logical conditions using AND (`&&`) and OR (`||`) operators to determine if she can enter the battle arena.

---

## ALGORITHM :

1. Start the program and create a `Scanner` object.
2. Read the hero’s power, rank, magic orb possession, and experience from the user.
3. Check if she satisfies either of the two entry conditions using logical operators.
4. Print `true` if she can enter the arena; otherwise print `false`.
5. End the program.

---

## PROGRAM:

```
/*
Program to implement variables and Operators using Java
Developed by: H AARON
RegisterNumber: 212223040001
*/
```

---

## Sourcecode.java:

```
import java.util.*;
public class Main {
    public static void main(String args[]) {
        int power, rank, experience;
        boolean hasMagicOrb;
        Scanner sc = new Scanner(System.in);
        power = sc.nextInt();
        rank = sc.nextInt();
        hasMagicOrb = sc.nextBoolean();
        experience = sc.nextInt();
        System.out.println("Can Enter Arena: " + ((power>80 && rank>5) || (hasMagicOrb==true && experience>=3)));
    }
}
```

---

## OUTPUT:
<img width="1214" height="543" alt="Screenshot 2025-11-22 at 8 51 37 PM" src="https://github.com/user-attachments/assets/65fd25d7-5b95-4209-be22-dea9304527e1" />



---

## RESULT:

Thus, the Java program using logical operators to determine a hero’s eligibility to enter the arena was successfully executed and verified.

