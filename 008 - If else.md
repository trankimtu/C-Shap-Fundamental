# If ... else if ... else ...
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
# If ... else ...
```
using System;

class ConsoleApp
{
    static void Main(string[] args)
    {
        Console.WriteLine("1 + 1 = ?");
        Console.WriteLine("A. 10");

        Console.Write("Input your choice A: ");

        string message = "";
        string choice = Console.ReadLine();

        if (choice == "A")
        {
            message = $"Your {choice} is correct in Binary";
        }
        else
        {
            message = $"Your {choice} is not an option ";
            message += $"Please input A";
        }
        Console.WriteLine(message);

        string message2 = (choice == "A") 
            ? $"Your {choice} is correct in Binary" 
            : string.Format("Your {0} is not an option. Please input A", choice); // use index
        Console.WriteLine($"message2 = {message2}");
    }
}
```
# Switch ... case
switch (day) {
    case 1:
        Console.WriteLine("Monday");
        break;
    case 2:
        Console.WriteLine("Tuesday");
        break;
    // Other cases...
    default:
        Console.WriteLine("Unknown day");
        break;
}
```
