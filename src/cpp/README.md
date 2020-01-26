# C++

_A mostly reasonable approach to C++._

## Table of Contents

1. [Basic Rules](#basic-rules)
1. [Formatting](#formatting)

## Basic Rules

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
