# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:
To write a Java program to implement composition where a Library contains multiple Book objects.

## ALGORITHM :
1. Start the program.
2. Create a class named Book with a book name attribute.
3. Create a class named Library.
4. Inside the Library class, create Book objects.
5. Store and display the details of the books.
6. Create an object of the Library class.
7. Call the method to display book details.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement composition using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.util.*;

public class CompositionExample 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) 
        {
            String title = sc.nextLine();
            String author = sc.nextLine();
            library.addBook(title, author);
        }

        library.showBooks();
        sc.close();
    }
}

class Book
{
    private String title;
    private String author;

    public Book(String title, String author) 
    {
        this.title = title;
        this.author = author;
    }

    public String getDetails() 
    {
        return title + " by " + author;
    }
}

class Library 
{
    private List<Book> books;

    public Library() 
    {
        books = new ArrayList<>();
    }

    public void addBook(String title, String author) 
    {
        books.add(new Book(title, author));
    }

    public void showBooks() 
    {
        System.out.println("Books in Library:");
        for (Book book : books) 
        {
            System.out.println("- " + book.getDetails());
        }
    }
}
```

## OUTPUT:
<img width="1292" height="640" alt="image" src="https://github.com/user-attachments/assets/f1d150be-ed00-4174-99a5-d4d8847a2cc1" />

## RESULT:
The Java program was executed successfully and the composition relationship between Library and Book objects was implemented successfully.
