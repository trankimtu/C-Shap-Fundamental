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
Note: <br>
1 <strong>Char</strong> is not always a single letter. It's 16 bit Unicode character
Ex: <br> 
'æ': count as 1 char. But it's component include 'a' and 'e' <br>
'á': count as 1 char. But it's component include a + ◌́ (Combining Acute Accent)<br>

<strong>String</strong>: instead using esc key, place $ in front of "..." to make all insie is tring. \t \n ... inside won't be convert to tab or new line.
 

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
