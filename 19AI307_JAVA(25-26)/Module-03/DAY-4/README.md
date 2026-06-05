# Ex.No:4(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.
Bot Types:
SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".
RainBot: Predicts "COLD" if temperature < 20, else "WARM".
Input:
temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.

## AIM:
To write a Java program to implement interfaces using weather prediction bots.

## ALGORITHM :
1. Start the program.
2. Create an interface with a method predict().
3. Create a class SunBot that implements the interface.
4. If temperature is greater than 30, return "HOT", otherwise return "MODERATE".
5. Create a class RainBot that implements the interface.
6. If temperature is less than 20, return "COLD", otherwise return "WARM".
7. Read the temperature and bot type from the user.
8. Create the corresponding bot object based on the bot type.
9. Display the prediction result.
10. End the program.

## PROGRAM:
 ```
/*
Program to implement interfaces using Java
Developed by:VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

interface WeatherBot
{
    String predict(int temperature);
}

class SunBot implements WeatherBot
{
    public String predict(int temperature)
    {
        if(temperature > 30)
        {
            return "HOT";
        }
        else
        {
            return "MODERATE";
        }
    }
}

class RainBot implements WeatherBot
{
    public String predict(int temperature)
    {
        if(temperature < 20)
        {
            return "COLD";
        }
        else
        {
            return "WARM";
        }
    }
}

public class Main
{
    public static void main(String[] args)
    {
        Scanner sc = new Scanner(System.in);

        int temperature = sc.nextInt();
        int botType = sc.nextInt();

        if(botType == 1)
        {
            SunBot s = new SunBot();
            System.out.println(s.predict(temperature));
        }
        else if(botType == 2)
        {
            RainBot r = new RainBot();
            System.out.println(r.predict(temperature));
        }
    }
}
```

## OUTPUT:
<img width="1288" height="269" alt="image" src="https://github.com/user-attachments/assets/5b26d10c-46f4-4b3f-af20-a0cd09e175e7" />

## RESULT:
The Java program was executed successfully and the weather prediction was displayed successfully using interfaces.
