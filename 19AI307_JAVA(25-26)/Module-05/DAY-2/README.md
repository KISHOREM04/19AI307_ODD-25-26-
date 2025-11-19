# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to simulate inter-thread communication using PipedInputStream and PipedOutputStream, where one thread writes data (input taken from the user) and another thread reads and displays the data.

## AIM:
To simulate inter-thread communication in Java using PipedInputStream and PipedOutputStream, where one thread writes user input into a pipe and another thread reads and displays the data.

## ALGORITHM :
1. **Start the program.**
2. Import the required packages: `java.io` and `java.util`.
3. Create a **PipedOutputStream** object for writing data.
4. Create a **PipedInputStream** object and connect it to the PipedOutputStream.
5. Create a **WriterThread** class that:

   * Takes user input
   * Writes the data into the PipedOutputStream
6. Create a **ReaderThread** class that:

   * Continuously reads data from the PipedInputStream
   * Displays the received data
7. In the main method:

   * Create objects for both WriterThread and ReaderThread
   * Start both threads
8. Ensure proper exception handling for IO operations.
9. Close the streams after the operation if required.
10. **End the program.**

## PROGRAM:
 ```
/*
Program to implement a Serialization and Deserialization using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.io.*;
import java.util.Scanner;

class WriterThread extends Thread {
    private PipedOutputStream pos;
    private String message;

    public WriterThread(PipedOutputStream pos, String message) {
        this.pos = pos;
        this.message = message;
    }

    @Override
    public void run() {
        try {
            pos.write(message.getBytes());
            pos.close();
        } catch (IOException e) {
            System.out.println("WriterThread Error: " + e.getMessage());
        }
    }
}

class ReaderThread extends Thread {
    private PipedInputStream pis;

    public ReaderThread(PipedInputStream pis) {
        this.pis = pis;
    }

    @Override
    public void run() {
        try {
            byte[] buffer = new byte[1024];
            int len = pis.read(buffer);
            String received = new String(buffer, 0, len);
            System.out.println("ReaderThread received: " + received);
            pis.close();
        } catch (IOException e) {
            System.out.println("ReaderThread Error: " + e.getMessage());
        }
    }
}

public class PipedStreamUserInputDemo {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        try {
            String userMessage = scanner.nextLine();

            PipedOutputStream pos = new PipedOutputStream();
            PipedInputStream pis = new PipedInputStream(pos);

            WriterThread writer = new WriterThread(pos, userMessage);
            ReaderThread reader = new ReaderThread(pis);

            reader.start();
            writer.start();

        } catch (IOException e) {
            System.out.println("Main Error: " + e.getMessage());
        } finally {
            scanner.close();
        }
    }
}
```







## OUTPUT:
<img width="1276" height="166" alt="image" src="https://github.com/user-attachments/assets/1a199d3f-0907-4222-b024-1a8288d5ef91" />



## RESULT:
The program successfully demonstrates inter-thread communication.
One thread writes user-provided data into a pipe, and another thread reads and prints that data, showing how threads can exchange information using PipedInputStream and PipedOutputStream.
