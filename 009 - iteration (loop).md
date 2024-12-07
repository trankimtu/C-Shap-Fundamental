# For loop
```
using System;

class ConsoleApp
{
    static void Main(string[] args)
    {
        Console.WriteLine("For loop");
        for (int i = 0; i < 10; i++)
        {
            if (i == 4)
            {
                Console.WriteLine($"i = {i} continue");
                continue;
            }
            if (i == 7)
            {
                Console.WriteLine($"i = {i} break");
                break;
            }
            Console.WriteLine(i);
        
        }
    }
}
```
# While loop
```
using System;

class ConsoleApp
{
    static void Main(string[] args)
    {
        int j = 0;
        Console.WriteLine("While loop");
        while (j < 10)
        {
            if (j == 4)
            {
                Console.WriteLine($"j = {j} continue");
                j++;
                continue;
            }
            if (j == 7)
            {
                Console.WriteLine($"j = {j} break");
                break;
            }
            Console.WriteLine(j);
            j++;

        }
    }
}
```
# Do while loop
```
int k = 0;
Console.WriteLine("Do While loop");
do
{
    if (k == 4)
    {
        Console.WriteLine($"k = {k} continue");
        k++;
        continue;
    }
    if (k == 7)
    {
        Console.WriteLine($"k = {k} break");
        break;
    }
    Console.WriteLine(k);
    k++;
}
while (k < 10);
```
