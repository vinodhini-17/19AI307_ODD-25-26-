# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a program to access a static variable using both class name and object.

## AIM:
To write a Java program to access a static variable using both class name and object.

## ALGORITHM :
1. Start the program.
2. Create a class with a static variable.
3. Assign a value to the static variable.
4. Create an object of the class.
5. Access the static variable using the class name.
6. Access the static variable using the object.
7. Display both values.
8. End the program.

## PROGRAM:
 ```
/*
Program to implement static variables using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
class Student
{
    static String college = "Saveetha Engineering College";
}

public class Main
{
    public static void main(String[] args)
    {
        Student s1 = new Student();

        System.out.println("Access using class name: " + Student.college);
        System.out.println("Access using object: " + s1.college);
    }
}
```

## OUTPUT:
<img width="1291" height="412" alt="image" src="https://github.com/user-attachments/assets/70230ab0-39ac-4d50-bc42-c23d8df662a9" />

## RESULT:
The Java program was executed successfully and the static variable was accessed using both the class name and the object successfully.
