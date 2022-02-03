# C# Vocabulary 

|**Git**|**C#**|**SQL**|**HTML**|**CSS**|**JavaScript**|
|---|---|---|---|---|---|
| <img src="https://edent.github.io/SuperTinyIcons/images/svg/git.svg" width="125" title="git"/>  | <img src="https://gistcdn.githack.com/johndward01/95c1d09de9e3707cfb4154989962376d/raw/f74007782421219d9e9ab4b6a27de2e172a8b714/csharp-logo.svg" width="125" title="c#"/> | <img src="https://www.vectorlogo.zone/logos/mysql/mysql-official.svg" width="125" title="mysql"/>  | <img src="https://edent.github.io/SuperTinyIcons/images/svg/html5.svg" width="125" title="HTML5" /> |  <img src="https://edent.github.io/SuperTinyIcons/images/svg/css3.svg" width="125" title="CSS3"/>  | <img src="https://edent.github.io/SuperTinyIcons/images/svg/javascript.svg" width="125" title="JavaScript" />|

### Table of Contents:

**[Git](#git)**<br>
**[C# Command-line](#csharp-command-line)**<br>
**[Value and Reference Types](#value-and-reference-types)**<br>
**[C# Variables](#csharp-variables)**<br>
**[C# Operators](#csharp-operators)**<br>
**[Selection Statements](#selection-statements)**<br>
**[C# Syntax Sugar](#csharp-syntax-sugar)**<br>
**[Iteration Statements & Loops](#iteration-statements-and-loops)**<br>
**[Methods](#methods)**<br>
**[Method Overloading](#method-overloading)**<br>
**[Arrays & Lists](#arrays-and-lists)**<br>
**[Classes](#classes)**<br>
**[Encapsulation](#encapsulation)**<br>
**[Inheritance](#inheritance)**<br>
**[Static Keyword](#static-keyword)**<br>
**[Abstract Classes](#abstract-classes)**<br>
**[Interfaces](#interfaces)**<br>
**[Factory Pattern](#factory-pattern)**<br>
**[LINQ](#linq)**<br>
**[Debugging](#debugging)**<br>
**[Exception Handling](#exception-handling)**<br>
**[Test Driven Development](#test-driven-development)**<br>
**[SQL Intro](#sql-intro)**<br>
**[SQL Joins](#sql-joins)**<br>
**[C# ORM and Dapper](#csharp-orm-and-dapper)**<br>
**[APIs and JSON](#apis-and-json)**<br>
**[IDE Parts: Google Chrome Inspector](#google-chrome-inspector)**<br>
**[HTML Intro](#html-intro)**<br>
**[CSS Intro](#css-intro)**<br>
**[JS Intro](#javascript-intro)**<br>
**[ASP.NET Core MVC](#mvc)**<br>

<br>
<br>
<br>

## Git

- ### **Version Control**: a means for managing your source code
- ### **Git:** A **[distributed version-control](https://en.wikipedia.org/wiki/Distributed_version_control) system (DVCS)** for tracking changes in [source code](https://en.wikipedia.org/wiki/Source_code) during [software development](https://en.wikipedia.org/wiki/Software_development). It is designed for coordinating work among [programmers](https://en.wikipedia.org/wiki/Programmer), but it can be used to track changes in any set of [files](https://en.wikipedia.org/wiki/Computer_file).
- ### **Github:** GitHub is where our **Remote repository** will live. Our computer is where our **Local repository** will live.
- ### **Commit:** A commit is the Git equivalent of a "save".
- `git init`: initializes a new repository in the current directory
- `git status`: The git status command displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven't, and which files aren't being tracked by Git
- `git clone <remote url goes here>`: puts a copy of the remote repository on our machine
- `git push`: push those changes to the remote repository
  - You must first use `git push -u origin main` BEFORE you can just use `git push`
- `git pull`: pulls the latest version of the remote repository to our machine.
- `git add <filename goes here>`: stages only the specified file
- `git add .`: stages all files in the directory so they are ready to commit
- `git commit -m "message goes here"`: commits the changes in the currently staged files and includes a message
- `git branch`: lists the branches in the repository
- `git branch <branchName>`: creates a new branch
- `git checkout <branchName>`: switches to a specific branch
- `git checkout –b <branchName>`: creates a new branch, and switches to that branch at the same time
- `git merge <branchName>`: merges a specific branch into the current branch
- `git pull`: downloads content from a remote repository and immediately update the local repository to match that content
- `git log`: display our commit history
- `git diff`: enables you to compare changes in the working directory against a previously committed version
- `git config --global user.email "YourEmailAddressGoesHere@gmail.com"`: sets the user email
- `git config --global user.name "Your Name"`: sets the user name

<br>
<br>
<br>

## Csharp Command-line

- ### **CLI**: The .NET Core command-line interface (CLI) is a new cross-platform toolchain for developing .NET applications. The CLI is a foundation upon which higher-level tools, such as Integrated Development Environments (IDEs), editors, and build orchestrators, can rest.
- ### **Solution file (.sln)** - a solution is a container used by Visual Studio to organize one or more related projects. When you open a solution in Visual Studio, it automatically loads all the projects the solution contains
- ### **Project file (.csproj)** – contains all the source code that is compiled. It also contains compiler settings and other configuration files
- `cd`: Command-line command to change directory
- `mkdir`: Command-line command to create a new folder (directory)
- `dotnet <command>`: dotnet is a tool for managing .NET source code and binaries. It exposes commands that perform specific tasks, such as dotnet build and dotnet run.
- `dotnet new`: Creates a new project, configuration file, or solution based on the specified template.
  - Example: `dotnet new console` ←- creates a new console application for us
- `dotnet build`: Builds a project and all of its dependencies.
- `dotnet run`: Runs source code without any explicit compile or launch commands.
- `dotnet sln`: The dotnet sln command provides a convenient way to add, remove, and list projects in a solution file.
- `dotnet test`: The dotnet test command is used to execute unit tests in a given project. The dotnet test command launches the test runner console application specified for a project. The test runner executes the tests defined for a unit test framework (for example, MSTest, NUnit, or xUnit) and reports the success or failure of each test. If all tests are successful, the test runner returns 0 as an exit code; otherwise, if any test fails, it returns 1. _If the project path is not specified, it defaults to the current directory._
  - Example: `dotnet test ~/projects/test1/test1.csproj`
- `dotnet clean`: The dotnet clean command cleans the output of the previous build. It's implemented as an MSBuild target, so the project is evaluated when the command is run. Only the outputs created during the build are cleaned. Both intermediate (_obj_) and final output (_bin_) folders are cleaned.

<br>
<br>
<br>

## Value and Reference Types

### **C# is a strongly AND statically typed object-oriented programming language.**

- ### **Strongly typed**: once a variable’s type is declared, it cannot change. (Although you can change its value)
- ### **Statically typed**: every variable must have a type at compile time.
- ### **Signed**: A signed integer is one with either a plus or minus sign in front. (It can be either positive or negative)
- ### **Unsigned**: integer is assumed to be positive
- ### **The Stack**: The Stack is used for static memory allocation. This is where Value Types are stored. It utilizes a LAST IN, FIRST OUT procedure.
- ### **The Heap**: The Heap is used for dynamic memory allocation. This is where Reference types are stored. Elements can be removed in any order from the heap.
- ### **Value Type**: A variable of a value type contains an instance of the type.
- ### **Reference Type**: A reference type contains a reference (\*pointer) to an instance of the type.

<br>
<br>
<br>

## Csharp Variables

- ### **Variable**: A variable is a container for storing value.
- ### **Constant**: A constant is a container for storing a value that never changes.
- ### **Variable Name**: A variable name is an identifier for the value stored in a particular location of computer memory
- ### **Data Type**: A data type specifies the size and type of variable values.
- ### **Camel Case**: The first letter of the first word will be lowercase, for the first time, but uppercase everytime after
  - Example:
  ```cs
  string camelCaseExample;
  ```
- ### **Pascal Case**: The first letter of every word is uppercase
  - Example:
  ```cs
  class PascalCaseExample;
  ```
  
  <br>
  <br>
  <br>
  
  ## Csharp Operators

- ### **Operator**: Operators are special symbols that perform actions on operands
  - Example : `2 + 2` ( **2** is the operand and **+** is the operator)
- ### **Operand**: The quantity on which the operation is performed.
- ### **Unary Operator**: An operator with only 1 operand.
  - Example: `x++`
  - Example: `!isTrue;`
  - Example: `--x;`
- ### **Binary Operator**: An operator with 2 operands.
  - Example: `1 + 1`; (**+** is the binary operator)
- ### **Ternary Operator**: An operator that requires 3 operands.
  ```cs
  bool answer = x < y ? true : false;  // ? is the ternary operator
  ```
- ### **Logical Operators**: Logical operators are used to combine two or more conditions or to complement the evaluation of the original condition in consideration.

- ### **Assignment Operator**: Assignment operators are used to assign a value to a variable. The left side operand of the assignment operator is a variable and the right side operand of the assignment operator is a value.
  > Note: The **value** on the right side must be of the same **data-type** as the variable on the left side, otherwise the compiler will raise an error.

<br>

```cs
int x = 100; // = is the simple assignment operator
int y = 200;

x += y; // same as long form x = x + y;
x -= y; // same as long form x = x - y;
x *= y; // same as long form x = x * y;
x /= y; // same as long form x = x / y;
x %= y; // same as long form x = x % y;
```

<br>
<br>

## Selection Statements

**Selection statements** enable you to branch to different sections of code, depending on one or more specified conditions.

### `if` : The if statement selects a statement to execute based on the value of a Boolean expression.

### `else`: An if statement with an else part selects one of the two statements to execute based on the value of a Boolean expression.

### `else if`: else if statements can be used after an if statement. It will only be executed when the if condition evaluates to false. So, either if or one of the else if statements can be executed, but not both.

### `switch/case`: A switch is a selection statement that chooses a single case section to execute based on if the value passed in matches the case conditional. The switch statement is a control statement different from the if statement because it evaluates a single expression against a list of possible cases. The switch statement is often used as an alternative to an if-else construct if a single expression is tested against three or more conditions.

### `default`: Specifies the code block to run if all else fails.

### `break`: Terminates the switch/case statement.

### `case`: Each case label specifies a pattern to compare to the match expression. If they match, control is transferred to the switch section that contains the first matching case label. If no case label pattern matches the match expression, control is transferred to the section with the default case label, if there's one. If there's no default case, no statements in any switch section are executed, and control is transferred outside the switch statement.

<br>
<br>
<br>

## Syntax Sugar

- CCR: Clear, Concise, and Readable
- Syntax: the grammar for programming
- Best Practices: This is syntax that is not required, but is considered the best thing to do.

