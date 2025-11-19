# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)

For PremiumCustomer, additionally show cashback amount (which is 1% of the final price).

## AIM:
To write a Java program that demonstrates inheritance by creating a base class Customer and subclasses RegularCustomer and PremiumCustomer, each applying different discount rates and cashback rules to calculate the final price of gold purchased.

## ALGORITHM :
1. Start the program.
2. Create a base class **Customer** with the attributes:

   * customerId
   * name
   * purchaseWeight
   * goldRatePerGram
3. Define methods:

   * `getDiscountRate()` → returns 0 for base customer.
   * `calculateFinalPrice()` → computes discounted price.
   * `display()` → prints customer details.
4. Create subclass **RegularCustomer**:

   * Override `getDiscountRate()` to return **2%**.
   * Override `display()` to show type as RegularCustomer.
5. Create subclass **PremiumCustomer**:

   * Override `getDiscountRate()` to return **5%**.
   * Add method to calculate cashback (**1% of final price**).
   * Override `display()` to also print cashback amount.
6. In `main()`:

   * Read gold rate from user.
   * Create objects of RegularCustomer and PremiumCustomer.
   * Display their final prices.
7. End the program.





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: KISHORE M
RegisterNumber: 212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;
import java.text.DecimalFormat;

class Customer 
{
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) 
    {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() 
    {
        return 0;
    }

    double calculateFinalPrice() 
    {
        double discountAmount = goldRatePerGram * getDiscountRate() / 100;
        double effectiveRate = goldRatePerGram - discountAmount;
        return purchaseWeight * effectiveRate;
    }

    void display() 
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer 
{
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() 
    {
        return 2;
    }

    @Override
    void display() 
    {
        DecimalFormat df = new DecimalFormat("0.00");
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer 
{
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    @Override
    double getDiscountRate() 
    {
        return 5;
    }

    @Override
    void display() 
    {
        DecimalFormat df = new DecimalFormat("0.00");
        double finalPrice = calculateFinalPrice();
        double cashback = finalPrice * 0.01;

        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + purchaseWeight + " grams");
        System.out.println("Gold Rate per Gram: " + goldRatePerGram);
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + df.format(finalPrice));
        System.out.println("Cashback: " + df.format(cashback));
    }
}

public class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        String type = sc.nextLine().trim();   
        String id = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double weight = sc.nextDouble();
        double rate = sc.nextDouble();

        Customer customer;

        if (type.equalsIgnoreCase("Regular")) 
        {
            customer = new RegularCustomer(id, name, weight, rate);
        } 
        else 
        {
            customer = new PremiumCustomer(id, name, weight, rate);
        }

        customer.display();
    }
}

```






## OUTPUT:
<img width="682" height="572" alt="image" src="https://github.com/user-attachments/assets/f2eff4fe-6156-4552-a11b-83826c9b4ad8" />



## RESULT:
The program successfully demonstrated inheritance with a base Customer class and derived classes RegularCustomer and PremiumCustomer.
