# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
You are developing a YouTube-like platform. Each channel can have multiple subscribers (viewers).

Whenever the channel uploads a new video, it must instantly notify all of its subscribers.

Each subscriber prints their own message like:

"[SubscriberName]: New video from [ChannelName]! Watching now..."

## AIM:
To implement the Observer Design Pattern where a Channel (Subject) notifies all its Subscribers (Observers) whenever a new video is uploaded.

## ALGORITHM :
1. **Start**
2. Create an interface **Observer** with a method `update(String channelName, String videoTitle)`.
3. Create a class **Subscriber** that implements Observer and stores the subscriber’s name.
4. In the `update()` method, display the message:
   *"[SubscriberName]: New video from [ChannelName]! Watching now..."*
5. Create an interface **Subject** with methods:

   * `subscribe(Observer o)`
   * `unsubscribe(Observer o)`
   * `notifySubscribers(String videoTitle)`
6. Create the class **Channel** that implements Subject and stores:

   * Channel name
   * List of subscribers
7. In `notifySubscribers()`, print:
   *"[ChannelName] uploaded: [VideoTitle]"*
   Then call the `update()` method of every subscriber.
8. Read input:

   * Channel name
   * Number of subscribers
   * Subscriber names
   * Number of videos
   * Video titles
9. For each video title, call `notifySubscribers(videoTitle)`.
10. **End**





## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: 
RegisterNumber:  
*/
```

## SOURCE CODE:
```java
import java.util.*;

interface Observer {
    void notify(String channelName, String videoTitle);
}

class Subscriber implements Observer {
    private String name;

    Subscriber(String name) {
        this.name = name;
    }

    @Override
    public void notify(String channelName, String videoTitle) {
        System.out.println(name + ": New video from " + channelName + "! Watch now...");
    }
}

class Channel {
    private String channelName;
    private List<Observer> subscribers;

    Channel(String channelName) {
        this.channelName = channelName;
        subscribers = new ArrayList<>();
    }

    void subscribe(Observer o) {
        subscribers.add(o);
    }

    void uploadVideo(String videoTitle) {
        System.out.println(channelName + " uploaded: " + videoTitle);
        notifyAllSubscribers(videoTitle);
    }

    private void notifyAllSubscribers(String videoTitle) {
        for (Observer ob : subscribers) {
            ob.notify(channelName, videoTitle);
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String channelName = sc.nextLine();

        Channel channel = new Channel(channelName);

        int n = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < n; i++) {
            String sub = sc.nextLine();
            channel.subscribe(new Subscriber(sub));
        }

        int v = sc.nextInt(); sc.nextLine();
        for (int i = 0; i < v; i++) {
            String title = sc.nextLine();
            channel.uploadVideo(title);
        }
        sc.close();
    }
}
```







## OUTPUT:
<img width="1299" height="248" alt="image" src="https://github.com/user-attachments/assets/811349d6-a488-4d97-8779-dd17bc425dc2" />



## RESULT:
The program successfully implements the Observer Pattern.
Each time the channel uploads a new video, all registered subscribers automatically receive a notification and display a personalized message acknowledging the upload.
