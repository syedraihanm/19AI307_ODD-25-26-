# Ex.No:5(D) THREAD PRIORITY

## QUESTION:
Write a java program for set the priority and name of the current thread.Consider two threads t1 and t2

## AIM:
To write a Java program that creates two threads, assigns names and priorities to them, and displays their details.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read thread names from the user.
4.	Create two thread objects.
5.	Set custom names for each thread.
6.	Assign different priorities to both threads.
7.	Display thread details.
8.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Thread Priority Concept using Java
Developed by: Syed Mohamed Raihan 
RegisterNumber: 212224240167
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        
        // Read two thread names from user
        String name1 = sc.nextLine();
        String name2 = sc.nextLine();
        
        // Create two threads
        Thread t1 = new Thread();
        Thread t2 = new Thread();
        
        // Set thread names
        t1.setName(name1);
        t2.setName(name2);
        
        // Set priorities
        t1.setPriority(4);
        t2.setPriority(2);
        
        // Print thread information exactly as requested
        System.out.println(t1);
        System.out.println(t2);
    }
}
```

## OUTPUT:

<img width="636" height="199" alt="image" src="https://github.com/user-attachments/assets/a2e2eb80-9d9c-406c-9626-30797e12a1a7" />

## RESULT:

Thus the output is executed successfully.
