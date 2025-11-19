# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Read a file and print only the lines containing the word "Java".

## AIM:
To read a text file and print only the lines that contain the word "Java".

## ALGORITHM :
1. Start the program.
2. Import the necessary package `java.io` for file operations.
3. Create a `FileReader` object to read the file.
4. Wrap it inside a `BufferedReader` to read the file line by line.
5. Read each line in a loop using `readLine()`.
6. For each line, check whether it contains the word **"Java"** using `line.contains("Java")`.
7. If the condition is true, print that line.
8. Continue until the end of the file is reached.
9. Close all file streams.
10. End the program.




## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.*;

public class PrintJavaLines {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        List<String> list = new ArrayList<>();

        while (true) {
            String line = sc.nextLine();
            if (line.equals("exit"))
                break;
            list.add(line);
        }

        System.out.println("Lines containing the word 'Java':");
        for (String s : list) {
            if (s.contains("Java")) {
                System.out.println(s);
            }
        }

        sc.close();
    }
}
```







## OUTPUT:
<img width="789" height="249" alt="image" src="https://github.com/user-attachments/assets/7b97aa33-e780-4353-bcbe-6f5ea05f4272" />



## RESULT:
The program successfully reads the file and displays only those lines that contain the word "Java", filtering out all other lines.
