# Ex.No:2(B) METHODS

## QUESTION:
Create two methods:

Get the input for radius from the user.

double getArea(double r) → calculate the area and return the area(Don't print anything in this method).

void printArea(double area) → pass the calculated area to this method and print the area of a circle.


## AIM:
To write a Java program that gets the radius of a circle from the user, calculates the area using a method, and prints the area using another method.

## ALGORITHM :
1. Start the program.
2. Read the radius value from the user.
3. Create the method `double getArea(double r)` to:

   * Calculate area using the formula: **area = 3.14 × r × r**
   * Return the calculated area (do not print inside this method).
4. Create the method `void printArea(double area)` to:

   * Print the area passed as an argument.
5. Call both methods in the main method.
6. End the program.





## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: KISHORE M
RegisterNumber: 212222040079
*/
```

## SOURCE CODE:
```java
import java.util.*;
public class Main
{
    static double getarea(double r)
    {
        return 3.14*r*r;
    }
    static void printarea(double area)
    {
        System.out.printf("%.2f",area);
    }
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        double r=sc.nextDouble();
        double area=getarea(r);
        printarea(area);
    }
}
```






## OUTPUT:

<img width="352" height="137" alt="image" src="https://github.com/user-attachments/assets/6295413a-7f9b-4249-afc3-f8caa2530290" />


## RESULT:
The program successfully calculated the area of a circle using the getArea() method and printed the result using the printArea() method.
