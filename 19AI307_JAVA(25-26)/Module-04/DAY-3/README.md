# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:

Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

For example:

**Input / Result**
2
Java
James Gosling
Python
Guido Van Rossum
Books in Library:

* Java by James Gosling
* Python by Guido Van Rossum

1
Machine Learning
Andrew Ng
Books in Library:

* Machine Learning by Andrew Ng

## AIM:

To write a Java program that demonstrates Composition by creating Book objects inside a Library class, ensuring Books cannot exist independently and displaying all stored books.

## ALGORITHM :

1. Start the program.
2. Import the necessary package `java.util`.
3. Create a `Book` class with title and author attributes.
4. Create a `Library` class that holds a list of Book objects and methods to add and display books.
5. Read user input for the number of books, then their titles and authors.
6. Add books to the library and display the list.
7. Stop the program.

## PROGRAM:

```
/*
Program to implement a Composition Concepts in Java
Developed by: H AARON
RegisterNumber: 212223040001 
*/
```

## SOURCE CODE:

```
import java.util.*;

public class CompositionExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return title + " by " + author;
    }
}

class Library {
    private List<Book> books = new ArrayList<>();

    public void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println("- " + b.getDetails());
        }
    }
}
```

## OUTPUT:
<img width="884" height="505" alt="Screenshot 2025-11-24 at 1 58 51 PM" src="https://github.com/user-attachments/assets/adc58acf-8232-4d80-b17e-fa99fff86b42" />


## RESULT:

Thus, the Java program demonstrating Composition using a Library and Book classes was successfully executed and verified.
