# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Write a class Circle that takes radius as input and calculates area and circumference. Use math.pi for π.

## AIM:
To create a Java class that accepts a circle’s radius and computes its area and circumference using Math.PI.

## ALGORITHM :

1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the radius value from the user.
4.	Store the radius in a class constructor.
5.	Compute the area using Math.PI * radius * radius.
6.	Compute the circumference using 2 * Math.PI * radius.
7.	Display the area and circumference.
8.	Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: JOHN PAUL J
RegisterNumber: 212223230093
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

class prog {
    double radius;

    prog(double radius) {
        this.radius = radius;
    }

    double getArea() {
        double result = Math.PI * Math.pow(radius,2);
        return result;
    }

    double getCircumference() {
        double result = 2 * Math.PI * radius;
        return result;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        double radius = scanner.nextDouble();
        prog obj = new prog(radius);
        System.out.println(obj.getArea());
        System.out.println(obj.getCircumference());
    }
}
```

## OUTPUT:

<img width="467" height="250" alt="image" src="https://github.com/user-attachments/assets/3f8bee95-10ab-4cad-8f38-31310eb4acb6" />

## RESULT:
Thus the output is executed successfully.
