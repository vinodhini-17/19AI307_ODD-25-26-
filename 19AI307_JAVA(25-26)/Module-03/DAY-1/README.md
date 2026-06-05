# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
Create a Super class Person with fields name and age. Create a subclass Student that inherits from Person and adds a field marks (integer). Implement a method in Student called calculateGrade() which returns the grade based on the marks:
Marks ≥ 90: Grade A
Marks ≥ 75 and < 90: Grade B
Marks ≥ 50 and < 75: Grade C
Marks < 50: Grade F

## AIM:
To write a Java program to implement inheritance using a superclass Person and a subclass Student with grade calculation based on marks.

## ALGORITHM :
1. Start the program.
2. Create a superclass named Person with fields name and age.
3. Create a subclass named Student that inherits Person and adds marks.
4. Create a method calculateGrade() in Student.
5. Check the marks using conditional statements.
6. Return Grade A if marks are greater than or equal to 90.
7. Return Grade B if marks are between 75 and 89.
8. Return Grade C if marks are between 50 and 74.
9. Return Grade F if marks are below 50.
10. Create an object of Student class.
11. Display the student details and grade.
12. End the program.

## PROGRAM:
 ```
/*
Program to implement inheritance using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

class Person
{
    String name;
    int age;

    Person(String name, int age) 
    {
        this.name = name;
        this.age = age;
    }
}

class Student extends Person 
{
    int marks;

    Student(String name, int age, int marks)
    {
        super(name, age);
        this.marks = marks;
    }

    char calculateGrade()
    {
        if (marks >= 90)
            return 'A';
        else if (marks >= 75)
            return 'B';
        else if (marks >= 50)
            return 'C';
        else
            return 'F';
    }
}

public class Main
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);

        String name = sc.nextLine();
        int age = sc.nextInt();
        int marks = sc.nextInt();

        Student s = new Student(name, age, marks);

        System.out.println("Name: " + s.name);
        System.out.println("Age: " + s.age);
        System.out.println("Marks: " + s.marks);
        System.out.println("Grade: " + s.calculateGrade());
    }
}
```

## OUTPUT:
<img width="1295" height="683" alt="image" src="https://github.com/user-attachments/assets/2ab251a5-9ec5-46f8-b4cf-a91b9adb030d" />

## RESULT:
The Java program was executed successfully and the student grade was calculated and displayed successfully using inheritance.
