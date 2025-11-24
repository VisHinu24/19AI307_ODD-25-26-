# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:

Simulate a fan speed controller using the **State Pattern**. Each time the user types **"next"**, change fan speed in the order:
**Off → Low → Medium → High → Off**.

### Example

| **Input**    | **Result**    |
| ------------ | ------------- |
| next<br>exit | Fan is on Low |

## AIM:

To write a Java program that implements the State Design Pattern to simulate a fan speed controller that cycles through multiple states (Off, Low, Medium, High) based on user input.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a `FanState` interface with methods `next()` and `printState()`.
4. Implement concrete state classes: OffState, LowState, MediumState, HighState.
5. Create a `Fan` class that maintains the current state.
6. Read user input and transition to the next state when "next" is entered.
7. Stop the program when "exit" is entered.

## PROGRAM:

```
/*
Program to implement a Behaviour Pattern using Java
Developed by: H AARON 
RegisterNumber:  212223040001 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

interface FanState {
    void next(Fan fan);
    void printState();
}

// write your code here

class OffState implements FanState {
    public void next(Fan fan) {
        fan.setState(new LowState());
    }
    public void printState() {
        System.out.println("Fan is Off");
    }
}

class LowState implements FanState {
    public void next(Fan fan) {
        fan.setState(new MediumState());
    }
    public void printState() {
        System.out.println("Fan is on Low");
    }
}

class MediumState implements FanState {
    public void next(Fan fan) {
        fan.setState(new HighState());
    }
    public void printState() {
        System.out.println("Fan is on Medium");
    }
}

class HighState implements FanState {
    public void next(Fan fan) {
        fan.setState(new OffState());
    }
    public void printState() {
        System.out.println("Fan is on High");
    }
}

class Fan {
    private FanState state;
    
    Fan() {
        this.state = new OffState();
    }
    
    public void setState(FanState state) {
        this.state = state;
    }
    
    public void pressButton() {
        state.next(this);
        state.printState();
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Fan fan = new Fan();
        while (true) {
            String input = scanner.nextLine();
            if (input.equalsIgnoreCase("exit")) break;
            if (input.equalsIgnoreCase("next")) fan.pressButton();
        }
    }
}
```

## OUTPUT:
<img width="586" height="417" alt="Screenshot 2025-11-24 at 2 04 46 PM" src="https://github.com/user-attachments/assets/5ef69194-ce9c-4878-b677-dcbb40e16b51" />

## RESULT:

Thus, the Java program implementing the Behavioural State Pattern for simulating a fan controller was executed successfully.
