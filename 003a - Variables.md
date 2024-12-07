# Variables
Camel Case: camelCase<br>
Pascal Case: PascalCase<br>
Snake Case: snake_case<br>

Suggest using Camel Case standard.
```
  int minInt = -2147483648; // a 4-byte area is allocated in Ram to store the value. The address of this specific area is set to minInt
  int maxInt =  2147483648;
  string s = "abc" + "def"; // Concatenate 2 string to "abcdef"
  byte b = 255; // Value 0-255
  char c = 'a';
  decimal dec = 3.14m;
  float f = 3.14f; 
  double d = 3.14 + 5.12;
```

Variables cannot start with number:
```
  string 5x = "abc"; // Error
```

Variable can use in: <br>
Expression - Evaluates to a value<br>
```
  using System;

  class ConsoleApp
  {
      static void Main(string[] args)
      {
          Console.Write("Input Your name: ");
          string name = Console.ReadLine();
          Console.WriteLine("Hello " + name + "!");
          // expression "Hello " + name + "!"
          // Operands: "Hello ", name, "!" are operands
          // Operator: + use to concatinate 3 strings.
          //literal: "Hello ", "!"  which are actual value
      }
  }

```

## Declaration a variable
```
  int x;
```
Declare a variable and use it without initialization will cause run time error<br>
To void it, use nullable type<br>
Nullable Type: int? is a shorthand for Nullable<int>. This allows the variable x to hold either an integer value or null.
```
  int? x = null; // Nullable<int> x = null;
```

## Initialization
```
  x = 5
```
During compilation, the compiler adds an entry for the variable x in the <strong>symbol table</strong>
<table>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Scope</th>
    <th>Address</th>
  </tr>
  <tr>
    <td>x</td>
    <td>int</td>
    <td>local (method)</td>
    <td>0x001</td>
  </tr>
</table>
Value Assignment<br>
The value 5 is stored in the memory location allocated for x.<br>
<strong>Stack Memory</strong>
<table>
  <tr>
    <th>Address</th>
    <th>Value</th>
  </tr>
  <tr>
    <td>0x001</td>
    <td>5</td>
  </tr>
</table>
