# C Shap-Fundamental

# Console.Write/Console.Writeline
```
  Console.Write("Hello\nWorld");
  Console.WriteLine("Hello World!");
```
# Open CLI
```
Ctrl + `
```
# Run program
```
dotnet run
```

# Comment
```
  // 1 line comment
  /*
    Block comment
    ...
  */ 
```
# Top-level statements

namespace -> classes -> members -> method -> statements<br>
.NET 6.0 use C# 10 by default. With C# 10, you don’t necessarily need to include using System; or define a class and Main method for very simple programs, thanks to top-level statements. You can write a minimal program like this:
```
  Console.WriteLine("Hello, World!");
```
This works because C# 10 allows you to omit the traditional structure, making it easier to write quick scripts or small applications.<br>

However, if you're working on a larger project or prefer the traditional structure for readability and organization, you can still use the full syntax:<br>
Traditional C#
```
using System;

class ConsoleApp
{
    static void Main(string[] args)
    {
        Console.WriteLine("Hello, World!");
    }
}

```
Both approaches are valid, so you can choose based on your preference and the context of your project!

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
# Operator
<ol>
  <li>
    Arithmetic Operators
    <ul>
      <li>+ (Addition)</li>
      <li>- (Subtraction)</li>
      <li>* (Multiplication)</li>
      <li>/ (Division)</li>
      <li>% (Modulus) 
            7  % 3 = 1 
      </li>
    </ul>

  <li>
    Relational Operators
    <ul>
      <li>== (Equal to)</li>
      <li>!= (Not equal to)</li>
      <li>> (Greater than)</li>
      <li>< (Less than)</li>
      <li>>= (Greater than or equal to)</li>
      <li><= (Less than or equal to)</li>
    </ul>
  </li>

  <li>
    Logical Operators
    <ul>
      <li>&& (Logical AND)</li>
      <li>|| (Logical OR)</li>
      <li>! (Logical NOT)</li>
    </ul>
  </li>
        
  <li>
    Bitwise Operators
    <ul>
      <li>& (Bitwise AND)</li>
      <li>| (Bitwise OR)</li>
      <li>^ (Bitwise XOR)</li>
      <li>~ (Bitwise NOT)</li>
      <li><< (Left shift)</li>
      <li>>> (Right shift)</li>
    </ul>
  </li>
        
  <li>
    Assignment Operators
    <ul>
      <li>= (Simple assignment)</li>
      <li>+= (Add and assign)</li>
      <li>-= (Subtract and assign)</li>
      <li>*= (Multiply and assign)</li>
      <li>/= (Divide and assign)</li>
      <li>%= (Modulus and assign)</li>
      <li>&= (Bitwise AND and assign)</li>
      <li>|= (Bitwise OR and assign)</li>
      <li>^= (Bitwise XOR and assign)</li>
      <li><<= (Left shift and assign)</li>
      <li>>>= (Right shift and assign)</li>
    </ul>
  </li>
        
  <li>
    Unary Operators
    <ul>
      <li>+ (Unary plus)</li>
      <li>- (Unary minus)</li>
      <li>++ (Increment)</li>
      <li>-- (Decrement)</li>
    </ul>
  </li>
  
  <li>
    Conditional Operator
    <ul>
      <li>?: (Ternary conditional)</li>
    </ul>
  </li>
  
  <li>
    Null-Coalescing Operator
    <ul>
      <li>?? (Null-coalescing)</li>
    </ul>
  </li>
  
  <li>
    Type Comparison Operator
    <ul>
      <li>is (Checks if an object is of a specific type)</li>
      <li>as (Attempts to cast an object to a specific type, returning null if it fails)</li>
    </ul>
  </li>
  
  <li>
    Member Access Operator
    <ul>
      <li>. (Dot operator to access members of a type)</li>
    </ul>
  </li>
  
  <li>
    Indexing Operator
    <ul>
      <li>[] (Used to access elements in arrays or collections)</li>
    </ul>
  </li>
  
  <li>
    Invocation Operator
    <ul>
      <li>() (Used to call methods)</li>
    </ul>
  </li>
  
  <li>
    Event Subscription Operator
    <ul>
      <li>+= (Subscribes to events)</li>
      <li>-= (Unsubscribes from events)</li>
    </ul>
  </li>
  
  <li>
    Lambda Operator
    <ul>
      <li>=> (Lambda expression)</li>
    </ul>
  </li>
</ol>

# Type casting
<ul>
  <li>Implicit Casting: Automatic and safe (e.g., from int to long).</li>
  <li>Explicit Casting: Manual and may cause data loss (e.g., from double to int).</li>
  <li>Convert Class: Provides safe conversions between types, especially for strings.</li>
  <li>as and is Operators: Useful for checking types and safe casting.</li>
</ul>

## Implicit Casting
Implicit casting occurs when the conversion is guaranteed to be safe and does not result in data loss. This usually happens when converting from a smaller data type to a larger data type.
```
int intValue = 123;
long longValue = intValue; // Implicit casting from int to long
double doubleValue = longValue; // Implicit casting from long to double
```

## Exprlicit Casting
Explicit casting is required when converting from a larger data type to a smaller data type or when converting between incompatible types. This can result in data loss or runtime exceptions if not handled properly.
```
double doubleValue = 123.45;
int intValue = (int)doubleValue; // Explicit casting from double to int
```
In this example, doubleValue is cast to int, which will result in the fractional part being discarded (so intValue will be 123).

## Using Convert Class
```
string stringValue = "123";
int intValue = Convert.ToInt32(stringValue); // Converts string to int

```

## Using as and is Operators
The as operator is used for safe type conversions. If the conversion fails, it returns null.
```
object obj = "Hello";
string str = obj as string; // Safe casting; str will be "Hello"

```
The is operator checks if an object is of a specific type.
```
object obj = "Hello";
if (obj is string)
{
    string str = (string)obj; // Safe explicit cast
}

```

## Using TryParse
<ul>
  <li>int.TryParse</li>
  <li>double.TryParse</li>
  <li>float.TryParse</li>
  <li>decimal.TryParse</li>
  <li>long.TryParse</li>
  <li>short.TryParse</li>
  <li>DateTime.TryParse</li>
  <li>bool.TryParse</li>
</ul>

```
bool int.TryParse(string s, out int result);
```

### Parameters
s: The string to convert.
result: An out parameter that will hold the converted integer value if the conversion is successful; otherwise, it will be zero.
### Return Value
Returns true if the conversion was successful; otherwise, it returns false.
### Example
Here’s an example demonstrating how to use int.TryParse:
```
string input = "123";
int number;

if (int.TryParse(input, out number))
{
    Console.WriteLine($"Conversion successful: {number}");
}
else
{
    Console.WriteLine("Conversion failed.");
}

```

# Stack and Heap - Value type vs reference type

<ul>
  <li>Stack is for value type</li>
  <li>Heap is for reference types</li>
  <li>C# does not have a dedicated memory location specifically for global variable. It uses static fields to achieve similar functionality. This static field is on heap</li>
</ul>

## Stack
All variable below is store in stack
```
  int a = 1;
  double b = 2;
  int c = a; // copy value 1 from address of a, allocate another address for c and paste the value 1 in. a and c use 2 different address
  a = 3;  // value 3 is store in address of a, value of c is still 1

  
  ...
```
## Heap
Variable declare by new keyword
```
  int[] myArray = new int[10]; // Allocated on the heap
```
Default array
```
  using System;

  class ConsoleApp
  {
      static void Main(string[] args)
      {
          int[] d = { -4 }; // create array d
          int[] e = d;      // reference array e = array d. This will create array e and point to the same data address of array d

          Console.WriteLine($"d[0] = {d[0]}"); //d[0] = -4
          Console.WriteLine($"e[0] = {e[0]}"); //e[0] = -4
  
          d[0] = -5; // Change data value in the data address

          Console.WriteLine($"d[0] = {d[0]}"); //d[0] = -5 
          Console.WriteLine($"e[0] = {e[0]}"); //e[0] = -5
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

# Variable
Cannot start with number:
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
# Data type
using System;
```
  class ConsoleApp
  {
      static void Main(string[] args)
      {
          int a = -5;
          uint b = 5;
          char c = 'C';
          float d = 5.5f;
          float e = 5.5F;
          double f = 5.5;
          decimal g = 5.5m; // for more accurate value such as money ...
          decimal h = 5.5M;
          bool i = false;
          bool j = true;
          string k = "Hello World!";
      }
  }
```
## Build-in type
Build-in Value Type:

<table>
    <tr>
        <th></th>
        <th>C# Type</th>
        <th>.NET Type</th>
    </tr>
    <tr>
        <th>1</th>
        <td>bool</td>
        <td>System.Boolean</td>
    </tr>
    <tr>
        <th>2</th>
        <td>byte</td>
        <td>System.Byte</td>
    </tr>
    <tr>
        <th>3</th>
        <td>sbyte</td>
        <td>System.SByte</td>
    </tr>
    <tr>
        <th>4</th>
        <td>char</td>
        <td>System.Char</td>
    </tr>
    <tr>
        <th>5</th>
        <td>decimal</td>
        <td>System.Decimal</td>
    </tr>
    <tr>
        <th>6</th>
        <td>double</td>
        <td>System.Double</td>
    </tr>
    <tr>
        <th>7</th>
        <td>float</td>
        <td>System.Single</td>
    </tr>
    <tr>
        <th>8</th>
        <td>int</td>
        <td>System.Int32</td>
    </tr>
    <tr>
        <th>9</th>
        <td>uint</td>
        <td>System.UInt32</td>
    </tr>
    <tr>
        <th>10</th>
        <td>nint</td>
        <td>System.IntPtr</td>
    </tr>
    <tr>
        <th>11</th>
        <td>nuint</td>
        <td>System.UIntPtr</td>
    </tr>
    <tr>
        <th>12</th>
        <td>long</td>
        <td>System.Int64</td>
    </tr>
    <tr>
        <th>13</th>
        <td>ulong</td>
        <td>System.UInt64</td>
    </tr>
    <tr>
        <th>14</th>
        <td>short</td>
        <td>System.Int16</td>
    </tr>
    <tr>
        <th>15</th>
        <td>ushort</td>
        <td>System.UInt16</td>
    </tr>
</table>

Build-in Reference Type
<table>
    <tr>
        <th></th>
        <th>C# type</th>
        <th>.NET type</th>
    </tr>
    <tr>
        <th>1</th>
        <td>object</td>
        <td>System.Object</td>
    </tr>
    <tr>
        <th>2</th>
        <td>string</td>
        <td>System.String</td>
    </tr>
    <tr>
        <th>3</th>
        <td>dynamic</td>
        <td>System.Object</td>
    </tr>
</table>

## Simple Type Property

<table>
    <tr>
        <th>Data Type</th>
        <th>Type</th>
        <th>Size</th>
        <th>Range</th>
        <th>Example</th>
        <th>Nullable</th>
        <th>Default Value</th>
    </tr>
    <tr>
        <td>bool</td>
        <td>Value Type</td>
        <td>1 byte</td>
        <td>true or false</td>
        <td>bool isActive = true;</td>
        <td>Yes</td>
        <td>false</td>
    </tr>
    <tr>
        <td>byte</td>
        <td>Value Type</td>
        <td>1 byte</td>
        <td>0 to 255</td>
        <td>byte b = 255;</td>
        <td>Yes</td>
        <td>0</td>
    </tr>
    <tr>
        <td>sbyte</td>
        <td>Value Type</td>
        <td>1 byte</td>
        <td>-128 to 127</td>
        <td>sbyte sb = -128;</td>
        <td>Yes</td>
        <td>0</td>
    </tr>
    <tr>
        <td>short</td>
        <td>Value Type</td>
        <td>2 bytes</td>
        <td>-32,768 to 32,767</td>
        <td>short s = 30000;</td>
        <td>Yes</td>
        <td>0</td>
    </tr>
    <tr>
        <td>ushort</td>
        <td>Value Type</td>
        <td>2 bytes</td>
        <td>0 to 65,535</td>
        <td>ushort us = 65535;</td>
        <td>Yes</td>
        <td>0</td>
    </tr>
    <tr>
        <td>int</td>
        <td>Value Type</td>
        <td>4 bytes</td>
        <td>-2,147,483,648 to 2,147,483,647</td>
        <td>int i = 100;</td>
        <td>Yes</td>
        <td>0</td>
    </tr>
    <tr>
        <td>uint</td>
        <td>Value Type</td>
        <td>4 bytes</td>
        <td>0 to 4,294,967,295</td>
        <td>uint ui = 4000000000;</td>
        <td>Yes</td>
        <td>0</td>
    </tr>
    <tr>
        <td>long</td>
        <td>Value Type</td>
        <td>8 bytes</td>
        <td>-9,223,372,036,854,775,808 to 9,223,372,036,854,775,807</td>
        <td>long l = 10000000000;</td>
        <td>Yes</td>
        <td>0</td>
    </tr>
    <tr>
        <td>ulong</td>
        <td>Value Type</td>
        <td>8 bytes</td>
        <td>0 to 18,446,744,073,709,551,615</td>
        <td>ulong ul = 18446744073709551615;</td>
        <td>Yes</td>
        <td>0</td>
    </tr>
    <tr>
        <td>float</td>
        <td>Value Type</td>
        <td>4 bytes</td>
        <td>±1.5 x 10<sup>−45</sup> to ±3.4 x 10<sup>38</sup></td>
        <td>float f = 3.14f;</td>
        <td>Yes</td>
        <td>0.0f</td>
    </tr>
    <tr>
        <td>double</td>
        <td>Value Type</td>
        <td>8 bytes</td>
        <td>±5.0 x 10<sup>−324</sup> to ±1.7 x 10<sup>308</sup></td>
        <td>double d = 3.14;</td>
        <td>Yes</td>
        <td>0.0</td>
    </tr>
    <tr>
        <td>decimal</td>
        <td>Value Type</td>
        <td>16 bytes</td>
        <td>±1.0 x 10<sup>−28</sup> to ±7.9 x 10<sup>28</sup> (28-29 significant digits)</td>
        <td>decimal dec = 19.99m;</td>
        <td>Yes</td>
        <td>0.0</td>
    </tr>
    <tr>
        <td>char</td>
        <td>Value Type</td>
        <td>2 bytes</td>
        <td>U+0000 to U+FFFF (Unicode)</td>
        <td>char c = 'A';</td>
        <td>Yes</td>
        <td>'\0'</td>
    </tr>
    <tr>
        <td>string</td>
        <td>Reference Type</td>
        <td>Varies</td>
        <td>Any sequence of characters</td>
        <td>string str = "Hello";</td>
        <td>Yes</td>
        <td>null</td>
    </tr>
    <tr>
        <td>object</td>
        <td>Reference Type</td>
        <td>Varies</td>
        <td>Any type (base type for all)</td>
        <td>object obj = new object();</td>
        <td>Yes</td>
        <td>null</td>
    </tr>
</table>
