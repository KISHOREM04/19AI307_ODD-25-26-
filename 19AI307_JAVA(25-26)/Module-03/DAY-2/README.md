# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program using method overriding. Create a superclass Bank with a method getInterestRate() returning 0. Create subclasses SBI, ICICI, and HDFC that override the method.

## AIM:
To write a Java program that demonstrates method overriding by creating a superclass Bank with a method getInterestRate() and subclasses SBI, ICICI, and HDFC that override this method to return different interest rates.

## ALGORITHM :
1. Start the program.
2. Create a superclass **Bank** with a method `getInterestRate()` that returns **0**.
3. Create subclasses **SBI**, **ICICI**, and **HDFC**.
4. In each subclass, override `getInterestRate()` to return a specific interest rate.
5. In the main method:

   * Create objects of SBI, ICICI, and HDFC.
   * Call their `getInterestRate()` methods.
6. Display the interest rates.
7. End the program.





## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: KISHORE M
RegisterNumber: 212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Bank {
    public double getInterestRate() {
        return 0;
    }
}

class SBI extends Bank {
    public double getInterestRate() {
        return 6.5;
    }
}

class ICICI extends Bank {
    public double getInterestRate() {
        return 7.0;
    }
}

class HDFC extends Bank {
    public double getInterestRate() {
        return 7.5;
    }
}

public class BankTest {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Bank b;

        String bankName = scanner.nextLine().trim().toUpperCase();

        switch (bankName) {
            case "SBI":
                b = new SBI();
                break;
            case "ICICI":
                b = new ICICI();
                break;
            case "HDFC":
                b = new HDFC();
                break;
            default:
                System.out.println("Invalid bank name.");
                scanner.close();
                return;
        }

        System.out.println(bankName + " Rate: " + b.getInterestRate() + "%");
        scanner.close();
    }
}
```






## OUTPUT:
<img width="428" height="203" alt="image" src="https://github.com/user-attachments/assets/d9bef525-2aeb-4aaf-bc1c-5ccaf540bd1f" />



## RESULT:
The program successfully demonstrated method overriding. The subclasses SBI, ICICI, and HDFC overrode the getInterestRate() method of the Bank class and returned different interest rates.
