# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program that calculates the area of different shapes using method overloading. Create a class AreaCalculator with:
area(int side) for square
area(int length, int breadth) for rectangle
area(double radius) for circle

## AIM:
To write a Java program to calculate the area of different shapes using method overloading.

## ALGORITHM :
1. Start the program.
2. Create a class named AreaCalculator.
3. Create a method area(int side) to calculate the area of a square.
4. Create a method area(int length, int breadth) to calculate the area of a rectangle.
5. Create a method area(double radius) to calculate the area of a circle.
6. Create an object of the AreaCalculator class.
7. Call the overloaded methods with different parameters.
8. Display the calculated areas.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement method overloading using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class AreaCalculator 
{
    void area(int side) 
    {
        System.out.println("Area of square: " + (side * side));
    }
    void area(int length, int breadth) 
    {
        System.out.println("Area of rectangle: " + (length * breadth));
    }

    void area(double radius) 
    {
        System.out.println("Area of circle: " + (Math.PI * radius * radius));
    }
}

public class Main 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        AreaCalculator ac = new AreaCalculator();

        int side = sc.nextInt();
        ac.area(side);

        int length = sc.nextInt();
        int breadth = sc.nextInt();
        ac.area(length, breadth);

        double radius = sc.nextDouble();
        ac.area(radius);
    }
}
```

## OUTPUT:
<img width="1291" height="493" alt="image" src="https://github.com/user-attachments/assets/67c425d9-3986-4487-98d5-d094d68a581e" />

## RESULT:
The Java program was executed successfully and the areas of square, rectangle, and circle were calculated and displayed successfully using method overloading.
