# Ex.No:4(B)  IMPLEMENT SOLID PRINCIPLES IN JAVA PROGRAM 

## QUESTION:
In a gaming lounge, there is only one master console power switch that controls all gaming consoles. Whenever a player turns on any console, it internally triggers the master power. The master switch must ensure only one instance is ever created, regardless of how many times it's accessed, to prevent power fluctuations.
Every time a player accesses the master switch, it logs an access count. Since the switch is Singleton, the count should increment globally and reflect shared state

## AIM:
To write a Java program to implement the Singleton design pattern for a master console power switch with a global access count.

## ALGORITHM :
1. Start the program.
2. Create a class named MasterSwitch.
3. Declare a private static object of the same class.
4. Declare a private static accessCount variable.
5. Create a private constructor to prevent object creation from outside.
6. Create a public static method getInstance() to return the single object.
7. Increment the access count whenever the instance is accessed.
8. Create a method to display the access count.
9. Access the singleton object multiple times.
10. Display the global access count.
11. End the program.

## PROGRAM:
 ```
/*
Program to implement Singleton design pattern using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.util.*;

class MasterPowerSwitch 
{
    private static MasterPowerSwitch instance=null;
    private int c=0;
    
    public static MasterPowerSwitch getInstance()
    {
        if(instance==null)
        {
            instance=new MasterPowerSwitch();
        }
        
        return instance;
    }
    
    private MasterPowerSwitch(){};
    
    public int logAccess()
    {
        return ++c;
    }
}

public class prog 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        sc.nextLine();

        for (int i = 0; i < n; i++) 
        {
            String player = sc.nextLine();
            MasterPowerSwitch power = MasterPowerSwitch.getInstance();
            int count = power.logAccess();
            System.out.println(player + " accessed Master Power Switch. Total accesses so far: " + count);
        }
    }
}
```

## OUTPUT:
<img width="1293" height="359" alt="image" src="https://github.com/user-attachments/assets/e2eb9f3c-9570-4828-8d2a-c5825d7b57e9" />

## RESULT:
The Java program was executed successfully and the Singleton object maintained a shared global access count successfully.
