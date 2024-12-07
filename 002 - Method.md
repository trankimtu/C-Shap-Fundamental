# Method
<ul>
  <li>Create the method</li>
  <li>Invoke the method</li>
</ul>

## Static method
Call the method directly
WriteLine() is a Static method in class Console. We can call the WriteLine() method directly without create an instance for it.<br>
Cannot create instance of a static class
```
Console.WriteLine();
```

## Instance method (Public, Private ...)
Must create instance of the class<br>
Then invoke or call the method under the instance
```
class ConsoleApp
{
    static void Main(string[] args)
    {
        Console.WriteLine("Hello, World!\nHello Tu");
        ConsoleApp callMyName = new ConsoleApp();
        callMyName.MyName();
        
    }

    void MyName () {
        string myName = "Tu";
        Console.WriteLine(myName);
    }
}
```

# Passing args in Main method
Code 1
```
using System;

class ConsoleApp
{
    static void Main(string[] args)
    {
        Console.WriteLine(args[0]);
    }
}
```
Output 1
```
  dotnet run Hello World!  -> Output result: Hello
  dotnet run "Hello World!"  -> Output result: Hello World!
  dotnet run -- -Hello -> Output: -Hello
```

Code 2
```
using System;

class ConsoleApp
{
    static void Main(string[] args)
    {
        for (int i = 0; i < args.Length; i++)
        {
            Console.Write(args[i] + " ");

        }
    }
}
```
Output 2
```
  dotnet run This is my String -> Output: This is my String
```
