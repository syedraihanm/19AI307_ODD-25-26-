# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:
To implement the Abstract Factory design pattern in Java by creating theme-specific factories (Dark and Light) that produce UI components such as Button and Checkbox based on user-selected themes.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Define interfaces Button and Checkbox with the render() method.
4.	Create concrete classes for Dark and Light variants of Button and Checkbox.
5.	Define a UIFactory interface with methods to create Button and Checkbox objects.
6.	Implement DarkThemeFactory and LightThemeFactory to generate theme-specific components.
7.	Read the theme choice from the user.
8.	Instantiate the appropriate factory and create UI components.
9.	Display the type of button and checkbox created.
10.	End the program.

## PROGRAM:
 ```
/*
Program to implement a Abstract Factory Pattern using Java
Developed by: Syed Mohamed Raihan M
RegisterNumber: 212224240167
*/
```

## SOURCE CODE:

```java
import java.util.Scanner;

interface Button { void render(); }
interface Checkbox { void render(); }

class DarkButton implements Button {
    public void render() { System.out.println("Dark Button created"); }
}
class LightButton implements Button {
    public void render() { System.out.println("Light Button created"); }
}
class DarkCheckbox implements Checkbox {
    public void render() { System.out.println("Dark Checkbox created"); }
}
class LightCheckbox implements Checkbox {
    public void render() { System.out.println("Light Checkbox created"); }
}

interface UIFactory {
    Button createButton();
    Checkbox createCheckbox();
}

class DarkThemeFactory implements UIFactory {
    public Button createButton() { return new DarkButton(); }
    public Checkbox createCheckbox() { return new DarkCheckbox(); }
}

class LightThemeFactory implements UIFactory {
    public Button createButton() { return new LightButton(); }
    public Checkbox createCheckbox() { return new LightCheckbox(); }
}

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String theme = scanner.nextLine().toLowerCase();
        UIFactory factory;
        if (theme.equals("dark")) factory = new DarkThemeFactory();
        else if (theme.equals("light")) factory = new LightThemeFactory();
        else {
            System.out.println("Invalid theme");
            return;
        }
        factory.createButton().render();
        factory.createCheckbox().render();
    }
}
```

## OUTPUT:

<img width="504" height="235" alt="image" src="https://github.com/user-attachments/assets/2577db6a-8795-4def-8eba-b242b58f4837" />

## RESULT:

Thus the output is executed successfully.
