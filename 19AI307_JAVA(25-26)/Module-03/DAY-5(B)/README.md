# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Write a Java program to check if a number is an Armstrong number using Math.pow() and the Integer wrapper class. Take input from the user.

## AIM:
To write a Java program to check whether a number is an Armstrong number using Math.pow() and the Integer wrapper class.

## ALGORITHM :
1. Start the program.
2. Read a number from the user.
3. Convert the number to a string using the Integer wrapper class.
4. Find the number of digits.
5. Store the original number in a temporary variable.
6. Extract each digit using modulus and division operations.
7. Calculate the power of each digit using Math.pow().
8. Find the sum of all powered digits.
9. Compare the sum with the original number.
10. If both are equal, display that it is an Armstrong number.
11. Otherwise, display that it is not an Armstrong number.
12. End the program.

## PROGRAM:
 ```
/*
Program to implement Armstrong number checking using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
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

        Integer num = sc.nextInt();
        int original = num;
        int digits = String.valueOf(num).length();

        int sum = 0;
        while (num > 0) 
        {
            int rem = num % 10;
            sum += (int) Math.pow(rem, digits);
            num /= 10;
        }

        if (sum == original) 
        {
            System.out.println(original + " is an Armstrong number.");
        } 
        else 
        {
            System.out.println(original + " is not an Armstrong number.");
        }
    }
}
```

## OUTPUT:
<img width="1293" height="350" alt="image" src="https://github.com/user-attachments/assets/c6d5eff0-ad11-4641-a1c3-e292f2904985" />

## RESULT:
The Java program was executed successfully and the given number was checked and displayed whether it is an Armstrong number or not.
