# Ex.No:2(B) METHODS

## QUESTION:
Write a method int cube(int x) that calls a method int square(int x) internally to calculate the cube as x * square(x).

## AIM:
To write a Java program to calculate the cube of a number by calling a square() method inside the cube() method.

## ALGORITHM :
1. Start the program.
2. Create a method square(int x) to return the square of a number.
3. Create a method cube(int x) to return x multiplied by square(x).
4. Read a number from the user.
5. Call the cube() method.
6. Display the cube of the number.
7. End the program.

## PROGRAM:
 ```
/*
Program to implement methods using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class Main
{
    static int square(int x)
    {
        return x * x;
    }

    static int cube(int x)
    {
        return x * square(x);
    }

    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);

        int n = sc.nextInt();

        System.out.println("Cube of " + n + " is " + cube(n));
    }
}
```

## OUTPUT:
<img width="1294" height="265" alt="image" src="https://github.com/user-attachments/assets/432eb1f6-ea51-4191-93a5-fcf29b40efff" />

## RESULT:
The Java program was executed successfully and the cube of the given number was calculated using the square() method and displayed successfully.
