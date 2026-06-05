# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Create a class Car with attributes brand, model, year. Create 2 objects and print their details.

## AIM:
To write a Java program to create a class named Car with attributes brand, model, and year, create two objects, and print their details.

## ALGORITHM :
1. Start the program.
2. Create a class named Car with attributes brand, model, and year.
3. Create a constructor to initialize the attributes.
4. Create a method to display car details.
5. Create two objects of the Car class.
6. Assign values to the objects.
7. Display the details of both objects.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement class and objects using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
class Car
{
    String brand;
    String model;
    int year;

    Car(String b, String m, int y)
    {
        brand = b;
        model = m;
        year = y;
    }

    void display()
    {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Year: " + year);
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Car car1 = new Car("Toyota", "Camry", 2020);
        Car car2 = new Car("Honda", "City", 2022);

        car1.display();
        System.out.println();
        car2.display();
    }
}
```

## OUTPUT:
<img width="1294" height="295" alt="image" src="https://github.com/user-attachments/assets/b17d7e1a-a518-4c69-a0bd-e29ed6dad9df" />

## RESULT:
The Java program was executed successfully and the details of the two Car objects were displayed successfully.
