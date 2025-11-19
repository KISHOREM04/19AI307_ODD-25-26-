# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
Assign exam room based on:

Gender and subject code

Male taking subject 1 or 2 → print("A")

Female taking subject 1 → print("B")

Female taking subject 2 → print("C")

All others → print("Admin")

Except above any input should print ("Invalid")
Write a java program that gets input from user for gender and subject, allot room based above conditions.

## AIM:
To write a Java program that reads gender and subject code from the user and assigns an exam room based on the given conditions, printing "Invalid" for incorrect inputs.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util` for reading user input.
3. Create a Scanner object to accept user input.
4. Read gender input from the user (e.g., "Male" or "Female").
5. Read subject code from the user (integer such as 1 or 2).
6. Convert gender input to a standard form (like uppercase or lowercase) for comparison.
7. Check the conditions:

   * If gender is male and subject is 1 or 2 → assign room **A**.
   * If gender is female and subject is 1 → assign room **B**.
   * If gender is female and subject is 2 → assign room **C**.
   * If gender or subject does not match these rules but inputs are otherwise valid → assign **Admin**.
   * Any invalid or unexpected input → print **Invalid**.
8. Display the assigned room.
9. End the program.
## PROGRAM:
 ```
/*
Program to implement a Conditional Statements using Java
Developed by: KISHORE M
RegisterNumber:212222040079
*/
```

## Sourcecode.java:
```java
import java.util.*;

public class HauntedHouse
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        
        int hour = sc.nextInt();

        if (hour % 2 == 0 && hour >= 2 && hour <= 6) 
        {
            System.out.println("Lights flicker");
        } 
        else if (hour % 2 != 0 && hour >= 7 && hour <= 11)
        {
            System.out.println("Lights off");
        } 
        else if (hour == 12) 
        {
            System.out.println("Lights red");
        } 
        else
        {
            System.out.println("Dark house");
        }
    }
}

```

## OUTPUT:
<img width="258" height="176" alt="image" src="https://github.com/user-attachments/assets/dd8f11c4-272b-4e1a-93a3-f76f388b9dc5" />






## RESULT:
The program successfully reads the gender and subject code from the user and assigns the correct exam room according to the given rules. If the user inputs invalid values, the program displays "Invalid".



