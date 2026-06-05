# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Create a class Calculator with: One non-static method add(int a, int b) that returns the sum, One static method info() that says "Calculator is ready".

## AIM:
To write a Java program to create a Calculator class with a non-static add() method and a static info() method.

## ALGORITHM :
1. Start the program.
2. Create a class named Calculator.
3. Create a non-static method add(int a, int b) to return the sum.
4. Create a static method info() to display a message.
5. Create an object of the Calculator class.
6. Call the static method using the class name.
7. Call the non-static method using the object.
8. Display the result.
9. End the program.

## PROGRAM:
 ```
/*
Program to implement static and non-static methods using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
class Calculator
{
    int add(int a, int b)
    {
        return a + b;
    }

    static void info()
    {
        System.out.println("Calculator is ready");
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Calculator.info();

        Calculator c = new Calculator();

        int result = c.add(10, 20);

        System.out.println("Sum = " + result);
    }
}
```

## OUTPUT:
<img width="1300" height="414" alt="image" src="https://github.com/user-attachments/assets/a7e404ae-a917-476b-bf9c-9342ff743648" />

## RESULT:
The Java program was executed successfully and the static method and non-static method were called successfully.
