# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Write a Java program that prompts the user to enter a non-negative integer and then calculates and displays the factorial of the given number.
Use a for loop to perform the calculation.
Make sure to handle the case when the user enters 0.
Display the result in a clear and user-friendly way.

## AIM:
To write a Java program to calculate the factorial of a non-negative integer using a for loop.

## ALGORITHM :
```
1. Start the program.
2. Read a non-negative integer from the user.
3. Initialize a variable factorial as 1.
4. Use a for loop from 1 to the given number.
5. Multiply factorial with each number in the loop.
6. If the number is 0, factorial remains 1.
7. Display the factorial value.
8. End the program.
```
## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
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

        int n = sc.nextInt();
        long factorial = 1;

        for(int i = 1; i <= n; i++)
        {
            factorial = factorial * i;
        }

        System.out.println("Factorial of " + n + " is " + factorial);
    }
}
```

## OUTPUT:
<img width="1295" height="355" alt="image" src="https://github.com/user-attachments/assets/cc3a5477-35f3-4c45-8f48-090911b1fb8a" />

## RESULT:
The Java program was executed successfully and the factorial of the given number was calculated and displayed successfully.
