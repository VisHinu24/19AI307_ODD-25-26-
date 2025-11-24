# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:

Create animals from two regions: **"Africa"** and **"Asia"**. Use the **Abstract Factory Pattern** to create families of animals (Herbivore, Carnivore). Print the interaction result.

### Example

| **Input** | **Result**           |
| --------- | -------------------- |
| africa    | Lion eats Wildebeest |

## AIM:

To write a Java program that implements the Abstract Factory Design Pattern to create related animal objects (Herbivore and Carnivore) from different regions and demonstrate their interaction.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create interfaces for Herbivore and Carnivore.
4. Implement concrete classes for African and Asian animals.
5. Create an AnimalFactory interface and concrete factories for Africa and Asia.
6. Read the region from user input and instantiate the appropriate factory.
7. Use the factory to create animals and print the interaction.
8. End the program.

## PROGRAM:

```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: H AARON 
RegisterNumber:  212223040001 
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}

class Wildebeest implements Herbivore {}

class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}

class Buffalo implements Herbivore {}

class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}

interface AnimalFactory {
    Carnivore createCarnivore();
    Herbivore createHerbivore();
}

class AfricaFactory implements AnimalFactory {
    public Carnivore createCarnivore() {
        return new Lion();
    }
    
    public Herbivore createHerbivore() {
        return new Wildebeest();
    }
}

class AsiaFactory implements AnimalFactory {
    public Carnivore createCarnivore() {
        return new Tiger();
    }
    
    public Herbivore createHerbivore() {
        return new Buffalo();
    }
}

// write your code here
public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;

        if (region.equals("africa")) factory = new AfricaFactory();
        else if (region.equals("asia")) factory = new AsiaFactory();
        else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}
```

## OUTPUT:
<img width="596" height="300" alt="Screenshot 2025-11-24 at 2 02 58 PM" src="https://github.com/user-attachments/assets/34c09671-c288-4750-adcd-62a29e3045cf" />

## RESULT:

Thus, the Java program implementing the Abstract Factory Design Pattern for creating region-based animal families was executed successfully.
