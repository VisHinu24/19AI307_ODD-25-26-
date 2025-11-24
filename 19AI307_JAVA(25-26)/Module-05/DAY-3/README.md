# Ex.No:5(C)  FILE HANDLING USING JAVA

## QUESTION:

Write a Java program to read a file and print only the lines containing the word **"Java"**.

## AIM:

To write a program that accepts user input, stores it in a file, and displays only the lines that contain the word **"Java"**.

## ALGORITHM :

1. Start the program.
2. Import the necessary packages (`java.io.*`, `java.util.*`).
3. Create a `File` object and a `FileWriter` to write user input into the file.
4. Read user input until the user types `"exit"`.
5. Write each line into the file.
6. After writing, read the file using `BufferedReader`.
7. Print only the lines that contain the word `"Java"`.
8. Close all streams.

---

## PROGRAM:

```
/*
Program to implement File Handling using Java
Developed by: H AARON
RegisterNumber:  212223040001
*/
```

## SOURCE CODE:

```java
import java.io.*;
import java.util.Scanner;

class prog {
    public static void main(String args[]) throws IOException {

        Scanner sc = new Scanner(System.in);
        File file = new File("sample.txt");
        FileWriter writer = new FileWriter(file);

        System.out.println("Enter lines (type 'exit' to stop):");

        while (true) {
            String line = sc.nextLine();
            if (line.equals("exit")) break;
            writer.write(line + "\n");
        }

        writer.close();

        System.out.println("Lines containing the word 'Java':");

        BufferedReader br = new BufferedReader(new FileReader(file));
        String l;

        while ((l = br.readLine()) != null) {
            if (l.contains("Java")) {
                System.out.println(l);
            }
        }

        br.close();
    }
}
```

---

## OUTPUT:
<img width="898" height="354" alt="Screenshot 2025-11-24 at 2 10 11 PM" src="https://github.com/user-attachments/assets/27d36f63-d030-42fe-bf3e-bd3dd31cb773" />


---

## RESULT:

Thus, the program to read a file and print lines containing the word **"Java"** was successfully executed.
