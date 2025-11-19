# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Floyd’s Triangle is a right-angled triangular arrangement of numbers where the numbers start from 1 and increase sequentially row by row.

Write a Java program that:

Prompts the user to enter the number of rows for the triangle.

Uses nested loops to print Floyd’s Triangle.

Ensures that the numbers increase sequentially from the top row to the bottom row.
## AIM:
To write a Java program that reads the number of rows from the user and prints Floyd’s Triangle using nested loops, ensuring numbers increase sequentially from 1 onward.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util` for taking input.
3. Create a Scanner object to read the number of rows from the user.
4. Initialize a counter variable starting from 1.
5. Use an outer loop to iterate from row 1 to the given number of rows.
6. For each row, use an inner loop to print as many numbers as the current row number.
7. In the inner loop:

   * Print the current value of the counter.
   * Increment the counter after each print.
8. Move to the next line after each row.
9. Continue until the triangle is fully printed.
10. End the program.

## PROGRAM:
 ```
/*
Program to implement a Looping Statements using Java
Developed by: KISHORE M
RegisterNumber:212222040079
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;
public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int rows = scanner.nextInt();

        int number = 1; 

        for (int i = 1; i <= rows; i++) {
            
            for (int j = 1; j <= i; j++) {
                System.out.print(number + " ");
                number++; 
            }
            System.out.println(); 
        }

        scanner.close();
    }
}

```




## OUTPUT:
<img width="378" height="339" alt="image" src="https://github.com/user-attachments/assets/9e1ac824-8275-4658-93e6-adb780f370b5" />



## RESULT:
The program successfully prints Floyd’s Triangle, with numbers arranged in a right-angled triangular pattern and incrementing sequentially from the first row to the last.





