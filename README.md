# C Shap-Fundamental

# Console.Write/Console.Writeline
```
  Console.Write("Hello\nWorld");
  Console.WriteLine("Hello World!");
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

# Stack and Heap

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
  ...
```

