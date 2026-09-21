# Ex.No:5(E) MULTITHREADING -SYNCHRONIZATION

## QUESTION:
Use ScheduledExecutorService to delay execution of tasks and print their message.

## AIM:
To implement delayed task execution using Java’s ScheduledExecutorService, allowing multiple tasks to run after specific time intervals.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read number of tasks from the user.
4.	For each task, read the message and delay time.
5.	Store tasks in a list.
6.	Use ScheduledExecutorService to schedule each task based on its delay.
7.	Print message when the delay completes.
8.	Shutdown the scheduler.
9.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Synchronization concept using Java
Developed by: Syed Mohamed Raihan M
RegisterNumber: 212224240167
*/
```

## SOURCE CODE:

```java
import java.util.*;
import java.util.concurrent.*;

class prog {
    static class Task {
        String message;
        int delay;
        int order; 
        Task(String message, int delay, int order) {
            this.message = message;
            this.delay = delay;
            this.order = order;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        List<Task> tasks = new ArrayList<>();

        for (int i = 0; i < n; i++) {
            String msg = sc.next();
            int delay = sc.nextInt();
            tasks.add(new Task(msg, delay, i));
        }

        ScheduledExecutorService scheduler = Executors.newScheduledThreadPool(1);

        tasks.sort(Comparator.comparingInt((Task t) -> t.delay).thenComparingInt(t -> t.order));

        for (Task t : tasks) {
            scheduler.schedule(() -> {
                System.out.println(t.message);
            }, t.delay, TimeUnit.SECONDS);
        }

        scheduler.shutdown();
    }
}
```

## OUTPUT:

<img width="303" height="460" alt="image" src="https://github.com/user-attachments/assets/9925f187-9f35-44bd-9621-08309c520d44" />


## RESULT:

Thus the output is executed successfully.
