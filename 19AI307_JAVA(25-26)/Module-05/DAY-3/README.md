# Ex.No:5(C)  FILE HANDLING USING JAVA
## QUESTION:
Write a program to count the number of characters in a file.

## AIM:
To develop a Java program that writes user input into a file and counts the total number of characters stored in that file using basic file handling operations.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read input from the user and write it into a file.
4.	Read the file character-by-character using FileReader.
5.	Increment a counter for each character read.
6.	Display the final character count.
7.	End the program.

## PROGRAM:
 ```
/*
Program to implement a File Handling using Java
Developed by: Syed Mohamed Raihan M
RegisterNumber: 212224240167
*/
```

## SOURCE CODE:

```java
import java.io.*;
import java.util.Scanner;

public class CharacterCountInFile {
    public static void main(String[] args) {
        String fileName = "charcount.txt";
        Scanner scanner = new Scanner(System.in);

        try {
            String input = scanner.nextLine();

            FileWriter writer = new FileWriter(fileName);
            writer.write(input);
            writer.close();

            FileReader reader = new FileReader(fileName);
            int count = 0;
            while (reader.read() != -1) {
                count++;
            }
            reader.close();
            System.out.println("Number of characters written to the file: " + count);

        } catch (IOException e) {
            System.out.println("Error: " + e.getMessage());
        } finally {
            scanner.close();
        }
    }
}
```

## OUTPUT:

<img width="890" height="201" alt="image" src="https://github.com/user-attachments/assets/edb8b580-9d6d-4835-94c4-48484343830d" />

## RESULT:

Thus the output is executed successfully.
