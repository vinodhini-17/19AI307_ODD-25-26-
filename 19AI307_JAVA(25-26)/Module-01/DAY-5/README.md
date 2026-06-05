# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To write a Java program to reverse a given string.

## ALGORITHM :
```
1. Start the program.
2. Read a string from the user.
3. Initialize an empty string for storing the reversed string.
4. Traverse the original string from the last character to the first character.
5. Append each character to the reversed string.
6. Display the reversed string.
7. End the program.
```
## PROGRAM:
 ```
/*
Program to implement string manipulation using Java
Developed by: ALIYA SHEEMA 
RegisterNumber: 212223230011
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);

        String str = sc.nextLine();
        String reverse = "";

        for(int i = str.length() - 1; i >= 0; i--)
        {
            reverse = reverse + str.charAt(i);
        }

        System.out.println("Reversed String: " + reverse);
    }
}
```

## OUTPUT:
<img width="1292" height="343" alt="image" src="https://github.com/user-attachments/assets/ad8c5dbb-303b-4f5e-8ae5-75cb67219534" />

## RESULT:
The Java program was executed successfully and the given string was reversed and displayed successfully.
