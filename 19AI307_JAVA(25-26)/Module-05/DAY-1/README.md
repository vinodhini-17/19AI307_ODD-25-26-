# Ex.No:5(A) INPUTSTREAMREADER 

## QUESTION:
Write a Java program to write characters to a file using FileWriter.

## AIM:
To write a Java program to write characters to a file using FileWriter.

## ALGORITHM :
1. Start the program.
2. Import the FileWriter class.
3. Create a FileWriter object with a file name.
4. Write characters into the file using the write() method.
5. Close the file using the close() method.
6. Display a success message.
7. End the program.
   
## PROGRAM:
 ```
/*
Program to implement file handling using FileWriter in Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.io.FileWriter;
import java.io.IOException;
import java.util.Scanner;

public class WriteFileUsingFileWriter 
{
    public static void main(String[] args) 
    {
        Scanner s=new Scanner(System.in);
        String a=s.nextLine();
        String b=s.nextLine();
        try{
            FileWriter fw=new FileWriter(a);
            fw.write(b);
            System.out.println("File written successfully.");
            fw.close();
        }
        catch(IOException e)
        {
            System.out.println("Error Occured");
        }
    }
}
```

## OUTPUT:
<img width="1295" height="416" alt="image" src="https://github.com/user-attachments/assets/02d0ae3e-0c0e-47a1-b951-b0f16c959c27" />

## RESULT:
The Java program was executed successfully and the characters were written to the file successfully using FileWriter.
