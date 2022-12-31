# C\#

_A mostly reasonable approach to C#._

1. [Basic Rules](#basic-rules)
2. [Formatting](#formatting)
3. [Naming](#naming)

> __TIP:__ Use the [.editorconfig](.editorconfig) file to maintain consistency

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

## Formatting

### _Structure_

```csharp
internal class Worker
{
    private readonly IDependency _dependency;
    private int _counter;

    public bool SomeProperty { get; init; }

    public Worker(IDependency dependency)
    {
        _dependency = dependency;
        _counter = 0;
    }

    public void DoSomething()
    {
        _counter++;
        DoSomethingElse();
    }

    private void DoSomethingElse()
    {
        _dependency.SomethingElse();
        Log.Information("Counter is set to {counter}", _counter);
    }
}
```

1. Private fields
1. Public properties
1. Constructors
1. Public methods
1. Private methods

### _Prefer spaces for indentation_

### _Prefer an indent size of 4_

### _Prefer one class per file_

For simplicity and code navigation only define one class per file.

An exception to this is the expansion into generics.

DO:

```csharp
// Result.cs
namespace Helpers
{
    internal class Result
    { }

    internal class Result<TData> : Result
    { }
}
```

DON'T:

```csharp
// Result.cs
namespace Helpers
{
    internal class Result
    { }

    internal class Result<TData> : Result
    { }

    internal class ResultError
    { }

    internal class Retry
    { }
}
```

### _Avoid unused using directives_

Remove any unused using statements from the top of each file.

### _Prefer using directives to be placed oustide of the namespace_

DO:

```csharp
using System;

namespace Foo
{
    internal class Bar
    { }
}
```

DON'T:

```csharp
namespace Foo
{
    using System;

    internal class Bar
    { }
}
```

### _Prefer to sort using directives first by system then alphabetically_

```csharp
using System;
using System.Threading.Tasks;
using Bar;
using Foo;
using Foo.Baz;
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

#### _Constants - Screaming snake case_

```csharp
public class Foo
{
  private const string MY_CONSTANT = "*screams*";
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

### _Prefer to match namespace to the folder structure_

For simplicity and code navigation keep the namespace declaration consistent to the folder structure.
