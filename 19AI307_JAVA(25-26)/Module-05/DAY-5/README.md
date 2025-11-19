# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Print "Hello" and "World" alternately from two threads using synchronized blocks.

## AIM:
To create two threads that print “Hello” and “World” alternately using a shared synchronized block, ensuring proper thread coordination.

## ALGORITHM :
1. Start the program.
2. Create a shared object (lock) that both threads will synchronize on.
3. Create a boolean or toggle flag to control whose turn it is to print.
4. Create the first thread (Thread A) to print **“Hello”**.
5. Inside Thread A:

   * Use a synchronized block with the shared lock.
   * Check if it is the "Hello" turn.
   * If yes, print **“Hello”**.
   * Switch the turn to "World".
   * Notify the other thread.
   * If not its turn, make the thread wait.
6. Create the second thread (Thread B) to print **“World”**.
7. Inside Thread B:

   * Use a synchronized block with the shared lock.
   * Check if it is the "World" turn.
   * If yes, print **“World”**.
   * Switch the turn to "Hello".
   * Notify the other thread.
   * If not its turn, make the thread wait.
8. Start both threads.
9. Allow printing for a fixed number of iterations (optional).
10. End the program.





## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

class Printer {
    private boolean helloTurn = true;

    public void printHello() throws InterruptedException {
        synchronized (this) {
            while (!helloTurn)
                wait();
            System.out.println("Hello");
            helloTurn = false;
            notify();
        }
    }

    public void printWorld() throws InterruptedException {
        synchronized (this) {
            while (helloTurn)
                wait();
            System.out.println("World");
            helloTurn = true;
            notify();
        }
    }
}

public class AlternateHelloWorld {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        Printer printer = new Printer();

        Thread t1 = new Thread(() -> {
            try {
                for (int i = 0; i < n; i++)
                    printer.printHello();
            } catch (InterruptedException e) {}
        });

        Thread t2 = new Thread(() -> {
            try {
                for (int i = 0; i < n; i++)
                    printer.printWorld();
            } catch (InterruptedException e) {}
        });

        t1.start();
        t2.start();
    }
}
```







## OUTPUT:
<img width="278" height="501" alt="image" src="https://github.com/user-attachments/assets/c1178857-2b92-47b4-bf73-4c7205871cdc" />


## RESULT:
The program successfully prints **“Hello”** and **“World”** alternately using two threads.
Synchronization ensures that only one thread prints at a time, producing the correct alternating sequence.
