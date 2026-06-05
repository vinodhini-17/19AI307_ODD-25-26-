# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
In a magical building, an elevator behaves oddly:
If the floor number is divisible by 3 and 5, it says "Skipped".
If the floor number is divisible by 3 only, it says "Beware!".
If the floor number is divisible by 5 only, it says "Blessings!".
Otherwise, it announces the floor number - print - "Floor {number}" .
Write a Java program to simulate this elevator logic for a given floor number.

## AIM:
To write a Java program to simulate the magical elevator logic using conditional statements.

## ALGORITHM :
```
1. Start the program.
2. Read the floor number from the user.
3. Check if the floor number is divisible by both 3 and 5.
4. If true, print "Skipped".
5. Else if the floor number is divisible by 3, print "Beware!".
6. Else if the floor number is divisible by 5, print "Blessings!".
7. Otherwise, print "Floor {number}".
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

        int floor = sc.nextInt();

        if(floor % 3 == 0 && floor % 5 == 0)
        {
            System.out.println("Skipped");
        }
        else if(floor % 3 == 0)
        {
            System.out.println("Beware!");
        }
        else if(floor % 5 == 0)
        {
            System.out.println("Blessings!");
        }
        else
        {
            System.out.println("Floor " + floor);
        }
    }
}
```

## OUTPUT:
<img width="1291" height="404" alt="image" src="https://github.com/user-attachments/assets/5cd8e8a4-4128-44b8-b49f-fcde330390f3" />

## RESULT:
The Java program was executed successfully and the magical elevator message was displayed based on the given floor number.
