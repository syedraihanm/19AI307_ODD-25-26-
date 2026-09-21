# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to print all elements in an array that are greater than a given value


## AIM:
To write a Java program that prints all elements in an array greater than a given value.

## ALGORITHM :
1. Start the program and create a Scanner object.
2. Read the size n and elements of the array.
3. Read a value to compare with.
4. Use a loop to check and print elements greater than the given value.
5. End the program.




## PROGRAM:

### Program to Implement Variables and Operators Using Java

**Developed by:** Syed Mohamed Raihan M 
**Register Number:** 212224240167
### SOURCE CODE:
```java
import java.util.Scanner;

public class GreaterThanValue {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int[] arr = {10, 25, 5, 40, 15, 30};

        System.out.print("Enter the value: ");
        int value = sc.nextInt();

        System.out.println("Elements greater than " + value + ":");

        for (int i = 0; i < arr.length; i++) {
            if (arr[i] > value) {
                System.out.println(arr[i]);
            }
        }

        sc.close();
    }
}

Example output:

Enter the value: 20
Elements greater than 20:
25
40
30
```

