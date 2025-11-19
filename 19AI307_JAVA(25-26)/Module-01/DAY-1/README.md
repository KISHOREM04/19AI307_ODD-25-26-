# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is preparing a countdown for her rocket launch game. She has a starting number and wants to understand how subtracting with -- works in Java. But she's puzzled by the two types:

Post-decrement (a--) → value is used first, then decreased

Pre-decrement (--a) → value is decreased first, then used

To complete the launch program, help Lovely:

Take a countdown number as input.

Apply both post-decrement and pre-decrement on it.

Show how the value changes in each case.


## AIM:
To write a Java program that demonstrates the use of variables, data types, operators, and different print statements (print, println, and printf).

## ALGORITHM :
1.	Start the program.
2.	Import the required package java.util.* (optional).
3.	Declare variables of different data types (int, float, char, String).
4.	Perform simple arithmetic operations using operators.
5.	Use System.out.print() to display output on the same line.
6.	Use System.out.println() to display output on the next line.
7.	Use System.out.printf() to print formatted output.
8.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Datatypes using Java
Developed by: KISHORE M
RegisterNumber:212222040079
*/
```

## Sourcecode.java:
```
import java.util.Scanner;
public class Countdown {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int a = sc.nextInt();

        System.out.println("Initial countdown = " + a);
        System.out.println("After post-decrement (a--) = " + (a--) + ", Now a = " + a);
        System.out.println("After pre-decrement (--a) = " + (--a) + ", Now a = " + a);
    }
}
```





## OUTPUT:
<img width="844" height="240" alt="image" src="https://github.com/user-attachments/assets/dccd908a-41ce-472b-bbd3-cde8d4751182" />



## RESULT:
Thus, the Java program demonstrating variables, data types, operators, and print statements was successfully executed.



