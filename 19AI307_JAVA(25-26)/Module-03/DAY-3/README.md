# Ex.No:3(C) ABSTRACTION

## QUESTION:
A group of researchers receives mysterious numerical sequences believed to be sent by intelligent alien life. To decode them, scientists have built intelligent SignalAgents that follow abstract processing rules. Each agent listens to the numbers differently.

Your task is to create a system where a base abstract class SignalAgent declares:

## AIM:
To write a Java program that demonstrates the use of abstract classes and method overriding by creating a base abstract class SignalAgent and derived classes PrimeAgent and MirrorAgent that decode alien signals differently.

## ALGORITHM :
1. Start the program.
2. Read the number of elements `n`.
3. Read the signal array of `n` integers.
4. Read the agent type (1 or 2).
5. If type = 1, create a `PrimeAgent` object.
6. If type = 2, create a `MirrorAgent` object.
7. Call the `decodeSignal()` method and display the result.
8. End the program.





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.*;

abstract class SignalAgent 
{
    abstract int decodeSignal(int[] signal);
}

class PrimeAgent extends SignalAgent 
{
    private boolean isPrime(int n) 
    {
        if (n < 2) return false;
        for (int i = 2; i * i <= n; i++) 
        {
            if (n % i == 0) return false;
        }
        return true;
    }

    @Override
    int decodeSignal(int[] signal) 
    {
        int sum = 0;
        for (int num : signal) 
        {
            if (isPrime(num)) sum += num;
        }
        return sum;
    }
}

class MirrorAgent extends SignalAgent 
{
    @Override
    int decodeSignal(int[] signal) 
    {
        int left = 0, right = signal.length - 1;
        while (left < right) 
        {
            if (signal[left] != signal[right]) return -1; 
            left++;
            right--;
        }
        return 1; 
    }
}

public class Main 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();
        int[] signal = new int[n];
        for (int i = 0; i < n; i++) signal[i] = sc.nextInt();

        int type = sc.nextInt();
        SignalAgent agent;

        if (type == 1) 
        {
            agent = new PrimeAgent();
            System.out.println(agent.decodeSignal(signal));
        } 
        else 
        {
            agent = new MirrorAgent();
            int result = agent.decodeSignal(signal);
            System.out.println(result == 1 ? "BALANCED" : "BROKEN");
        }
    }
}
```






## OUTPUT:
<img width="351" height="252" alt="image" src="https://github.com/user-attachments/assets/f7017f67-5bbe-47b6-bb40-d5dbc28a7e77" />



## RESULT:
The program successfully demonstrated method overriding using an abstract class.

