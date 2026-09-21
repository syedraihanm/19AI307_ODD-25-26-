# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
To implement exception handling in Java by safely performing division and managing division-by-zero errors using try–catch blocks.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read two integers from the user.
4.	Use a try block to perform division.
5.	Catch any division-by-zero exceptions using a catch block.
6.	Display the appropriate output or error message.
7.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: Syed Mohamed Raihan M
RegisterNumber: 212224240167
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

public class Main{
    
    public static void main(String[] args) {
        
        Scanner scan = new Scanner(System.in);
        
        int a,b;
        
        try{
            a = scan.nextInt();
            b = scan.nextInt();
            System.out.println("Result: "+a/b);
        }
        
        catch(Exception e){
            System.out.println("Error: Division by zero");
        }
        
    }
}
```

## OUTPUT:

<img width="553" height="253" alt="image" src="https://github.com/user-attachments/assets/b1e003cc-90fd-4740-b72c-ade72a0b4e14" />

## RESULT:

Thus the output is executed successfully.
