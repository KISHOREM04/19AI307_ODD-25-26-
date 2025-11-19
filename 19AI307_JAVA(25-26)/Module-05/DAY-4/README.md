# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for determine the priority and name of the current thread.

Note : Read the threadname from the User

## AIM:
To read a thread name from the user and set the name and priority of the current thread, then display the updated thread details.

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.util` for taking user input.
3. Create a Scanner object to read the thread name from the user.
4. Get the reference of the **current thread** using `Thread.currentThread()`.
5. Read the thread name entered by the user.
6. Set the thread name using `setName()`.
7. Set the thread priority (default or user-given as needed).
8. Retrieve the name and priority using `getName()` and `getPriority()`.
9. Display the thread name, thread priority, and complete thread information.
10. End the program.





## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

public class ThreadDetailsUserInput {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        String threadName = sc.nextLine();

        Thread current = Thread.currentThread();
        current.setName(threadName);

        System.out.println("Priority of Thread: " + current.getPriority());
        System.out.println("Name of Thread: " + current.getName());
        System.out.println(current);

        sc.close();
    }
}
```







## OUTPUT:
<img width="521" height="156" alt="image" src="https://github.com/user-attachments/assets/da35df4f-101d-46b0-b36e-19718638ef31" />



## RESULT:
The program successfully reads the thread name from the user, assigns it to the current thread, sets the priority, and displays the updated thread details including the thread name, priority, and full thread information.
