# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is prime using wrapper classes. 

## AIM:
To write a Java program to check whether a given number is prime or not using Wrapper classes.

## ALGORITHM :
1. Start the program.
2. Create a `Scanner` object to read an integer from the user.
3. Store the input number using the `Integer` wrapper class.
4. Define a method `isPrime(Integer n)` to check if the number is prime.
5. If the number is less than or equal to 1, return false.
6. Check divisibility from 2 to `n/2`.
7. If divisible, it is not a prime number.
8. If no divisors are found, it is a prime number.
9. Display whether the number is prime or not.
10. Stop the program.





## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class PrimeCheck {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Integer num = sc.nextInt();
        boolean isPrime = true;

        if (num <= 1) {
            isPrime = false;
        } else {
            for (int i = 2; i <= Math.sqrt(num); i++) {
                if (num % i == 0) {
                    isPrime = false;
                    break;
                }
            }
        }

        if (isPrime)
            System.out.println(num + " is a prime number.");
        else
            System.out.println(num + " is not a prime number.");
    }
}
```






## OUTPUT:
<img width="580" height="211" alt="image" src="https://github.com/user-attachments/assets/c039f018-b673-4805-a6b1-4a4b8a303771" />



## RESULT:
Thus, the Java program to check whether a number is prime using Wrapper classes was successfully executed.
