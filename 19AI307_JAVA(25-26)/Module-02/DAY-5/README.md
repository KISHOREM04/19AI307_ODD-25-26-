# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Student with variables name, rollNumber. Create a method setDetails(String name, int rollNumber),and display them.

## AIM:
To write a Java program that creates a class Student with variables name and rollNumber, sets the details using a method, and displays them.

## ALGORITHM :
1. Start the program.
2. Create a class **Student** with two instance variables:

   * `String name`
   * `int rollNumber`
3. Create a method `setDetails(String name, int rollNumber)` to assign values to these variables.
4. Create a method `display()` to print the student details.
5. In the main method:

   * Create an object of Student
   * Call the `setDetails()` method
   * Call the `display()` method
6. End the program.




## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Student 
{
    String name;
    int rollNumber;
    void setDetails(String name,int rollNumber)
    {
        System.out.println("Name: "+name);
        System.out.println("Roll Number: "+rollNumber);
    }
}

class prog 
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        String name=sc.nextLine();
        int rn=sc.nextInt();
        Student s=new Student();
        s.setDetails(name,rn);
    }
}
```





## OUTPUT:
<img width="450" height="275" alt="image" src="https://github.com/user-attachments/assets/b12dd9bd-d421-4d39-a550-58933436b107" />



## RESULT:
The program successfully stored student details using the setDetails() method and displayed them using the display() method.
