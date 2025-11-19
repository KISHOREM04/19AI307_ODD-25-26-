# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
A right-angled triangle star pattern is a common programming exercise used to practice nested loops in Java. In this pattern, stars (*) are printed in such a way that they form a right-angled triangle, where the right angle is aligned at the bottom-left corner.

Write a Java program that prints a right-angled triangle star pattern based on the number of rows entered by the user.
## AIM:
To write a Java program using looping statements to print a right-angled triangle star pattern based on user input.

## ALGORITHM :
1.	Start the program.

2.	Import the necessary package 'java.util'

3. Read the number of rows from the user.

4. Use an outer loop to iterate through each row.

5. Use an inner loop to print stars (*) for each row.

6. Move to the next line after printing stars for each row.

7. End the program.


## PROGRAM:
 ```
/*
Program to implement a Looping Statements using Java
Developed by: KISHORE M
RegisterNumber:212222040079
*/
```

## SOURCE CODE:

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int rows = scanner.nextInt();

        for (int i = 1; i <= rows; i++) {
            for (int j = 1; j <= i; j++) {
                System.out.print("* ");
            }
            System.out.println(); 
        }

        scanner.close();
    }
}
```




## OUTPUT:
<img width="399" height="395" alt="image" src="https://github.com/user-attachments/assets/07286d0c-5174-4702-8d58-34b630bd23d6" />



## RESULT:
Thus, the Java program using looping statements to print a right-angled triangle star pattern was successfully written, executed, and verified.





