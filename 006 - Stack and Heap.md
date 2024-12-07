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
