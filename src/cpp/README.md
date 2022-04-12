# C++

_A mostly reasonable approach to C++._

1. [Basic Rules](#basic-rules)
2. [Formatting](#formatting)
3. [Naming](#naming)

## Basic Rules

### _Prefer `auto` keyword_

Use `auto` to avoid redundant reputation of type names and simplify generic code.

DO:

```cpp
auto age = GetAge();
```

DON'T:

```cpp
int age = GetAge();
```

## Formatting

### _Prefer spaces and indent 2 spaces at a time_

Spaces are preferred to allow consistent alignment across different environments.

### _Prefer to align related code chunks with the least amount of indents_

DO:

```cpp
Foo device;
device.id        = 1;
device.instance  = CreateInstance();
device.style     = FOO | BAR | BAZ;
```

DON'T:

```cpp
Foo device;
device.id = 1;
device.instance = CreateInstance();
device.style = FOO | BAR | BAZ;
```

## Naming

### _Casing_

#### _File - Pascal case_

```txt
MyFile.cpp
```

#### _Class - Pascal case_

```cpp
class MyClass {...}
```

#### _Method - Pascal case_

```cpp
class Foo
{
public:
  void MyMethod();
}
```

#### _Property - Pascal case_

```cpp
class Foo
{
public:
  int MyPublicProperty;
}
```

#### _Field - Lower snake case with trailing underscore_

```cpp
class Foo
{
private:
  int my_private_field_;
}
```

#### _Parameter - Lower snake case_

```cpp
void Foo::Bar(int my_parameter) {...}
```

#### _Variable - Lower snake case_

```cpp
void Foo::Bar()
{
  auto my_variable = 1337;
}
```

### _Avoid Hungarian Notation_

The compiler and IDE can provide type information, prefixing this information is redundant and gets in the way of reading the code.

DO:

```cpp
std::string username = "batman";
```

DON'T:

```cpp
std::string strUsername = "batman";
```
