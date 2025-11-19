# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Create an Article class where changes to the content are saved as mementos. Let the user view and restore any saved version.

## AIM:
To implement the Memento Design Pattern by creating an Article class whose content changes are saved as mementos. The user should be able to view all saved versions and restore any previously saved version

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3. Create the **Article** (Originator) class with:

   * A variable `content`
   * A method `setContent(String c)` to update content
   * A method `save()` that returns a new Memento containing the current content
   * A method `restore(Memento m)` to set the content back to a stored state
4. Create a **Caretaker** class to maintain a list of saved mementos.

   * Provide methods to add mementos and retrieve them by index
5. In the main method:

   * Create an Article object
   * Read new versions of content from the user
   * Each time content changes, save a memento and store it in the caretaker
   * Allow the user to view all saved version numbers
   * Allow the user to select a version to restore
6. Restore the selected memento and display the restored content.
7. Stop the program.


## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: KISHORE M
RegisterNumber: 212222040079
*/
```

## SOURCE CODE:
```java
import java.util.*;

class Article {
    private String content;

    public void setContent(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }

    public ArticleMemento save() {
        return new ArticleMemento(content);
    }

    public void restore(ArticleMemento memento) {
        this.content = memento.getContent();
    }
}

class ArticleMemento {
    private final String content;

    public ArticleMemento(String content) {
        this.content = content;
    }

    public String getContent() {
        return content;
    }
}

class ArticleHistory {
    private List<ArticleMemento> versions = new ArrayList<>();

    public void saveVersion(Article article) {
        versions.add(article.save());
    }

    public ArticleMemento getVersion(int index) {
        if (index >= 0 && index < versions.size()) {
            return versions.get(index);
        }
        return null;
    }
}

public class ArticleManager {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Article article = new Article();
        ArticleHistory history = new ArticleHistory();

        int n = Integer.parseInt(sc.nextLine());
        for (int i = 0; i < n; i++) {
            String content = sc.nextLine();
            article.setContent(content);
            history.saveVersion(article);
        }

        int restoreIndex = Integer.parseInt(sc.nextLine());
        ArticleMemento m = history.getVersion(restoreIndex);
        if (m != null) {
            article.restore(m);
            System.out.println(article.getContent());
        } else {
            System.out.println("Invalid version");
        }

        sc.close();
    }
}
```






## OUTPUT:
<img width="631" height="429" alt="image" src="https://github.com/user-attachments/assets/ea78dc52-9736-45c3-a8c9-b6e98c974331" />

## RESULT:
The program successfully uses the Memento Pattern to save multiple versions of an article. Users can view previously saved states and restore any version, demonstrating controlled rollback of object state without violating encapsulation.
