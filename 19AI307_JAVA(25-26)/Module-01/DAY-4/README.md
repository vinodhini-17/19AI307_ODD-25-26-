# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java Program to Find the Average of Array Elements.

## AIM:
To write a Java program to find the average of array elements.

## ALGORITHM :
```
1. Start the program.
2. Read the size of the array from the user.
3. Declare an array of given size.
4. Read the array elements.
5. Find the sum of all array elements using a loop.
6. Calculate the average by dividing the sum by the number of elements.
7. Display the average value.
8. End the program.
```
## PROGRAM:
 ```
/*
Program to implement array operations using Java
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
        int[] arr = new int[n];

        int sum = 0;

        for(int i = 0; i < n; i++)
        {
            arr[i] = sc.nextInt();
            sum = sum + arr[i];
        }

        double average = (double)sum / n;

        System.out.println("Average = " + average);
    }
}
```

## OUTPUT:
<img width="1289" height="588" alt="image" src="https://github.com/user-attachments/assets/d9ac0fa2-a1b3-42a0-8764-8e1a2b2f1c72" />

## RESULT:
The Java program was executed successfully and the average of the array elements was calculated and displayed successfully.
