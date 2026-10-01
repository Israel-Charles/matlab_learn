# 03 - Data Types

MATLAB variables have a class that determines how their values are represented and what operations are available.

## Default Numeric Type

Ordinary numeric literals are stored as `double` by default.

```matlab
x = 4;
class(x)
```

returns:

```text
double
```

A scalar `double` normally uses 8 bytes.

Inspect details with:

```matlab
whos x
```

## Floating-Point Types

MATLAB provides:

```text
double
single
```

Example:

```matlab
a = 3.14;
b = single(3.14);
```

Inspect:

```matlab
class(a)
class(b)
```

## Signed Integer Types

```text
int8
int16
int32
int64
```

## Unsigned Integer Types

```text
uint8
uint16
uint32
uint64
```

## Integer Ranges

| Type | Range |
|---|---|
| `int8` | -128 to 127 |
| `uint8` | 0 to 255 |
| `int16` | -32768 to 32767 |
| `uint16` | 0 to 65535 |
| `int32` | -2^31 to 2^31 - 1 |
| `uint32` | 0 to 2^32 - 1 |
| `int64` | -2^63 to 2^63 - 1 |
| `uint64` | 0 to 2^64 - 1 |

MATLAB can report the exact limits:

```matlab
intmin("int8")
intmax("int8")

intmin("uint8")
intmax("uint8")
```

## Creating Typed Values

```matlab
a = int8(10);
b = uint8(200);
c = int32(5000);
d = single(3.14);
```

## Logical Type

MATLAB also supports:

```text
logical
```

Example:

```matlab
isReady = true;
isStopped = false;
```

## Inspecting Type and Memory

Use:

```matlab
class(x)
```

for the class.

Use:

```matlab
whos x
```

for:

- Name
- Size
- Bytes
- Class
- Attributes

## Choosing Numeric Types

Use `double` for most general numerical work unless there is a reason to choose something else.

Other types matter when:

- Working with images
- Interfacing with sensors
- Processing network packets
- Using embedded hardware
- Reducing memory use
- Matching external binary formats
- Using specialized algorithms

## Quick Reference

| Goal | Syntax |
|---|---|
| Check class | `class(x)` |
| Detailed info | `whos x` |
| Create single | `single(x)` |
| Create signed 8-bit | `int8(x)` |
| Create unsigned 8-bit | `uint8(x)` |
| Minimum integer value | `intmin("int16")` |
| Maximum integer value | `intmax("uint16")` |
| Create logical true | `true` |
| Create logical false | `false` |
