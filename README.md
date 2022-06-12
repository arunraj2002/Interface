# Interface

## Aim:
To Develop a small bank application by declaring deposit() and withdrawal() as abstract methods in the interface.  Get the choice from the user whether to perform withdrawal or deposit operation. After the operation completes, display the balance amount

## Algorithm:
### step 1: 
Create an interface.

### step 2:
Create a child class.

### step 3:
Declare 2 functions deposit() and withdrawal() as abstract methods in the interface.

### step 4:
Create those 2 functions in the child class and perform respective operation.

### step 4:
Use while loop and and switch case to Get the choice from the user whether to perform withdrawal or deposit operation.

### step 5:
After performing the functions display the remaining balance of the user.

## Program:
```c#
using System;

namespace inter
{
    public interface bank
    {
        void deposit();
        void withdraw();
    }
    public class operation : bank
    {
        public int amount, ch, balance = 5000;
        public operation()
        {
            Console.WriteLine("Enter the Choice\n1.deposit 2.Withdraw");
            ch = Convert.ToInt32(Console.ReadLine());
            if (ch == 1)
            {
                deposit();
            }
            else
            {
                withdraw();
            }
        }
        public void withdraw()
        {
            int amount = Convert.ToInt32(Console.ReadLine());
            balance = balance - amount;
            Console.WriteLine("Balance="+balance);
        }
        public void deposit()
        {
            int amount = Convert.ToInt32(Console.ReadLine());
            balance = balance + amount;
            Console.WriteLine("Balance="+balance);
        }

    }
    public class banking
    {
        public static void Main()
        {
            operation o = new operation();
        }
    }

}
```
## Output:
![Capture](https://user-images.githubusercontent.com/75235747/173223523-7fd6f548-03e6-4bbb-855e-90f879ae53d4.JPG)

## Result:
C# program to develop a bank application using interface is implemented successfully.
