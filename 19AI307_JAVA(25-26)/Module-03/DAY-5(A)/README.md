# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program where the inner class is declared private and accessed through a method in the outer class. 

## AIM:
To write a Java program where a private inner class is declared inside an outer class and accessed using a public method of the outer class.

## ALGORITHM :
1. Start the program.
2. Create an outer class `Outer`.
3. Inside it, declare a **private inner class** `Inner`.
4. The inner class should have a method (e.g., `showMessage()`) that prints a message.
5. In the outer class, create a **public method** `accessInner()` that:

   * Creates an object of the private inner class
   * Calls its method
6. In the main method, create an object of `Outer` and call `accessInner()`.
7. End the program.




## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Outer {
    private class Inner {
        int data;
        Inner(int data) { this.data = data; }
        void display() { System.out.println("Data set inside private inner class: " + data); }
    }

    void createInner(int data) {
        Inner inner = new Inner(data);
        inner.display();
    }
}

public class PrivateInnerDemo {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int input = sc.nextInt();
        Outer outer = new Outer();
        outer.createInner(input);
    }
}
```






## OUTPUT:
<img width="773" height="210" alt="image" src="https://github.com/user-attachments/assets/139bd0d2-11c2-4689-a617-67709a24fbb4" />



## RESULT:
The program successfully demonstrated accessing a private inner class through a public method of the outer class.
