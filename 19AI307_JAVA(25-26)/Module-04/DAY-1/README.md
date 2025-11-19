# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
You wrote a program that stores some input strings into a String array and prints each string in uppercase.
However, you're getting a NullPointerException.
What should you check in your array before calling .toUpperCase() on a element?

## AIM:
To avoid NullPointerException when converting strings from an array to uppercase by ensuring each array element is valid before calling .toUpperCase().

## ALGORITHM :
1.	Start the program.
2. Iterate through the `String[]` array using an index or enhanced for-loop.
3. For each element `s` do:

   * Check `if (s != null)` (and optionally `&& !s.isEmpty()` if empty strings are also undesirable).
   * If true, call `s.toUpperCase()` and print/use the result.
   * If false, handle the `null` case (skip, print placeholder, or log a message).
4. Continue until all elements are processed.
5. End the program.




## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class NullPointerArrayExample {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String input = sc.next();
        String str = input.equalsIgnoreCase("null") ? null : input;

        try {
            System.out.println(str.toUpperCase());
        } catch (NullPointerException e) {
            System.out.println("Null element");
        }

        sc.close();
    }
}
```







## OUTPUT:
<img width="405" height="200" alt="image" src="https://github.com/user-attachments/assets/60259ac8-11e9-4e75-a716-e9acca7c54d3" />



## RESULT:
Before calling .toUpperCase() on an array element, the element was checked for null. This prevented NullPointerException and allowed only valid strings to be converted to uppercase and printed.
