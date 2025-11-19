# Ex.No:4(C)  COMPOSITION IN JAVA

## QUESTION:
Implement a system where a Library contains multiple Book objects. Each Book is created inside the Library. Books can't exist independently (Composition).

## AIM:
To implement Composition in Java where a Library object contains multiple Book objects, and the Book objects cannot exist independently outside the Library.

## ALGORITHM :
1.	Start the program.
2. Create a class **Book** with attributes such as `title` and `author`.
3. Do **not** allow Book objects to be created outside — create them **only inside** the Library class.
4. Create a class **Library** that:

   * Holds a list/array of Book objects.
   * Has a method to add new books (internally creates Book objects).
   * Has a method to display all books.
5. In the main method:

   * Create a Library object.
   * Add books using Library’s method.
   * Display all books.
6. End.




## PROGRAM:
 ```
/*
Program to implement a Composition Concepts in Java
Developed by: KISHORE M
RegisterNumber: 212222040079
*/
```

## SOURCE CODE:
```java
import java.util.*;

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
        this.books = new ArrayList<>();
    }

    public void addBook(String title, String author) 
    {
        Book newBook = new Book(title, author);
        this.books.add(newBook);
    }

    public void showBooks() 
    {
        System.out.println("Books in Library:");
        for (Book book : this.books) 
        {
            System.out.println("- " + book.getDetails());
        }
    }
}

public class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        Library library = new Library();

        int n = 0;
        if (sc.hasNextInt()) 
        {
            n = sc.nextInt();
        }
        sc.nextLine();

        for (int i = 0; i < n; i++) 
        {
            if (!sc.hasNextLine()) break;
            String title = sc.nextLine().trim();
            if (!sc.hasNextLine()) break;
            String author = sc.nextLine().trim();
            library.addBook(title, author);
        }

        library.showBooks();

        int m = 0;
        if (sc.hasNextInt()) 
        {
            m = sc.nextInt();
        } 
        else 
        {
            sc.close();
            return;
        }
        sc.nextLine();
        
        for (int i = 0; i < m; i++) 
        {
            if (!sc.hasNextLine()) break;
            String title = sc.nextLine().trim();
            if (!sc.hasNextLine()) break;
            String author = sc.nextLine().trim();
            library.addBook(title, author);
            
            library.showBooks();
        }
    }
}
```






## OUTPUT:
<img width="764" height="451" alt="image" src="https://github.com/user-attachments/assets/40081a1e-c21d-425f-8596-7ddb28cebab6" />



## RESULT:
The system demonstrates Composition, where the Library fully owns the Book objects. When the Library object is destroyed, all its Book objects cease to exist, proving strong ownership and lifetime dependency.
