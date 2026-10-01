# 04 - Type Conversion and Integer Arithmetic

Changing a variable's numeric type can change the represented value.

This matters when data must fit into a fixed numeric range.

## Direct Conversion

```matlab
x = 55.343;

a = int8(x);
b = uint8(x);
c = single(x);
```

## `cast`

Another option is:

```matlab
y = cast(x, "single");
```

This is useful when the destination type is stored as text or derived programmatically.

## Floating-Point to Integer Conversion

When converting floating-point values to integer types, MATLAB rounds to an integer value.

Example:

```matlab
x = 55.7;
y = int8(x);
```

Do not assume the decimal portion is simply discarded.

## Saturation

When a converted value is outside the destination integer range, MATLAB saturates to the nearest representable endpoint.

```matlab
uint8(-45)
```

returns:

```text
0
```

```matlab
uint8(300)
```

returns:

```text
255
```

because `uint8` is restricted to values from 0 through 255.

## Integer Arithmetic Can Saturate

```matlab
a = uint8(150);
b = uint8(200);

c = a + b;
```

Mathematically:

```text
150 + 200 = 350
```

but `uint8` cannot represent 350.

The result saturates at 255.

## Convert Before Arithmetic When Appropriate

For general numerical calculations:

```matlab
c = double(a) + double(b);
```

Now the mathematical value 350 can be represented.

## Averaging Integer Values

This pattern can be risky:

```matlab
a = uint8(150);
b = uint8(200);

averageValue = (a + b)/2;
```

The addition can saturate before division occurs.

A safer general calculation is:

```matlab
averageValue = (double(a) + double(b))/2;
```

or:

```matlab
averageValue = mean(double([a b]));
```

## Why This Matters

Type-related errors are especially common in:

- Image processing
- Sensors
- Embedded systems
- Binary file formats
- Communications
- Hardware interfaces

Always know:

1. The current data type
2. The representable range
3. The desired output type
4. Whether intermediate operations can overflow or saturate

## Quick Reference

| Goal | Syntax |
|---|---|
| Convert to double | `double(x)` |
| Convert to single | `single(x)` |
| Convert to signed integer | `int8(x)`, `int16(x)`, etc. |
| Convert to unsigned integer | `uint8(x)`, `uint16(x)`, etc. |
| Generic conversion | `cast(x, "single")` |
| Check class | `class(x)` |
| Inspect limits | `intmin(...)`, `intmax(...)` |
