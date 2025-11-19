# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to calculate the power of a given number.


## AIM:
To write a Java program to compute the power of a number using the Math.pow() function in Java.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the base value from the user.
4. Read the exponent value from the user.
5. Use the Math.pow(base, exponent) function to calculate the power.
6. Display the result.
7. Stop the program.

## PROGRAM:
 ```java
/*
Program to implement a Strings and Math Function using Java
Developed by: KISHORE M
RegisterNumber:212222040079
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class PowerCalculator
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        double base = sc.nextDouble();
        double exponent = sc.nextDouble();

        double result = Math.pow(base, exponent);

        System.out.println(base + " raised to the power of " + exponent + " is: " + result);
    }
}

```





## OUTPUT:
<img width="784" height="208" alt="image" src="https://github.com/user-attachments/assets/9dfc2e16-5d9b-489b-8d3b-2a3917f0875d" />



## RESULT:
Thus, the Java program to calculate the power of a given number using Math function was successfully executed.








