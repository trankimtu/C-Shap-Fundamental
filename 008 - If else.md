# If else
```
using System;

class ConsoleApp
{
    static void Main(string[] args)
    {
        Console.WriteLine("1 + 1 = ?");
        Console.WriteLine("A. 10");
        Console.WriteLine("B. 1");
        Console.WriteLine("C. 2");
        Console.Write("Input your choice A, B, or C: ");

        string message = "";
        string choice = Console.ReadLine();

        if (choice == "A")
        {
            message = $"Your {choice} is correct in Binary";
        }
        else if (choice == "B")
        {
            message = $"Your {choice} is wrong";
        }
        else if (choice == "C")
        {
            message = $"Your {choice} is correct in Decimal";
        }
        else
        {
            message = $"Your {choice} is not an option ";
            message += $"Please input A, B, or C";
        }
        Console.WriteLine(message);
    }
}
```
