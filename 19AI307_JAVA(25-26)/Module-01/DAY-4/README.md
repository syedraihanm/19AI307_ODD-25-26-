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

**Developed by:** Syed Mohamed Raihan 

**Register Number:** 212224240167
### SOURCE CODE:
```java
import java.util.Scanner;

public class ElementsGreaterThanX {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int n = scanner.nextInt();     // size of array
        int[] arr = new int[n];

        for(int i = 0; i < n; i++) {
            arr[i] = scanner.nextInt();  // array elements
        }

        int x = scanner.nextInt();     // value to compare

        boolean found = false;

        for(int i = 0; i < n; i++) {
            if(arr[i] > x) {
                System.out.println(arr[i]);
                found = true;
            }
        }

        if(!found) {
            System.out.println("No elements greater than " + x);
        }
    }
}

```






## OUTPUT:
<img width="1141" height="823" alt="image" src="https://github.com/user-attachments/assets/34a186f8-3e64-4b59-a0c6-c0fd2da49e52" />



## RESULT:
The program successfully prints all array elements greater than the given value.




