# 05 - Text, Logical Values, and Structured Data

MATLAB supports more than numeric arrays.

This lesson introduces text, logical values, and several important container types.

## Strings

Use double quotation marks:

```matlab
name = "MATLAB";
```

Check:

```matlab
class(name)
```

Result:

```text
string
```

A string scalar can contain multiple characters while remaining a 1-by-1 string value.

## Character Vectors

Use single quotation marks:

```matlab
name = 'MATLAB';
```

Check:

```matlab
class(name)
```

Result:

```text
char
```

Its size is 1-by-6 because it stores six characters.

## String vs Character Vector

```matlab
a = "MATLAB";
b = 'MATLAB';
```

These are different data types.

Use:

```matlab
class(a)
class(b)
size(a)
size(b)
```

to inspect the difference.

Modern MATLAB code commonly uses strings for text-oriented operations, while character vectors remain common in legacy code and some interfaces.

## Numeric Values and Text

This:

```matlab
char(65)
```

interprets 65 as a character code.

It does not produce the text `"65"`.

To convert a number to text:

```matlab
string(65)
```

or, when a character vector is specifically required:

```matlab
num2str(65)
```

## Logical Values

```matlab
a = true;
b = false;
```

Comparisons produce logical values:

```matlab
x = 10;
isLarge = x > 5;
```

`isLarge` is logical true.

Logical values become especially useful for array filtering and indexing.

## Cell Arrays

Cell arrays can hold values of different types and sizes.

```matlab
C = {10, "hello", [1 2 3]};
```

Cell arrays are useful when heterogeneous data must be stored together.

## Structures

Structures group named fields.

```matlab
robot.name = "Racer 1";
robot.speed = 5.2;
robot.active = true;
```

Access fields using dot notation:

```matlab
robot.speed
```

## Tables

Tables are designed for column-oriented data where variables may have different types.

They are especially useful for:

- Experimental data
- CSV files
- Data analysis
- Named columns

Tables are covered more fully in a later data section.

## Function Handles

MATLAB can store references to functions.

Example:

```matlab
f = @sin;
y = f(pi/2);
```

Function handles become important when working with:

- Optimization
- Numerical integration
- ODE solvers
- Callbacks
- Higher-order functions

## Quick Reference

| Goal | Syntax |
|---|---|
| Create string | `s = "hello";` |
| Create character vector | `c = 'hello';` |
| Convert number to string | `string(x)` |
| Convert number to char text | `num2str(x)` |
| Logical true | `true` |
| Logical false | `false` |
| Create cell array | `{a, b, c}` |
| Create structure field | `s.field = value` |
| Function handle | `f = @sin` |
