# C++

_A mostly reasonable approach to C++._

## Table of Contents

1. [Basic Rules](#basic-rules)
1. [Formatting](#formatting)
1. [Naming](#naming)

## Basic Rules

### CPP_BR1: _Prefer auto keyword_

Use `auto` to avoid redundant reputation of type names and simplify generic code.

#### DO

```cpp
auto age = GetAge();
```

#### DON'T

```cpp
int age = GetAge();
```

## Formatting

### CPP_FORM1: _Prefer spaces and indent 2 spaces at a time_

Spaces are preferred to allow consistent alignment columns cross-platform.

### CPP_FORM2: _Prefer to align related code chunks with the least amount of indents_

#### DO

```cpp
Foo device;
device.id        = 1;
device.instance  = GetInstance();
device.style     = FOO | BAR | BAZ;
```

```cpp
Device*           GetDevice();
DeviceContext*    GetDeviceContext();
RenderTargetView* GetRenderTarget();
```

#### DON'T

```cpp
Foo device;
device.id = 1;
device.instance = GetInstance();
device.style = FOO | BAR | BAZ;
```

```cpp
Device* GetDevice();
DeviceContext* GetDeviceContext();
RenderTargetView* GetRenderTarget();
```

## Naming
