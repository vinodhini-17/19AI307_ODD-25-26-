# Ex.No:4(A) EXCEPTION HANDLING

## QUESTION:
Write a program that reads two integers and divides the first by the second. Handle the case when division by zero occurs.

## AIM:
To write a Java program to divide two integers and handle division by zero using exception handling.

## ALGORITHM :
1. Start the program.
2. Read two integers from the user.
3. Use a try block to divide the first number by the second number.
4. Display the division result if successful.
5. Use a catch block to handle ArithmeticException.
6. Display an error message if division by zero occurs.
7. End the program.

## PROGRAM:
 ```
/*
Program to implement a Exception Handling using Java
Developed by: VINODHINI K
RegisterNumber:  212223230245
*/
```

## SOURCE CODE:
```
import java.util.*;
public class main
{
    public static void main(String[] args)
    {
        Scanner s=new Scanner(System.in);
        try
        {
            int a=s.nextInt();
            int b=s.nextInt();
            System.out.println("Result: "+a/b);
        }
        catch(Exception e)
        {
            System.out.println("Error: Division by zero");
        }
    }
}
```

## OUTPUT:
<img width="1293" height="416" alt="image" src="https://github.com/user-attachments/assets/820cd509-00b6-4d94-adbd-fd0233aa1fab" />

## RESULT:
The Java program was executed successfully and the division result was displayed with proper handling of division by zero exception.
