# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called BankAccount with private instance variables accountNumber and balance. Provide public getter and setter methods to access and modify these variables.

## AIM:
To write a Java program that creates a class BankAccount with private instance variables and provides public getter and setter methods to access and modify them.

## ALGORITHM :
1. Start the program.
2. Create a class **BankAccount**.
3. Declare two private instance variables:

   * `accountNumber`
   * `balance`
4. Create public **setter methods** to set the values of accountNumber and balance.
5. Create public **getter methods** to retrieve the values of accountNumber and balance.
6. In the main method, create an object of **BankAccount**.
7. Use setter methods to store values and getter methods to access them.
8. Display the account number and balance.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class BankAccount 
{
    private String accountNumber;
    private double balance;

    public String getAccountNumber() 
    {
        return accountNumber;
    }
    public void setAccountNumber(String accountNumber) 
    {
        this.accountNumber = accountNumber;
    }

    public double getBalance() 
    {
        return balance;
    }
    public void setBalance(double balance) 
    {
        this.balance = balance;
    }

    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        BankAccount account = new BankAccount();
        account.setAccountNumber(sc.nextLine());
        account.setBalance(sc.nextDouble());
        System.out.println("Account Number: " + account.getAccountNumber());
        System.out.println("Balance: " + account.getBalance());
    }
}
```






## OUTPUT:
<img width="663" height="300" alt="image" src="https://github.com/user-attachments/assets/9cac65b6-d5f6-4207-be81-66b0255a552d" />



## RESULT:
The program successfully created a BankAccount class with private variables and accessed them using public getter and setter methods.
