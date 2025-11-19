# Ex.No:3(D)    INTERFACE 

## QUESTION:
You're building the equalizer system for a music app like BeatBoxx. The equalizer has 3 basic sound modes:

BassBoost
VocalBoost
Balanced
Each mode behaves differently and alters the sound experience. The app uses a SoundMode interface that each mode implements.

## AIM:
To write a Java program that demonstrates interfaces by creating a SoundMode interface and implementing it in classes BassBoost, VocalBoost, and Balanced. The program selects a mode based on user input and displays the corresponding message.

## ALGORITHM :
1. Start the program.
2. Create an interface **SoundMode** with a method `applyMode()`.
3. Create three classes implementing the interface:

   * **BassBoost** → prints bass message
   * **VocalBoost** → prints vocal message
   * **Balanced** → prints balanced mode message
4. Read user input (bass/vocal/balanced).
5. Based on the input:

   * Create the corresponding mode object
   * Call `applyMode()`
6. If the input does not match any valid mode, print `"Invalid mode selected."`
7. End the program.




## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: KISHORE M
RegisterNumber:  212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

interface SoundMode {
    void apply();
}

class BassBoost implements SoundMode {
    public void apply() {
        System.out.println("Bass Boost applied. Feel the beat drop!");
    }
}

class VocalBoost implements SoundMode {
    public void apply() {
        System.out.println("Vocal Boost enabled. Enjoy crystal-clear lyrics!");
    }
}

class Balanced implements SoundMode {
    public void apply() {
        System.out.println("Balanced mode set. A perfect blend of bass and vocals.");
    }
}

public class EqualizerApp {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String mode = sc.nextLine().trim().toLowerCase();
        SoundMode soundMode;

        switch(mode) {
            case "bass": soundMode = new BassBoost(); break;
            case "vocal": soundMode = new VocalBoost(); break;
            case "balanced": soundMode = new Balanced(); break;
            default:
                System.out.println("Invalid mode selected.");
                sc.close();
                return;
        }

        soundMode.apply();
    }
}
```







## OUTPUT:
<img width="985" height="204" alt="image" src="https://github.com/user-attachments/assets/d48eac41-0864-4fc0-b290-4f22e9116311" />



## RESULT:
The program successfully demonstrated interface implementation by applying the correct sound mode based on user input. Appropriate messages were displayed for BassBoost, VocalBoost, Balanced, and invalid mode selections.
