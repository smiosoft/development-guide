# C\#

_A mostly reasonable approach to C#._

1. [Basic Rules](#basic-rules)
1. [Formatting](#formatting)
1. [Naming](#naming)

## Basic Rules

### CS_BR1: _Prefer `var` keyword_

Use `var` to avoid redundant reputation of type names and simplify generic code.

DO:

```csharp
var age = GetAge();
```

DON'T:

```csharp
int age = GetAge();
```

### CS_BR2: _Avoid comments_

Use comments sparingly and only when there is unusual behaviour that needs explanation; focus on the why and what of a code block and not the how.

Avoid line-by-line commentary; code should be self-documenting and easy for other developers to understand. Comments simply get in the way of reading code, add an unnecessary overhead during refactoring, and very easily fall out-of-date.

### CS_BR3: _Avoid unused using statements_

Remove any unused using statements from the top of each file.

## Formatting

### CS_FORM1: _Structure_

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

### CS_FORM2: _Prefer tabs for indentation_

Tabs are preferred to allow developers to set their own indentation size.

### CS_FORM3: _Prefer one class per file_

For simplicity and code navigation only define one class per file.

### CS_FORM4: _Prefer to sort using statements alphabetically_

DO:

```csharp
using Foo;
using Foo.Bar;
using System;
using System.Threading.Tasks;
```

DON'T:

```csharp
using System.Threading.Tasks;
using Foo.Bar;
using System;
using Foo;
```

## Naming

### CS_NAME1: _Casing_

#### CS_NAME1.1: _File - Pascal case_

```txt
MyFile.cs
```

#### CS_NAME1.2: _Class - Pascal case_

```csharp
public class MyClass {...}
```

#### CS_NAME1.3: _Method - Pascal case_

```csharp
public class Foo
{
  public void MyMethod() {...}
}
```

#### CS_NAME1.4: _Property - Pascal case_

```csharp
public class Foo
{
  public int MyProperty { get; set; }
}
```

#### CS_NAME1.5: _Field - Lower camel case with leading underscore_

```csharp
public class Foo
{
  private int _myField;
}
```

#### CS_NAME1.6: _Parameter - Lower camel case_

```csharp
public void Foo(int myParameter) {...}
```

#### CS_NAME1.7: _Variable - Lower camel case_

```csharp
public void Foo()
{
  var myVariable = 413;
}
```

### CS_NAME2: _Avoid Hungarian Notation_

The compiler and IDE can provide type information, prefixing this information is redundant and gets in the way of reading the code.

DO:

```csharp
var username = "batman";
```

DON'T:

```csharp
var strUsername = "batman";
```

### CS_NAME3: _Prefer class name and file name to match_

For simplicity and code navigation keep the class name and the file name the same.
