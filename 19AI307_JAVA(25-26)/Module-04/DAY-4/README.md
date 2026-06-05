# Ex.No:4(D) DESIGN PATTERN -- ABSTRACT FACTORY

## QUESTION:
You’re creating a cross-platform UI tool using the Abstract Factory pattern. Implement factories to create Button and Checkbox for "dark" and "light" themes. Let the user choose the theme, then generate UI components and display their types

## AIM:
To write a Java program to implement the Abstract Factory design pattern for creating Button and Checkbox components for dark and light themes.

## ALGORITHM :
1. Start the program.
2. Create interfaces Button and Checkbox.
3. Create concrete classes for DarkButton, LightButton, DarkCheckbox, and LightCheckbox.
4. Create an abstract factory interface UIFactory with methods createButton() and createCheckbox().
5. Create DarkThemeFactory and LightThemeFactory classes implementing UIFactory.
6. Read the theme choice from the user.
7. Create the corresponding factory object.
8. Generate Button and Checkbox objects using the factory.
9. Display the types of UI components created.
10. End the program.
    
## PROGRAM:
 ```
/*
Program to implement Abstract Factory design pattern using Java
Developed by:VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface Button
{
    void display();
}

interface Checkbox
{
    void display();
}

class DarkButton implements Button
{
    public void display()
    {
        System.out.println("Dark Theme Button");
    }
}

class LightButton implements Button
{
    public void display()
    {
        System.out.println("Light Theme Button");
    }
}

class DarkCheckbox implements Checkbox
{
    public void display()
    {
        System.out.println("Dark Theme Checkbox");
    }
}

class LightCheckbox implements Checkbox
{
    public void display()
    {
        System.out.println("Light Theme Checkbox");
    }
}

interface UIFactory
{
    Button createButton();
    Checkbox createCheckbox();
}

class DarkThemeFactory implements UIFactory
{
    public Button createButton()
    {
        return new DarkButton();
    }

    public Checkbox createCheckbox()
    {
        return new DarkCheckbox();
    }
}

class LightThemeFactory implements UIFactory
{
    public Button createButton()
    {
        return new LightButton();
    }

    public Checkbox createCheckbox()
    {
        return new LightCheckbox();
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);

        String theme = sc.nextLine();

        UIFactory factory;

        if(theme.equalsIgnoreCase("dark"))
        {
            factory = new DarkThemeFactory();
        }
        else
        {
            factory = new LightThemeFactory();
        }

        Button b = factory.createButton();
        Checkbox c = factory.createCheckbox();

        b.display();
        c.display();
    }
}
```

## OUTPUT:
<img width="1298" height="406" alt="image" src="https://github.com/user-attachments/assets/3643b5aa-96b6-4c7a-a0d5-450b3af3a92b" />

## RESULT:
The Java program was executed successfully and the UI components for the selected theme were created and displayed successfully using the Abstract Factory design pattern.
