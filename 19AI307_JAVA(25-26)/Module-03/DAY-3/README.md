# Ex.No:3(C) ABSTRACTION

## QUESTION:
Create abstract class BankAccount with method calculateInterest(). Extend it in SavingsAccount and FixedDepositAccount.
Input Format:
First line: 1 for SavingsAccount, 2 for FixedDepositAccount
- If 1: next line → balance (double)
- If 2: next line → amount (double) and years (int)
Output Format:
- A single line showing interest earned rounded to 2 decimal places.

## AIM:
To write a Java program to implement abstraction using an abstract class BankAccount and subclasses SavingsAccount and FixedDepositAccount.

## ALGORITHM :
1. Start the program.
2. Create an abstract class named BankAccount with an abstract method calculateInterest().
3. Create a subclass SavingsAccount that calculates interest for savings balance.
4. Create a subclass FixedDepositAccount that calculates interest based on amount and years.
5. Read the account type from the user.
6. If the choice is 1, read the balance and calculate savings interest.
7. If the choice is 2, read the amount and years and calculate fixed deposit interest.
8. Display the interest earned rounded to 2 decimal places.
9. End the program.
    
## PROGRAM:
 ```
/*
Program to implement abstraction using Java
Developed by: VINODHINI K
RegisterNumber: 212223230245
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

abstract class BankAccount 
{
    abstract double calculateInterest();
}

class SavingsAccount extends BankAccount 
{
    double balance;
    final double rate = 0.04; 

    SavingsAccount(double balance) 
    {
        this.balance = balance;
    }

    double calculateInterest() 
    {
        return balance * rate;
    }
}

class FixedDepositAccount extends BankAccount 
{
    double amount;
    int years;
    final double rate = 0.07;

    FixedDepositAccount(double amount, int years) 
    {
        this.amount = amount;
        this.years = years;
    }

    double calculateInterest() 
    {
        return amount * rate * years;
    }
}

public class Main 
{
    public static void main(String[] args) 
    {
        Scanner sc = new Scanner(System.in);
        int choice = sc.nextInt();

        BankAccount account;

        if (choice == 1) 
        {
            double balance = sc.nextDouble();
            account = new SavingsAccount(balance);
        } 
        else 
        {
            double amount = sc.nextDouble();
            int years = sc.nextInt();
            account = new FixedDepositAccount(amount, years);
        }

        System.out.printf("%.2f", account.calculateInterest());
    }
}
```

## OUTPUT:
<img width="1288" height="468" alt="image" src="https://github.com/user-attachments/assets/5ec5fec7-a6c9-4199-9f68-ab0c4326efe4" />

## RESULT:
The Java program was executed successfully and the interest earned was calculated and displayed successfully using abstraction.
