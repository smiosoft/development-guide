# C\#

_A mostly reasonable approach to C#._

1. [Basic Rules](#basic-rules)
2. [Formatting](#formatting)
3. [Naming](#naming)

## Basic Rules

### _Prefer `var` keyword_

Use `var` to avoid redundant reputation of type names and simplify generic code.

DO:

```csharp
var age = GetAge();
```

DON'T:

```csharp
int age = GetAge();
```

### _Avoid comments_

Use comments sparingly and only when there is unusual behaviour that needs explanation; focus on the why and what of a code block and not the how.

Avoid line-by-line commentary; code should be self-documenting and easy for other developers to understand. Comments simply get in the way of reading code, add an unnecessary overhead during refactoring, and very easily fall out-of-date.

### _Avoid unused using statements_

Remove any unused using statements from the top of each file.

## Formatting

### _Structure_

```csharp
using App.Logging;
using System;

namespace App
{
    internal class Worker
    {
        private readonly ILogger _logger;
        private int _counter;

        public bool IsWoking => true;

        public Worker(ILogger logger)
        {
            _logger = logger;
            _counter = 0;
        }

        public void DoSomething()
        {
            Console.WriteLine("I'm working...");
            _counter++;
            LogAction();
        }

        private void LogAction()
        {
            _logger.Log($"Counter is set to {_counter}.");
        }
    }
}
```

1. Private fields
1. Public properties
1. Constructors
1. Public methods
1. Private methods

### _Prefer tabs for indentation_

Tabs are preferred to allow developers to set their own indentation size.

### _Prefer one class per file_

For simplicity and code navigation only define one class per file.

### _Prefer to sort using statements alphabetically_

```csharp
using Foo;
using Foo.Bar;
using System;
using System.Threading.Tasks;
```

## Naming

### _Casing_

#### _File - Pascal case_

```txt
MyFile.cs
```

#### _Class - Pascal case_

```csharp
public class MyClass {...}
```

#### _Method - Pascal case_

```csharp
public class Foo
{
  public void MyMethod() {...}
}
```

#### _Property - Pascal case_

```csharp
public class Foo
{
  public int MyProperty { get; set; }
}
```

#### _Field - Lower camel case with leading underscore_

```csharp
public class Foo
{
  private int _myField;
}
```

#### _Parameter - Lower camel case_

```csharp
public void Foo(int myParameter) {...}
```

#### _Variable - Lower camel case_

```csharp
public void Foo()
{
  var myVariable = 413;
}
```

### _Avoid Hungarian Notation_

The compiler and IDE can provide type information, prefixing this information is redundant and gets in the way of reading the code.

DO:

```csharp
var username = "batman";
```

DON'T:

```csharp
var strUsername = "batman";
```

### _Prefer to match class name and file name_

For simplicity and code navigation keep the class name and the file name the same.
