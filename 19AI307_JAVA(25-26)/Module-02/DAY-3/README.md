# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Smartphone with private instance variables brand, model, and storageCapacity. Provide public getter and setter methods to access and modify these variables. Add a method called increaseStorage() that takes an integer value and increases the storageCapacity by that value.

## AIM:


## ALGORITHM :
1. Start the program.
2. Create a class named Smartphone.
3. Declare private instance variables brand, model, and storageCapacity.
4. Create public getter and setter methods for all variables.
5. Create a method increaseStorage() to increase the storage capacity.
6. Create an object of the Smartphone class.
7. Set values using setter methods.
8. Increase the storage capacity using increaseStorage().
9. Display the smartphone details using getter methods.
10. End the program.

## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: VINODHINI K
RegisterNumber:  212223230245
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Smartphone 
{
    private String brand;
    private String model;
    private int storageCapacity;

    public String getBrand() 
    {
        return brand;
    }

    public String getModel() 
    {
        return model;
    }

    public int getStorageCapacity() 
    {
        return storageCapacity;
    }

    public void setBrand(String brand) 
    {
        this.brand = brand;
    }

    public void setModel(String model) 
    {
        this.model = model;
    }

    public void setStorageCapacity(int storageCapacity)
    {
        this.storageCapacity = storageCapacity;
    }

    public void increaseStorage(int value) 
    {
        storageCapacity += value;
    }

    public void display() 
    {
        System.out.println("Brand: " + brand);
        System.out.println("Model: " + model);
        System.out.println("Updated Storage Capacity: " + storageCapacity + " GB");
        System.out.println("------------------------------");
    }
}

public class Main 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        Smartphone s = new Smartphone();

        s.setBrand(sc.nextLine());
        s.setModel(sc.nextLine());
        s.setStorageCapacity(sc.nextInt());
        int inc = sc.nextInt();

        s.increaseStorage(inc);
        s.display();
    }
}

```

## OUTPUT:
<img width="1290" height="562" alt="image" src="https://github.com/user-attachments/assets/1fb76aed-a561-4800-a84f-cae725a34985" />

## RESULT:
The Java program was executed successfully and the smartphone details along with the updated storage capacity were displayed successfully.
