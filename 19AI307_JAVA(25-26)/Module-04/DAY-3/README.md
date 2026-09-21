# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:
To architect a tightly coupled Library–Book ecosystem where Book objects are fully lifecycle-dependent on the Library. This demonstrates Composition by ensuring books are instantiated, managed, and destroyed exclusively through the Library container.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Instantiate the Library object that internally creates and retains Book instances.
4.	Read user inputs for book details and populate the Library.
5.	Trigger the Library’s display function to showcase all composed Book objects.
6.	Terminate the program lifecycle.

## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: Syed Mohamed Raihan M
RegisterNumber: 212224240167
*/
```

## SOURCE CODE:

```java
import java.util.*;

class Book {
    private String title;
    private String author;

    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    public String getDetails() {
        return "- " + title + " by " + author;
    }
}

class Library {
    private List<Book> books;

    public Library() {
        books = new ArrayList<>();
    }

    public void addBook(String title, String author) {
        books.add(new Book(title, author));
    }

    public void showBooks() {
        System.out.println("Books in Library:");
        for (Book b : books) {
            System.out.println(b.getDetails());
        }
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = Integer.parseInt(sc.nextLine());
        Library library = new Library();

        for (int i = 0; i < n; i++) {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}
```

## OUTPUT:

<img width="703" height="428" alt="image" src="https://github.com/user-attachments/assets/061f969e-2e6c-4458-a579-c654e4a63ecb" />

## RESULT:

Thus the output is executed successfully.
