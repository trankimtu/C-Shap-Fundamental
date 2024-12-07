# User input
```
  using System;

  class ConsoleApp
  {
      static void Main(string[] args)
      {
          Console.Write("Input Your name: ");
          string name = Console.ReadLine();
          Console.WriteLine("Hello " + name + "!");
          Console.WriteLine($"Hello {name}!"); // String interpolation

      }
  }

```
Output:
```
  Input Your name: Tu Tran
  Hello Tu Tran!
  Hello Tu Tran!
```
