# Ex.No:4(D) DESIGN PATTERN  ---- BEHAVIOUR PATTERN

## QUESTION:
Develop a weather monitoring system using the Observer Design Pattern. The WeatherStation acts as the subject and notifies multiple display units (MobileDisplay and LEDDisplay) whenever temperature changes. Implement the behavioural pattern so that all registered displays automatically update when the temperature is modified.

## AIM:
To implement the Observer Behavioural Design Pattern in Java by creating a WeatherStation (subject) that broadcasts updates to multiple observers whenever data changes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an Observer interface with an update() method.
4.	Create a Subject interface with register(), remove(), and notifyObservers().
5.	Implement WeatherStation class that maintains temperature and observer list.
6.	Implement MobileDisplay and LEDDisplay classes as observers.
7.	Read temperature input from the user.
8.	Update the WeatherStation and notify all observers.
9.	Display the updated messages from all observers.
10.	End the program.
11.	
## PROGRAM:
 ```
/*
Program to implement a Behaviour Pattern using Java
Developed by: Syed Mohamed Raihan M
RegisterNumber: 212223230093
*/
```

## SOURCE CODE:

```java
import java.util.*;

interface Observer {
    void update(int temperature);
}

interface Subject {
    void register(Observer o);
    void remove(Observer o);
    void notifyObservers();
}

class WeatherStation implements Subject {
    private int temperature;
    private List<Observer> observers = new ArrayList<>();

    public void setTemperature(int temp) {
        this.temperature = temp;
        notifyObservers();
    }

    public void register(Observer o) {
        observers.add(o);
    }

    public void remove(Observer o) {
        observers.remove(o);
    }

    public void notifyObservers() {
        for (Observer obs : observers) {
            obs.update(temperature);
        }
    }
}

class MobileDisplay implements Observer {
    public void update(int temperature) {
        System.out.println("Mobile Display: Temperature updated → " + temperature + "°C");
    }
}

class LEDDisplay implements Observer {
    public void update(int temperature) {
        System.out.println("LED Display: Temperature changed → " + temperature + "°C");
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        WeatherStation ws = new WeatherStation();
        ws.register(new MobileDisplay());
        ws.register(new LEDDisplay());

        int temp = sc.nextInt();
        ws.setTemperature(temp);
    }
}
```

## OUTPUT:

<img width="814" height="194" alt="image" src="https://github.com/user-attachments/assets/80c75c20-f6b6-4c69-a7d4-68909c28ccbe" />

## RESULT:

Thus the output is executed successfully.
