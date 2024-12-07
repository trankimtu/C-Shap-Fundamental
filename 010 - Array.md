# Array
```
using System;

class ConsoleApp
{
    static void Main(string[] args)
    {
        // Way 1
        int[] array = new int[5];
        for (int i = 0; i < array.Length; i++)
        {
            array[i] = i+1;
        }
        for (int i = 0; i < 5; i++)
        {
            Console.WriteLine(array[i]);
        }
        
        // Way 2
        int[] numbers = new int[] { 1, 2, 3, 4, 5 };
        for (int i = 0; i < numbers.Length; i++)
        {
            Console.WriteLine(numbers[i]);
        }
        
        // Way 3
        char[] chars = { 'a', 'b', 'c', 'd', 'e' };
        for (int i = 0; i < chars.Length; i++)
        {
            Console.WriteLine(chars[i]);
        }

        // String to chars
        Console.WriteLine("ToCharArray");
        string myString = "This is my string";
        char[] charArray = myString.ToCharArray();
        for (int i = 0; i < charArray.Length; i++)
        {
            Console.WriteLine(charArray[i]);
        }
    }
}
```
