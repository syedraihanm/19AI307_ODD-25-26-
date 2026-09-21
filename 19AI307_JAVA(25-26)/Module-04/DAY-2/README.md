# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
A smart city has a grid of sensors installed across various zones to monitor Air Quality (AQI).

## AIM:
To operationalize SOLID design principles in a Java-based smart city AQI monitoring system by decoupling responsibilities, enabling scalable alert controllers, and ensuring clean observer-based data processing.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define the Observer interface to enforce a single responsibility for AQI evaluation.
4.	Implement GreenZoneController, AlertZoneController, and DangerZoneController as independent observers aligned with the Open/Closed Principle.
5.	Build the SensorNetwork class to register observers and broadcast AQI data according to the Liskov and Dependency Inversion principles.
6.	Read the number of sensor inputs from the user and iterate through each AQI record.
7.	Dispatch data to all registered observers for zone-specific actions.
8.	Terminate the program.

## PROGRAM:
 ```
/*
Program to implement a SOLID Principles in Java Program
Developed by: Syed Mohamed Raihan M
RegisterNumber: 212224240167
*/
```

## SOURCE CODE:

```java
import java.util.*;

interface Observer {
    void check(int aqi, String sensorId);
}

class GreenZoneController implements Observer {
    public void check(int aqi, String sensorId) {
        if (aqi < 100) {
            System.out.println("[GreenZoneController]: AQI is good at Sensor " + sensorId + ". No action needed.");
        }
    }
}

class AlertZoneController implements Observer {
    public void check(int aqi, String sensorId) {
        if (aqi >= 100 && aqi <= 200) {
            System.out.println("[AlertZoneController]: Moderate AQI at Sensor " + sensorId + ". Send public health alert.");
        }
    }
}

class DangerZoneController implements Observer {
    public void check(int aqi, String sensorId) {
        if (aqi > 200) {
            System.out.println("[DangerZoneController]: Critical AQI at Sensor " + sensorId + "! Trigger lockdown protocol.");
        }
    }
}

class SensorNetwork {
    private Observer[] observers = new Observer[3];
    private int count = 0;

    public void register(Observer o) {
        observers[count++] = o;
    }

    public void receiveData(String sensorId, int aqi) {
        System.out.println("Sensor " + sensorId + " reports AQI: " + aqi);
        for (int i = 0; i < count; i++) {
            observers[i].check(aqi, sensorId);
        }
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        SensorNetwork network = new SensorNetwork();

        network.register(new GreenZoneController());
        network.register(new AlertZoneController());
        network.register(new DangerZoneController());

        int n = sc.nextInt(); 
        sc.nextLine();
        for (int i = 0; i < n; i++) {
            String[] parts = sc.nextLine().split(" ");
            String id = parts[0];
            int aqi = Integer.parseInt(parts[1]);
            network.receiveData(id, aqi);
        }
    }
}
```

## OUTPUT:

<img width="1293" height="221" alt="image" src="https://github.com/user-attachments/assets/ad77b3cf-286f-4410-8161-e46ba3df5399" />

## RESULT:

Thus the output is executed successfully.
