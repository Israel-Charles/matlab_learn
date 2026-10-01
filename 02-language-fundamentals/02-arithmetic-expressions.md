# 02 - Arithmetic Expressions

MATLAB expressions follow programming syntax rather than handwritten mathematical notation.

## Basic Operators

| Operation | MATLAB |
|---|---|
| Addition | `+` |
| Subtraction | `-` |
| Multiplication | `*` |
| Division | `/` |
| Power | `^` |

Example:

```matlab
x = 4;

a = x + 2;
b = x - 2;
c = 3*x;
d = x/2;
e = x^2;
```

## Explicit Multiplication

MATLAB requires the multiplication operator.

Incorrect:

```matlab
5x
```

Correct:

```matlab
5*x
```

Likewise:

```matlab
y = 2*x + 3;
```

not:

```text
y = 2x + 3
```

## Parentheses

Use parentheses to make mathematical grouping explicit.

```matlab
y = (x + 1) / (x - 1);
```

This differs from:

```matlab
y = x + 1/x - 1;
```

## Powers

```matlab
x = 4;
y = x^5;
```

For scalars, `x^5` is the standard way to compute a power.

## Built-In Mathematical Functions

Example:

```matlab
x = 4;
y = sqrt(x^2 + 3*x + 10);
```

Common functions include:

```matlab
sqrt(x)
abs(x)
sin(x)
cos(x)
tan(x)
exp(x)
log(x)
log10(x)
```

## `sqrt` and `sqrtm`

These are different operations.

Element-wise square root:

```matlab
A = [1 4;
     9 16];

sqrt(A)
```

returns:

```text
1 2
3 4
```

Matrix square root:

```matlab
sqrtm(A)
```

has a linear-algebra meaning and is not the same operation (`sqrtm(A)` calculates the principal matrix square root, meaning it finds a matrix X such that X × X = A).

## Operator Precedence

MATLAB follows normal operator precedence.

When in doubt, use parentheses.

Instead of:

```matlab
y = a + b/c^2 - d;
```

write grouping explicitly if that makes the intended equation clearer:

```matlab
y = a + (b/(c^2)) - d;
```

## Useful Numeric Constants

```matlab
pi
Inf
NaN
eps
```

Example:

```matlab
circumference = 2*pi*radius;
```

`NaN` means "Not a Number."

`Inf` represents infinity.

## Quick Reference

| Operation | Syntax |
|---|---|
| Add | `a + b` |
| Subtract | `a - b` |
| Multiply | `a * b` |
| Divide | `a / b` |
| Power | `a^b` |
| Square root | `sqrt(x)` |
| Absolute value | `abs(x)` |
| Natural exponential | `exp(x)` |
| Natural log | `log(x)` |
| Base-10 log | `log10(x)` |
| Pi | `pi` |
