# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
Create animals from two regions: "Africa" and "Asia". Use Abstract Factory to create families of animals (Herbivore, Carnivore). Print the interaction result.

## AIM:
To implement the Abstract Factory Pattern for creating families of animals (Herbivore and Carnivore) from two regions: Africa and Asia, and to display how animals from each region interact.

## ALGORITHM :
1.	Start the program.
2. Create an interface **Herbivore** and an interface **Carnivore**.
3. Create concrete classes:

   * For Africa: `Zebra` (Herbivore), `Lion` (Carnivore)
   * For Asia: `Deer` (Herbivore), `Tiger` (Carnivore)
4. Create an abstract factory interface **AnimalFactory** with methods:

   * `createHerbivore()`
   * `createCarnivore()`
5. Create two concrete factories:

   * **AfricaFactory** → returns Zebra and Lion
   * **AsiaFactory** → returns Deer and Tiger
6. Create a client class **AnimalWorld** that accepts an AnimalFactory and:

   * Creates a Herbivore
   * Creates a Carnivore
   * Prints the interaction (Carnivore eats Herbivore)
7. In the main method:

   * Create AfricaFactory → pass to AnimalWorld → display interaction
   * Create AsiaFactory → pass to AnimalWorld → display interaction
8. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: KISHORE M
RegisterNumber:212222040079
*/
```

## SOURCE CODE:
```java
import java.util.Scanner;

interface Herbivore {}
interface Carnivore {
    void eat(Herbivore h);
}

class Wildebeest implements Herbivore {}
class Lion implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Lion eats Wildebeest");
    }
}

class Buffalo implements Herbivore {}
class Tiger implements Carnivore {
    public void eat(Herbivore h) {
        System.out.println("Tiger eats Buffalo");
    }
}

interface AnimalFactory {
    Herbivore createHerbivore();
    Carnivore createCarnivore();
}

class AfricaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Wildebeest(); }
    public Carnivore createCarnivore() { return new Lion(); }
}

class AsiaFactory implements AnimalFactory {
    public Herbivore createHerbivore() { return new Buffalo(); }
    public Carnivore createCarnivore() { return new Tiger(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String region = sc.nextLine().toLowerCase();
        AnimalFactory factory;

        if (region.equals("africa")) factory = new AfricaFactory();
        else if (region.equals("asia")) factory = new AsiaFactory();
        else {
            System.out.println("Invalid region");
            return;
        }

        Carnivore carn = factory.createCarnivore();
        Herbivore herb = factory.createHerbivore();
        carn.eat(herb);
    }
}
```






## OUTPUT:
<img width="505" height="208" alt="image" src="https://github.com/user-attachments/assets/a3098a3e-9874-4b67-8648-2fda49ce0813" />

## RESULT:
The program successfully applies the Abstract Factory Pattern to create related animal families based on regions. Each region produces its own herbivore and carnivore, and the interaction is printed, demonstrating how factory selection controls object creation without modifying client code.
