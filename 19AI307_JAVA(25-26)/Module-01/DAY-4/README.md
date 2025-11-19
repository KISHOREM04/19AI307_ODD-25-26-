# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to check if an element is present more than once in an array

## AIM:
To write a Java program that checks whether any element in an array appears more than once.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util` for reading input.
3. Create a Scanner object to take the size of the array and its elements from the user.
4. Store all the elements in an integer array.
5. Use a nested loop or a frequency-checking method:

   * For each element in the array, compare it with all other elements.
   * If a match is found (same value, different index), mark that a duplicate exists.
6. If any element repeats, display that a duplicate is found.
7. If no element repeats, display that all elements are unique.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement a Array using Java
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

        int n = sc.nextInt();
        int[] arr = new int[n];

        for (int i = 0; i < n; i++) {
            arr[i] = sc.nextInt();
        }

        boolean duplicateFound = false;
        for (int i = 0; i < n; i++) {
            for (int j = i + 1; j < n; j++) {
                if (arr[i] == arr[j]) {
                    duplicateFound = true;
                    break;
                }
            }
            if (duplicateFound) break;
        }

        if (duplicateFound)
            System.out.println("Yes");
        else
            System.out.println("No");

        sc.close();
    }
}
```







## OUTPUT:
<img width="265" height="467" alt="image" src="https://github.com/user-attachments/assets/e2b288a2-c196-487b-b948-8c14a6706a66" />



## RESULT:
The program successfully checks the given array and identifies whether any element appears more than once. It reports either "Duplicate found" or "No duplicates found" based on the array values.





