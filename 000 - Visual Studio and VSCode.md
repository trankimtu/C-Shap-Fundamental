# SDK
Must update .NET runtime and .NET SDK
```
dotnet --version
```
```
dotnet --info
```
```
dotnet --list-sdks
```
# .NET Runtime
```
dotnet --list-runtimes
```
From .NET 5 and above, there's no separate between .NET and .NET Core.
# Visual Studio
## Add Workloads: ASP.NET, .NET desktop development, Python development
Tools -> Get Tools and Features
<ul>
  <li>ASP.NET and web development</li>
  <li>.NET desktop development: this inculdes console app</li>
  <li>Desktop development with C++ with all default component: this enables publishing console apps and web services that start faster and have smaller meory footprints</li>
</ul>

## Set StartUp Project
Right-click on the project choose "Set as startup project" to set a startUp project or right-click on the solution choose "Configure Startup Project" to start up multiple projects

## Change value in multiple places
Change in one then press Control + "." select rename 'old" to 'new"

## Start without debugging
Ctrl + F5 or Green outline Triangle

## In Visual Studio 2022 for windows
run a console app, it executes the app from the <project name>\bin\Debug\net9.0 folder



# Visual Studio Code
## Extension
<ul>
  <li>C# Dev Kit</li>
  <li>C# - This will automatically install with C# Dev Kit</li>
  <li>Polyglot Notebooks</li>
</ul>
Keyboard shortcut 
https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf
<br>

Help
```
dotnet help <command>
```
1. Create folder for the solution
2. Create new solution

```
dotnet new sln --name <Solution name>
```
3. Create new project, this will create a subfolder name <project name> in the same location of sln file
```
dotnet new console ---output <project name>
```
4. Add project
```
dotnet sln add <project name>
```
5. Repeat 3 and 4> <br>
- 3. Add 2nd project using VSCode<br>
place cursor in folder contain sln file
```
dotnet new console -o <2nd project name> --use-program-main
```
- 4. Add 2nd project to sln<br>
Place cursor in folder contain sln
```
dotnet sln add <2nd project name>
```
6. Open folder: code .
7. Set Regions
```
#region

#endregion
```
## Naming convention
Camel case - local variables, private fields<br>
Title case aka pascal case - Type, non-private fields, and other member like methods<br>
### nameof

```
nameof (<Variable>, <type>, or <member> ...);
```
Function will return a string with value = <Variable>, <type>, or <member> <br>
Benefit
<ul>
  <li><strong>Refactoring:</strong> When you rename the variable, method, or member using a tool like Visual Studio, nameof will automatically update, reducing the risk of errors compared to hard-coded strings.</li>
  <li><strong>Readability:</strong> Makes your code more readable and maintainable.</li>
  <li><strong>Consistency:</strong> Ensures the correctness of names used in code, especially useful in logging and exception handling.</li>
</ul>
Common Use Cases
<ul>
  <li><strong>Logging and Debugging:</strong> To include variable or member names in log messages.</li>
  <li><strong>Argument Validation:</strong> To include parameter names in exception messages.</li>
  <li><strong>Refactoring:</strong> To ensure that renaming variables or members propagates correctly throughout your code.</li>
</ul>



































