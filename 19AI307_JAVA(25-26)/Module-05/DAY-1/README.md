# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
To operationalize a Java workflow that captures user input at runtime and pipelines it into a text file using FileWriter and buffered I/O for optimized throughput.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Capture the target filename and content from the user.
4.	Initialize FileWriter wrapped in BufferedWriter.
5.	Write the user content into the file.
6.	Close the I/O stream and finalize execution.

## PROGRAM:
 ```
/*
Program to implement a InputStreamReader using Java
Developed by: Syed Mohamed Raihan M
RegisterNumber: 212224240167
*/
```

## SOURCE CODE:

```java
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;
import java.io.*;

public class WriteFileUsingFileWriter {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);
        try{
            BufferedWriter writer = new BufferedWriter(new FileWriter(scan.nextLine()));
            writer.write(scan.nextLine());
            writer.close();
            System.out.println("File written successfully.");
        }
        catch(Exception e){
            e.printStackTrace();
        }
        
    }
}
```

## OUTPUT:

<img width="595" height="254" alt="image" src="https://github.com/user-attachments/assets/cdbb4e18-0431-4bd1-8b2a-2429c82e7005" />

## RESULT:

Thus the output is executed successfully.
