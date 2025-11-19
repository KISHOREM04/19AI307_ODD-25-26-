# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Vehicle with attributes as number, type and owner.

## AIM:
To write a Java program that creates a class Vehicle with attributes number, type, and owner, reads input values from the user, and displays them in the required formatted output.

## ALGORITHM :
1. Start the program.
2. Create a class **Vehicle** with the following attributes:

   * `String number`
   * `String type`
   * `String owner`
3. Create a constructor to initialize the above variables.
4. In the main method:
   a. Create a Scanner object to read input.
   b. Read the three values: vehicle number, vehicle type, and owner name.
   c. Create two Vehicle objects using the input.
   d. Display each object's details in the format:

   ```
   number | type | owner
   ```
5. End the program.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: KISHORE M
RegisterNumber: 212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Vehicle
{
    String number;
    String type; 
    String owner;
}
public class Main 
{
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        Vehicle v1 = new Vehicle();
        v1.number = sc.next();
        v1.type = sc.next();
        v1.owner = sc.next();

        Vehicle v2 = new Vehicle();
        v2.number = sc.next();
        v2.type = sc.next();
        v2.owner = sc.next();

        System.out.println(v1.number + " | " + v1.type + " | " + v1.owner);
        System.out.println(v2.number + " | " + v2.type + " | " + v2.owner);

        sc.close();
    }
}
```




## OUTPUT:
<img width="644" height="198" alt="image" src="https://github.com/user-attachments/assets/6e2d0572-2d05-42a7-bc69-32fd633f160f" />



## RESULT:
The details of the vehicles entered by the user were successfully displayed using the Vehicle class.
