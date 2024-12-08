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
</ul>
Keyboard shortcut 
https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf
Create new solution

```
dotnet new sln --name <Solution name>
```
