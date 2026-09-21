# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.


## AIM:
To demonstrate accessing a static variable in Java using both the class name and an object.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Declare a class containing a static variable.
4. Access the static variable directly using the class name.
5.	Create an object of the class.
6.	Access the same static variable using the object.
7.	Display both outputs.
8.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: JOHN PAUL J
RegisterNumber: 212223230093
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

class Sample {
    static int number;

    Sample(int number) {
        Sample.number = number;
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        int input = scan.nextInt();
        Sample obj = new Sample(input);
        System.out.println("Accessing using class name: " + Sample.number);
        System.out.println("Accessing using object: " + obj.number);
