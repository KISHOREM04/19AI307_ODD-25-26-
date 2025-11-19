# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a Java program to demonstrate a parameterized constructor.

## AIM:
To write a Java program that demonstrates the use of a parameterized constructor in a class.

## ALGORITHM :
1. Start the program.
2. Create a class with required instance variables.
3. Define a **parameterized constructor** that accepts values and initializes the variables.
4. Create an object of the class by passing arguments to the constructor.
5. Display the initialized values.
6. End the program.


## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Employee {
    String name;
    int id;

    Employee(String n, int i) {
        name = n;
        id = i;
    }

    void display() {
        System.out.println("Employee Name: " + name);
        System.out.println("Employee ID: " + id);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        int id = sc.nextInt();

        Employee e = new Employee(name, id);
        e.display();
    }
}
```







## OUTPUT:
<img width="499" height="264" alt="image" src="https://github.com/user-attachments/assets/de2464df-315b-4a54-86e4-5a281a30767d" />



## RESULT:
The program successfully demonstrated the use of a parameterized constructor to initialize object values at the time of object creation.
