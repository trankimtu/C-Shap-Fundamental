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
