# C\#

_A mostly reasonable approach to C#._

1. [Basic Rules](#basic-rules)
1. [Formatting](#formatting)

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
