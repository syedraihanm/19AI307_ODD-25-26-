# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Print Hollow Square Pattern

## AIM:
To write a Java program to print a hollow square pattern using asterisks (*).

## ALGORITHM :
1.Start the program and create a Scanner object.
2.Read an integer n representing the size of the square.
3.Use nested loops to iterate through rows (i) and columns (j).
4.Print * for boundary positions (first/last row or column), else print space.
5.End the program.




## PROGRAM:

### Program to Implement Variables and Operators Using Java

**Developed by:** JOHN PAUL J

**Register Number:** 212223230176

### SOURCE CODE:
```java
import java.util.Scanner;

public class HollowSquare {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        for (int i = 1; i <= n; i++) {
            for (int j = 1; j <= n; j++) {
                if (i == 1 || i == n || j == 1 || j == n) {
                    System.out.print("* ");
                } else {
                    System.out.print("  ");
                }
            }
            System.out.println();
        }

        sc.close();
    }
}
```

## OUTPUT:
<img width="1211" height="654" alt="image" src="https://github.com/user-attachments/assets/983aaead-17af-41d8-ba15-73b241800145" />



## RESULT:
The program successfully prints a hollow square pattern of size n × n.






