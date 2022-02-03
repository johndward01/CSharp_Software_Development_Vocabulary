# C# Software Development Vocabulary

| **Git**                                                                                        | **C#**                                                                                                                                                                    | **SQL**                                                                                           | **HTML**                                                                                            | **CSS**                                                                                          | **JavaScript**                                                                                                |
| ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------- |
| <img src="https://edent.github.io/SuperTinyIcons/images/svg/git.svg" width="125" title="git"/> | <img src="https://gistcdn.githack.com/johndward01/95c1d09de9e3707cfb4154989962376d/raw/f74007782421219d9e9ab4b6a27de2e172a8b714/csharp-logo.svg" width="125" title="c#"/> | <img src="https://www.vectorlogo.zone/logos/mysql/mysql-official.svg" width="125" title="mysql"/> | <img src="https://edent.github.io/SuperTinyIcons/images/svg/html5.svg" width="125" title="HTML5" /> | <img src="https://edent.github.io/SuperTinyIcons/images/svg/css3.svg" width="125" title="CSS3"/> | <img src="https://edent.github.io/SuperTinyIcons/images/svg/javascript.svg" width="125" title="JavaScript" /> |

Table of Contents:

**[Git](#git)**<br>
**[C# Command-line](#CSharp-command-line)**<br>
**[Value and Reference Types](#value-and-reference-types)**<br>
**[C# Variables](#CSharp-variables)**<br>
**[C# Operators](#CSharp-operators)**<br>
**[Selection Statements](#selection-statements)**<br>
**[C# Syntax Sugar](#CSharp-syntax-sugar)**<br>
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
**[C# ORM and Dapper](#CSharp-orm-and-dapper)**<br>
**[APIs and JSON](#apis-and-json)**<br>
**[IDE Parts: Google Chrome Inspector](#google-chrome-inspector)**<br>
**[HTML Intro](#html-intro)**<br>
**[CSS Intro](#css-intro)**<br>
**[JS Intro](#javascript-intro)**<br>
**[ASP.NET Core MVC](#ASPNET-Core-MVC)**<br>

<br>
<br>

# A Concise List of Vocabulary from the C# Software Engineering Review

<br>
<br>

## Git

- **Version Control**: a means for managing your source code
- **Git:** A **[distributed version-control](https://en.wikipedia.org/wiki/Distributed_version_control) system (DVCS)** for tracking changes in [source code](https://en.wikipedia.org/wiki/Source_code) during [software development](https://en.wikipedia.org/wiki/Software_development). It is designed for coordinating work among [programmers](https://en.wikipedia.org/wiki/Programmer), but it can be used to track changes in any set of [files](https://en.wikipedia.org/wiki/Computer_file).
- **Github:** GitHub is where our **Remote repository** will live. Our computer is where our **Local repository** will live.
- **Commit:** A commit is the Git equivalent of a "save".
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

## CSharp Command-line

- **CLI**: The .NET Core command-line interface (CLI) is a new cross-platform toolchain for developing .NET applications. The CLI is a foundation upon which higher-level tools, such as Integrated Development Environments (IDEs), editors, and build orchestrators, can rest.
- **Solution file (.sln)** - a solution is a container used by Visual Studio to organize one or more related projects. When you open a solution in Visual Studio, it automatically loads all the projects the solution contains
- **Project file (.csproj)** – contains all the source code that is compiled. It also contains compiler settings and other configuration files
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

**C# is a strongly AND statically typed object-oriented programming language.**

- **Strongly typed**: once a variable’s type is declared, it cannot change. (Although you can change its value)
- **Statically typed**: every variable must have a type at compile time.
- **Signed**: A signed integer is one with either a plus or minus sign in front. (It can be either positive or negative)
- **Unsigned**: integer is assumed to be positive
- **The Stack**: The Stack is used for static memory allocation. This is where Value Types are stored. It utilizes a LAST IN, FIRST OUT procedure.
- **The Heap**: The Heap is used for dynamic memory allocation. This is where Reference types are stored. Elements can be removed in any order from the heap.
- **Value Type**: A variable of a value type contains an instance of the type.
- **Reference Type**: A reference type contains a reference (\*pointer) to an instance of the type.

<br>
<br>
<br>

## CSharp Variables

- **Variable**: A variable is a container for storing value.
- **Constant**: A constant is a container for storing a value that never changes.
- **Variable Name**: A variable name is an identifier for the value stored in a particular location of computer memory
- **Data Type**: A data type specifies the size and type of variable values.
- **Camel Case**: The first letter of the first word will be lowercase, for the first time, but uppercase everytime after
- **Pascal Case**: The first letter of every word is uppercase

  <br>
  <br>
  <br>

  ## CSharp Operators

- **Operator**: Operators are special symbols that perform actions on operands
- **Operand**: The quantity on which the operation is performed.
- **Unary Operator**: An operator with only 1 operand.
- **Binary Operator**: An operator with 2 operands.
- **Ternary Operator**: An operator that requires 3 operands.
- **Logical Operators**: Logical operators are used to combine two or more conditions or to complement the evaluation of the original condition in consideration.

- **Assignment Operator**: Assignment operators are used to assign a value to a variable. The left side operand of the assignment operator is a variable and the right side operand of the assignment operator is a value.
  > Note: The **value** on the right side must be of the same **data-type** as the variable on the left side, otherwise the compiler will raise an error.

<br>
<br>
<br>

## Selection Statements

- **Selection statements** enable you to branch to different sections of code, depending on one or more specified conditions.

- `if` : The if statement selects a statement to execute based on the value of a Boolean expression.

- `else`: An if statement with an else part selects one of the two statements to execute based on the value of a Boolean expression.

- `else if`: else if statements can be used after an if statement. It will only be executed when the if condition evaluates to false. So, either if or one of the else if statements can be executed, but not both.

- `switch/case`: A switch is a selection statement that chooses a single case section to execute based on if the value passed in matches the case conditional. The switch statement is a control statement different from the if statement because it evaluates a single expression against a list of possible cases. The switch statement is often used as an alternative to an if-else construct if a single expression is tested against three or more conditions.

- `default`: Specifies the code block to run if all else fails.

- `break`: Terminates the switch/case statement.

- `case`: Each case label specifies a pattern to compare to the match expression. If they match, control is transferred to the switch section that contains the first matching case label. If no case label pattern matches the match expression, control is transferred to the section with the default case label, if there's one. If there's no default case, no statements in any switch section are executed, and control is transferred outside the switch statement.

<br>
<br>
<br>

## CSharp Syntax Sugar

- **CCR**: Clear, Concise, and Readable
- **Syntax**: the grammar for programming
- **Best Practices**: This is syntax that is not required, but is considered the best thing to do.
- **Syntax Sugar**: This is syntax that is not required and not necessarily best practice, but merely makes coding more convenient or concise.
- **Code Smell**: Any indicator in a program that a potentially deep-seated issue is present. (usually subjective and depends on factors including the particular language and experience)
- **Explicit Typing**: When you specifically say what each variable’s type is.
- **Inferred Typing**: Inferred typing is where the compiler defines the variable’s type by looking at what the variable’s value is and inferring what the most probable type is.

<br>
<br>
<br>

## Iteration Statements and Loops

- `while`: The while loop executes a statement or a block of statements while a specified Boolean expression evaluates to true. Because that expression is evaluated before each execution of the loop, a while loop executes zero or more times.
- `do-while`: The do-while loop executes a statement or a block of statements while a specified Boolean expression evaluates to true. Because that expression is evaluated after each execution of the loop, a do-while loop is guaranteed to execute at least one or more times.
- `for`: The “for” loop executes a statement or a block of statements while a specified Boolean expression evaluates to true.
  - the **initializer** - runs once at the beginning and sets an initial value to serve as a counter `int i = 0;`
  - the **conditional** - evaluates before each iteration to determine whether the loop should continue executing `i < 10;`
  - the **increment** - after the body of the loop is executed, the increment updates the value of the counter `i++;`
  - and the **body** - the is the block of code the loop will execute. We also call this the scope of the loop `{ }`
- `foreach`: A “foreach” loop executes a statement or a block of statements for each element in an instance of the type that implements the `System.Collections.IEnumerable;`

<br>
<br>
<br>

## Methods

- **Method**: A method, or function, helps you separate your code into modules that perform a given task... You execute this code by calling the Method. In C# a method consists of a few things:
- **Access Modifiers**: Access modifiers are keywords used to specify the declared accessibility of a member or a type.
- **Return Type**: the type returned by the method, or void when not returning anything
  - `void`: void is the absence of a return type
- **Name**: a descriptive method name using PascalCase
  - **PascalCase**: every first letter of every word is capitalized
- **Parameters**: an optional list of variables to be passed to the method
- **Scope/Body**: the block of code to be executed when the method is called
- **Argument**: the value you pass into the function when it is being called
- **Abstraction**: Abstraction is used to hide the implementation details and display only what's essential

> Note: Abstraction is one of the 4 pillars of Object Oriented Programming! (OOPs **A** PIE)

<br>
<br>
<br>

## Method Overloading

- **Method Overloading**: When multiple methods share the same name but have a different signature
  > Note: The number of parameters, the order of the parameters, and the data types of the parameters change the signature
- **Signature**: A method signature is a unique identification of a method for the C# compiler. The signature consists of a method name and the type and kind (value, reference, or output) of each of its formal parameters. Method signature does not include the return type.

<br>
<br>
<br>

## Arrays and Lists

- **Arrays**: Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value. In C#, arrays are actually objects, and not just addressable regions of contiguous memory as in C and C++. Therefore, using dot notation, you have access to the properties and methods of the abstract Array class.
- **Lists**: The C# List class represents a collection of strongly typed objects that can be accessed by index. Lists provide a more flexible way to work with groups of objects. Unlike arrays, the group of objects you work with can grow and shrink dynamically as the needs of the application change. For some collections, you can assign a key to any object that you put into the collection so that you can quickly retrieve the object by using the key.

<br>
<br>
<br>

## Classes

- **Functional Programming**: Functional programming allows building a program using mathematical functions. In other words, it binds the program into a purely mathematical function. Using functional programming, the developer can build a program as a combination of separate mathematical functions.
- **Object-Oriented Programming**: Object-oriented programming (OOP) is a programming paradigm based on the concept of "objects", which can contain data and code: data in the form of fields (often known as attributes or properties), and code, in the form of procedures (often known as methods).
- **Class**: Classes are the cornerstone of Object-Oriented Programming. They help you take all the properties and behaviors of an object in your program, and combine them into a single object, then re-use that object wherever you need it in your program. Using classes in your code enables you to implement Encapsulation, Abstraction, Inheritance, and Polymorphism.
- **Object**: An object is defined as a singular instance of a class or type. A class can be thought of as a blueprint, a template or a cookie cutter. A class describes an object, but it is not that object.
- **Class Members**: Classes have members sort of like how methods have variables; however, classes are not only limited to variables. Examples:
  - **Fields** - a variable of any type that is declared directly in a class or struct.
  - **Properties** - a member that provides a mechanism to read, write, or compute the value of a private field.
  - **Methods** - a code block that contains a series of statements to execute.
  - **Constructors** - Whenever a class or struct is created, its constructor is called.
- **Dot Notation**: The way we access the methods and properties of a class is with the ( . ) Dot operator, Dot Notation, or Class Member Access Operator.

<br>
<br>
<br>

## Encapsulation

- **Encapsulation**: groups of related properties, methods, and other members are treated as a single unit or object.
- `public` - access modifier makes the member accessible from outside of the class
- `private` - makes members accessible only from within the class it was created in and hides the member from the outside
- `protected` - the member can only be accessed by code in the same class or in a derived class
- `internal` - the member can be accessed by any code in the same assembly, but not from another assembly
- `protected internal` - the member can be accessed by any code in the same assembly, or by any derived class in another assembly

> Note: Encapsulation is also called information hiding.

> Note: Encapsulation is one of the 4 pillars of Object Oriented Programming! (OOPs A PI**E**)

<br>
<br>
<br>

## Inheritance

- **Inheritance**: Inheritance enables you to create new classes that reuse, extend, and modify the behavior that is defined in other classes.

> Note: Inheritance is one of the 4 pillars of Object Oriented Programming! (OOPs A P**I**E)

<br>
<br>
<br>

## Static Keyword

- **Static**: The Static Modifier means that it (the property, method or other class member) belongs to the type/class itself and not to the object instance.

<br>
<br>
<br>

## Abstract Classes

- **Abstract Class**: An abstract class acts as a stubbed-out template class that other classes will derive from and use as an incomplete base. The derived class will define its own way to complete the stubbed-out template provided by the abstract class.

> Note: The purpose of an abstract class is to define some common behavior that can be inherited by multiple subclasses, without implementing the entire class.

- `abstract`: The modifier indicates that the thing being modified has a missing or incomplete implementation. The abstract modifier can be used with classes, methods, properties, indexers, and events. Use the abstract modifier in a class declaration to indicate that a class is intended only to be a base class of other classes, not instantiated on its own. Members marked as abstract must be implemented by non-abstract classes that derive from the abstract class.

- `override`: The override modifier is required to extend or modify the abstract or virtual implementation of an inherited method, property, indexer, or event.
- `virtual`: The virtual keyword is used to modify a method, property, indexer, or event declaration and allow for it to be overridden in a derived class.

> Note: Method Overloading gives us static **polymorphism**

> Abstract Classes give us dynamic **polymorphism**

> Note: Polymorphism is one of the 4 pillars of Object Oriented Programming! (OOPs A **P**IE)

<br>
<br>
<br>

## Interfaces

- **Interface**: An interface contains definitions for a group of related functionalities that a non-abstract class or a struct must implement.

> Note: Interfaces in C# provide another way to achieve runtime polymorphism.

<br>
<br>
<br>

## Factory Pattern

- **Factory Pattern**: The Factory Design Pattern is a programming concept that allows one class, separate to the main program or “client”, to create new objects. By using the factory pattern to encapsulate object creation, you have one location to make changes to the way objects are instantiated. The way this is accomplished is by programming to an interface or an abstract class. When we program to an interface or ABS class, the program doesn’t care what type of object we wish to create as long as it implements the interface or inherits from the ABS class.

> Note: We also use the **Repository Design Pattern in ASP.NET Core MVC!**

<br>
<br>
<br>

## LINQ

- **LINQ**: Language-Integrated Query (LINQ) is the name for a set of technologies based on the integration of query capabilities directly into the C# language.

> Note: You need to add the using directive using System.Linq; in order to access the LINQ Extension methods

<br>

**Common LINQ Methods**:

- `Where()`- Filters a sequence of values based on a predicate.
- `Select()`- Projects each element of a sequence into a new form.
- `OrderBy()`- Sorts the elements of a sequence in ascending order.
- `Sum()`- Computes the sum of a sequence of numeric values.
- `Average()`- Computes the average of a sequence of numeric values.
- `Count()`- Returns the number of elements in a sequence.
- `Min()`- Returns the minimum value in a sequence of values.
- `Max()`- Returns the maximum value in a sequence of values.
- `Take()`- Returns a specified number of contiguous elements from the start of a sequence.
- `Append()`- Appends a value to the end of the sequence.
- `GroupBy()`- Groups the elements of a sequence according to a specified key selector function and creates a result value from each group and its key.
- `ThenBy()`- Performs a subsequent ordering of the elements in a sequence in ascending order.

<br>
<br>
<br>

## Debugging

- **Debugging**: Debugging means to run your code step by step in a debugging tool like Visual Studio, to find the exact point where you made a programming mistake. You then understand what corrections you need to make in your code, and debugging tools often allow you to make temporary changes so you can continue running the program.
- **Compile Time Errors**: A compile-time error is an error that shows up when you’re writing code, it will be accompanied by a red squiggly and show up in the error window.
- **Runtime Error**: A Runtime error is an error that occurs while your application is running. While in debug mode this will show up as an exception.
- **Logical Error**: A logical error is an error that while you can still run your program and it will not crash, you won’t be getting the results you might expect.
- **Breakpoints**: Breakpoints are one of the most important debugging techniques in your developer's toolbox. You set breakpoints wherever you want to pause debugger execution.
- **Step Into**: To stop on each statement when you're debugging, use Debug > Step Into, or select F11.
  - The debugger steps through code statements, not physical lines. For example, an if clause can be written on one line.
- **Step Out**: Step Out continues running code and suspends execution when the current function returns. The debugger skips through the current function.
- **Step Over**: If the current line contains a function call, Step Over runs the code and then suspends execution at the first line of code after the called function returns.

<br>
<br>
<br>

## Exception Handling

- **Exception Handling**: The C# language's exception handling features help you deal with any unexpected or exceptional situations that occur when a program is running. Exception handling uses the try, catch, and finally keywords to try actions that may not succeed, to handle failures when you decide that it's reasonable to do so, and to clean up resources afterward. Exceptions can be generated by the common language runtime (CLR), by .NET or third-party libraries, or by application code. Exceptions are created by using the throw keyword.
- `try`: A try block is used by C# programmers to partition code that might be affected by an exception.
- `catch`: Associated catch blocks are used to handle any resulting exceptions.
- `finally`: A finally block contains code that is run regardless of whether or not an exception is thrown in

<br>
<br>
<br>

## Test Driven Development

- **Test Driven Development**: TDD is a process in which we write our tests first and those tests are used to drive the design of our code or application.
- **Red, Green, Refactor Process**:

  - **Red**: We write the test and then watch it fail (it fails because the code needed in order for the test to pass hasn’t been written yet!). We create a test that will fail on purpose so that we know with a degree of confidence that our tests will fail when expected to - making it red
  - **Green**: Now we write code in our software or application so that our test will pass - making it green
  - **Refactor**: Here we change the passing code we wrote (the code that made our test pass) without changing the behavior of the code itself. We want our code to still behave as we expect. This allows us to improve code readability and possibly reduce complexity.

- **xUnit Syntax**:
  - `[Fact]`: xUnit uses the [Fact] attribute to denote a parameterless unit test, which tests invariants in your code
  - `[Theory]`: represents a suite of tests that execute the same code but have different input arguments.

> Note: `[Fact]`s typically don't contain any parameters; In contrast, the [Theory] attribute denotes a parameterized test that is true for a subset of data. That data can be supplied in a number of ways, but the most common is with an `[InlineData]` attribute.

<br>
<br>
<br>

## SQL Intro

- `SELECT`: The SELECT statement in SQL is used to read, or query, existing records in your database.
- `INSERT`: The INSERT statement in SQL is used to create a new record to your database.
- `UPDATE`: The UPDATE statement in SQL is used to modify existing records in your database.
- `DELETE`: The DELETE statement in SQL is used to remove existing records in your database.

> Note: Without the WHERE clause in the UPDATE statement, every record in our table will be updated based on the key, value pairs provided.

> Note: Without the WHERE clause in the DELETE statement, every record in our table will be deleted.

<br>
<br>
<br>

## SQL JOINS

- `JOIN`: A JOIN clause is used to combine rows from two or more tables, based on a related column between them.
- `INNER JOIN`: The INNER JOIN statement in SQL gets only the records where a match occurs on both tables.
- `LEFT JOIN`: The LEFT JOIN statement in SQL gets all the records from the left table and only records from the right table where a match occurs.
- `RIGHT JOIN`: The RIGHT JOIN statement in SQL gets all the records from the right table and only records from the left table where a match occurs.
- `LEFT EXCLUDING JOIN`: The LEFT EXCLUDING JOIN statement in SQL gets all the records from the left table where a match does not occur on the right table.
- `RIGHT EXCLUDING JOIN`: The RIGHT EXCLUDING JOIN statement in SQL gets all the records from the right table where a match does not occur on the left table.
- `FULL OUTER EXCLUDING JOIN`: The FULL OUTER EXCLUDING JOIN statement in SQL gets all the records from both the left and right tables where a match does not occur in either table.

> Note: Although Full Outer Excluding Join is available to you, there are very few cases where this Join will be required.

<br>
<br>
<br>

## CSharp ORM and Dapper

- **Object Relational Mappers (ORMs)**: ORMs are the plumbers of the programming world. They help get data out of and back into databases from our data models. Additionally, ORM's like Dapper will handle parameterizing your SQL statements for you and make it very easy to fire a SQL query against a database and get the result mapped to C# domain class.
- **SQL Injection**: SQL Injection is the "injection" of unexpected or malicious code into SQL statements.
- **Parameterized Statements**: Parameterized statements allow you to abstract your statement from your parameters. Parameterized statements will sanitize your data by escaping any dangerous characters and performing any parsing or optimization necessary.
- **Dapper**: Dapper is a .NET compatible, NuGet library ORM that you can add to your project that will extend your IDbConnection interface.

> Note: Dapper has no DB specific implementation details; it works across SQLite, Oracle, MySQL, PostgreSQL, and SQL Server, to name a few.

- **Query Method**: The Dapper Query is designed for any database reads, like SELECT. Query returns an IEnumerable, so a select statement will return one T for each record in the database.
- **Execute Method**: The Dapper Execute is designed for any database writes, like INSERT, UPDATE, and DELETE. Execute only returns the number of records affected, so it can be ignored if you aren't interested in the affected records.

<br>
<br>
<br>

## APIs and JSON

- **API**: API stands for Application Programming Interface. It defines how two pieces of software will communicate with each other.
- **JSON**: JSON is a text format that is completely language independent but uses conventions that are familiar to programmers of the C-family of languages, including C, C++, C#, Java, JavaScript, Perl, Python, and many others.
- **RESTful API**: A RESTful API is an application program interface (API) that uses HTTP requests to GET, PUT, POST and DELETE data.
- **HTTP Status Codes**:
  - **1xx**: Informational
  - **2xx**: Success This class of status code indicates that the client's request was successfully received, understood, and accepted.
  - **3xx**: Redirection The client must take additional action to complete the request.
  - **4xx**: Client Error (404)
  - **5xx**: Server Error The server failed to fulfill an apparently valid request
- **HTTP**: Hyper Text Transport Protocol: (HyperText Transfer Protocol) The communications protocol used to connect to Web servers on the Internet or on a local network (intranet). The primary function of HTTP is to establish a connection with the server and send HTML pages back to the user's browser. It is also used to download data from the server either to the browser or to any requesting application that uses HTTP.
- **HTTPS**: HTTPS (HTTP Secure) is the encrypted version of HTTP (see HTTPS).

<br>
<br>
<br>

## Google Chrome Inspector

- **Chrome DevTools**: Chrome DevTools is a set of web developer tools built directly into the Google Chrome browser. DevTools can help you edit pages on-the-fly and diagnose problems quickly, which ultimately helps you build better websites, faster.
- **Elements Panel**: View and change the DOM and CSS.
- **Console Panel**: View messages and run JavaScript from the Console.
- **Sources Panel**: Debug JavaScript, persist changes made in DevTools across page reloads, save and run snippets of JavaScript, and save changes that you make in DevTools to disk.
- **Network Panel**: View and debug network activity.
- **Performance Panel**: Find ways to improve load and runtime performance.
- **Memory Panel**: Fix Memory Problems and work with the JavaScript CPU Profiler.
- **Application Panel**: Inspect all resources that are loaded, including IndexedDB or Web SQL databases, local and session storage, cookies, Application Cache, images, fonts, and stylesheets.
- **Security Panel**: Debug mixed content issues, certificate problems, and more.

<br>
<br>
<br>

## HTML Intro

- **HTML**: The HyperText Markup Language, or HTML is the standard markup language for documents designed to be displayed in a web browser.
- **HyperText**: Hypertext is text displayed on a computer display or other electronic devices with references ([hyperlinks](https://en.wikipedia.org/wiki/Hyperlink)) to other text that the reader can immediately access. Hypertext documents are interconnected by hyperlinks, which are typically activated by a mouse click, keypress set, or screen touch.
- **HTML Element**: An HTML element is defined by a start tag, some content, and an end tag.
- **HTML Attribute**: HTML attributes provide additional information about HTML elements.
- **Block Level Elements**: HTML (Hypertext Markup Language) elements historically were categorized as either "block-level" elements or "inline-level" elements. Since this is a presentational characteristic it is nowadays specified by CSS in the Flow Layout. A Block-level element occupies the entire horizontal space of its parent element (container), and vertical space equal to the height of its contents, thereby creating a "block".
- **Inline Level Elements**: An inline element does not start on a new line. An inline element only takes up as much width as necessary.

> Note: All HTML documents must start with a document type declaration: `<!DOCTYPE html>`.

> Note: The HTML document itself begins with `<html>` and ends with `</html>`.

> Note: The visible part of the HTML document is between `<body>` and `</body>`.

<br>
<br>
<br>

## CSS Intro

- **CSS**: Cascading Style Sheets (CSS) is a style sheet language used for describing the presentation of a document written in a markup language such as HTML.
- **Inline CSS**: Using an inline style is one of the ways to insert a style sheet. With an inline style, a unique style is applied to a single element. In order to use an inline style, add the style attribute to the relevant tag.
- **Embedded/Internal CSS**: Internal styles are defined within the style element, inside the head section of an HTML page.
- **External CSS**: With this method, all styling rules are contained in a single text file, which is saved with the .css extension. This CSS file is then referenced in the HTML using the tag. The element goes inside the head section.
- **CSS Element Selector**: The element selector selects HTML elements based on the element name.
- **CSS ID Selector**: The id selector uses the id attribute of an HTML element to select a specific element. The id of an element is unique within a page, so the id selector is used to select one unique element. To select an element with a specific id, write a hash `#` character, followed by the id of the element.
- **CSS Class Selector**: The Class selector selects HTML elements with a specific class attribute. To select elements with a specific class, write a period `.` character, followed by the class name.
- **CSS Universal Selector**: The universal selector `*` selects all HTML elements on the page.

<br>
<br>
<br>

## JavaScript Intro

- **JavaScript**: JavaScript is a dynamic programming language that's used for web development, in web applications, for game development, and lots more. It allows you to implement dynamic features on web pages that cannot be done with only HTML and CSS.
- **Duck Typing**: Duck Typing is a feature in javascript where the variable attempts to behave in the manner it is used. Duck Typing refers to a duck test program. You will test something, if it quacks like a duck, and flies like a duck, it is a duck. If a method responds to any given object call, it passes the “Duck Test”.
- **Truthy and Falsy**: In Javascript, all values have an inherit boolean value assigned to it. A falsy value is a value that is considered false when encountered in a Boolean context. We can use these in if statements.
- **The Document Object Model (DOM)**: The Document Object Model (DOM) is a programming interface for web documents. It represents the page so that programs can change the document structure, style, and content. The DOM represents the document as nodes and objects; that way, programming languages can interact with the page.

> Note: The DOM is not a programming language, but without it, the JavaScript language wouldn't have any model or notion of web pages, HTML documents, SVG documents, and their component parts. The document as a whole, the head, tables within the document, table headers, text within the table cells, and all other elements in a document are parts of the document object model for that document. They can all be accessed and manipulated using the DOM and a scripting language like JavaScript.

<br>
<br>
<br>

## ASPNET Core MVC

- **ASP.NET Core**: 
- **MVC**: 
