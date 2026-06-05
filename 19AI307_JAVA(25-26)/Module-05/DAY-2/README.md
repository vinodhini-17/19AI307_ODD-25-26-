# Ex.No:5(B) SERIALIZATION AND DESERIALIZATION 

## QUESTION:
Write a Java program to serialize a collection of objects (like ArrayList<Student>) into a file.

## AIM:
To write a Java program to serialize a collection of Student objects using ArrayList into a file.

## ALGORITHM :
1. Start the program.
2. Create a Student class that implements Serializable.
3. Declare student attributes and create a constructor.
4. Create an ArrayList to store Student objects.
5. Add Student objects to the ArrayList.
6. Create a FileOutputStream object for the file.
7. Create an ObjectOutputStream object.
8. Write the ArrayList object into the file using writeObject().
9. Close the streams.
10. Display a success message.
11. End the program.
    
## PROGRAM:
 ```
/*
Program to implement serialization of collection objects using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.io.*;
import java.util.*;

class Student implements Serializable
{
    private static final long serialVersionUID = 1L;

    private int id;
    private String name;
    private double marks;

    public Student(int id, String name, double marks) 
    {
        this.id = id;
        this.name = name;
        this.marks = marks;
    }

    @Override
    public String toString() 
    {
        return "Student{id=" + id + ", name='" + name + "', marks=" + marks + "}";
    }
}

public class StudentSerializationUserInput
{

    public static void serializeStudents(List<Student> students, String fileName) 
    {
        try (ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream(fileName))) 
        {
            oos.writeObject(students);
            System.out.println("Students serialized successfully into: " + fileName);
        } 
        catch (IOException e)
        {
            System.out.println("Error during serialization: " + e.getMessage());
        }
    }

    @SuppressWarnings("unchecked")
    public static List<Student> deserializeStudents(String fileName) 
    {
        List<Student> students = null;
        try (ObjectInputStream ois = new ObjectInputStream(new FileInputStream(fileName))) 
        {
            students = (List<Student>) ois.readObject();
            System.out.println("Students deserialized successfully from: " + fileName);
        } 
        catch (IOException | ClassNotFoundException e) 
        {
            System.out.println("Error during deserialization: " + e.getMessage());
        }
        return students;
    }

    public static void main(String[] args) 
    {
        Scanner scanner = new Scanner(System.in);
        List<Student> students = new ArrayList<>();

        int n = scanner.nextInt();
        scanner.nextLine(); 

        for (int i = 0; i < n; i++) 
        {
            int id = scanner.nextInt();
            scanner.nextLine();

            String name = scanner.nextLine();

            double marks = scanner.nextDouble();
            scanner.nextLine();

            students.add(new Student(id, name, marks));
        }

        String fileName = "students.dat";

        serializeStudents(students, fileName);

        List<Student> deserializedStudents = deserializeStudents(fileName);

        if (deserializedStudents != null) 
        {
            System.out.println("\nDeserialized Students:");
            for (Student s : deserializedStudents) 
            {
                System.out.println(s);
            }
        }

        scanner.close();
    }
}
```

## OUTPUT:
<img width="1296" height="550" alt="image" src="https://github.com/user-attachments/assets/659c9c71-6e0c-475e-a567-185f4f7eadd9" />

## RESULT:
The Java program was executed successfully and the collection of Student objects was serialized into a file successfully.
