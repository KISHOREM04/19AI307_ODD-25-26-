# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a program to read user input from the keyboard using InputStreamReader 

## AIM:
To read user input from the keyboard using InputStreamReader and display the entered text.

## ALGORITHM :
1. **Start the program.**
2. **Import the necessary package `java.io`** for InputStreamReader and IOException.
3. Create an InputStreamReader object to read bytes from the keyboard and convert them into characters.
4. Wrap it with a BufferedReader to read a full line of text.
5. Display a message asking the user to enter some text.
6. Use the `readLine()` method to read the user’s input.
7. Store the input in a variable.
8. Print the entered text to confirm successful input reading.
9. Close the InputStreamReader/BufferedReader if needed.
10. **End the program.**.	





## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.io.*;

public class InputStreamReaderExample {
    public static void main(String[] args) {
        try {
            InputStreamReader isr = new InputStreamReader(System.in);
            BufferedReader br = new BufferedReader(isr);

            String name = br.readLine();
            System.out.println("Hello, " + name + "!");
        } catch (IOException e) {
            System.out.println("Error reading input.");
        }
    }
}
```






## OUTPUT:
<img width="379" height="167" alt="image" src="https://github.com/user-attachments/assets/fc8c3ff0-bf90-465b-9bcf-3ad8f0d4d4fd" />



## RESULT:
The program successfully reads keyboard input using InputStreamReader and displays the text entered by the user.
