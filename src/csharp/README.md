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

## Formatting

### CS_FORM1: _Prefer tabs for indentation_

Tabs are preferred to allow developers to set their own indentation size.

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
