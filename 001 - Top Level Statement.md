# Top-level statements

namespace -> classes -> members -> method -> statements<br>
.NET 6.0 use C# 10 by default. With C# 10, you don’t necessarily need to include using System; or define a class and Main method for very simple programs, thanks to top-level statements. You can write a minimal program like this:
```
  Console.WriteLine("Hello, World!");
```
This works because C# 10 allows you to omit the traditional structure, making it easier to write quick scripts or small applications.<br>

However, if you're working on a larger project or prefer the traditional structure for readability and organization, you can still use the full syntax:<br>
Traditional C#<br>
The Auto-generate code does not  define a namespace, so the "ConsoleApp" class is implicitly defined in an empty namespace with no name instead of a namespace that matches the name of the project.
```
using System;
//namespace ???? {
  class ConsoleApp
  {
      static void Main(string[] args)
      {
          Console.WriteLine("Hello, World!");
      }
  }
//}
```
Both approaches are valid, so you can choose based on your preference and the context of your project!
