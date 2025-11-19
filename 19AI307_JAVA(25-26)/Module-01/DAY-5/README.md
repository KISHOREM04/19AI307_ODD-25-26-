# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:

Write a Java program to count the frequency of a given character in a string.


## AIM:
To write a Java program that counts how many times a specific character appears in a given string.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util` for reading user input.
3. Create a Scanner object to read a string from the user.
4. Read the character whose frequency needs to be counted.
5. Initialize a counter variable to zero.
6. Loop through each character of the string using a `for` loop.
7. For every character in the loop:

   * Compare it with the target character.
   * If they match, increment the counter.
8. After the loop ends, display the frequency count.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: KISHORE M
RegisterNumber:212222040079
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        char ch = sc.next().charAt(0);

        int count = 0;
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) == ch) {
                count++;
            }
        }

        System.out.println("Frequency of '" + ch + "' is: " + count);

        sc.close();
    }
}

```





## OUTPUT:
<img width="480" height="228" alt="image" src="https://github.com/user-attachments/assets/adc38118-f8bd-433e-805f-861f48b3a74e" />




## RESULT:
he program successfully counts and displays how many times the specified character appears in the given string.








