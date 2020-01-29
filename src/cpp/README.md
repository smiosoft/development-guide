# C++

_A mostly reasonable approach to C++._

1. [Basic Rules](#basic-rules)
1. [Formatting](#formatting)
1. [Naming](#naming)

## Basic Rules

### CPP_BR1: _Prefer `auto` keyword_

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

### CPP_FORM1: _Prefer spaces and indent 2 spaces at a time_

Spaces are preferred to allow consistent alignment columns cross-platform.

### CPP_FORM2: _Prefer to align related code chunks with the least amount of indents_

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

### CPP_NAME1: _Casing_

#### CPP_NAME1.1: _File - Pascal case_

```txt
MyFile.cpp
```

#### CPP_NAME1.2: _Class - Pascal case_

```cpp
class MyClass {...}
```

#### CPP_NAME1.3: _Method - Pascal case_

```cpp
class Foo
{
public:
  void MyMethod();
}
```

#### CPP_NAME1.4: _Property(Public) - Pascal case_

```cpp
class Foo
{
public:
  int MyPublicProperty;
}
```

#### CPP_NAME1.5: _Property(Private) - Lower snake case_

```cpp
class Foo
{
private:
  int _my_private_property;
}
```

#### CPP_NAME1.6: _Parameter - Lower snake case_

```cpp
void Foo::Bar(int my_parameter) {...}
```

#### CPP_NAME1.7: _Variable - Lower snake case_

```cpp
void Foo::Bar()
{
  auto my_variable = 1337;
}
```

### CPP_NAME2: _Avoid Hungarian Notation_

The compiler and IDE can provide type information, prefixing this information is redundant and gets in the way of reading the code.

DO:

```cpp
std::string username = "batman";
```

DON'T:

```cpp
std::string strUsername = "batman";
```
