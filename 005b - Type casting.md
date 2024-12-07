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
s: The string to convert.<br>
result: An out parameter that will hold the converted integer value if the conversion is successful; otherwise, it will be zero.<br>
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
