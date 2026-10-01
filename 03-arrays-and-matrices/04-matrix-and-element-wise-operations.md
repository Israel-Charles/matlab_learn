# 04 - Matrix and Element-Wise Operations

MATLAB distinguishes linear-algebra operations from element-by-element operations.

This distinction is essential.

## Matrix Multiplication

```matlab
C = A * B;
```

This performs matrix multiplication.

If:

```text
A is m x n
B is n x p
```

then:

```text
C is m x p
```

The inner dimensions must match.

## Element-Wise Multiplication

```matlab
C = A .* B;
```

Example:

```matlab
A = [1 2 3];
B = [4 5 6];

C = A .* B;
```

Result:

```text
4 10 18
```

## Matrix Power

```matlab
A^2
```

for a square matrix means:

```matlab
A * A
```

## Element-Wise Power

```matlab
A.^2
```

squares each element.

Example:

```matlab
A = [1 2 3];
A.^2
```

Result:

```text
1 4 9
```

## Matrix Division

MATLAB provides:

```matlab
A / B
A \ B
```

These have linear-algebra meanings.

The backslash operator is particularly important for solving linear systems:

```matlab
x = A \ b;
```

This will be explored in a later linear algebra section.

## Element-Wise Division

```matlab
A ./ B
```

performs corresponding-element division.

MATLAB also supports:

```matlab
A .\ B
```

for element-wise left division.

## Addition and Subtraction

For arrays of compatible sizes:

```matlab
A + B
A - B
```

operate element-wise.

## Transpose Operators

Nonconjugate transpose:

```matlab
A.'
```

Complex-conjugate transpose:

```matlab
A'
```

## Common Mistake

If `x` is a vector:

```matlab
y = x^2;
```

is usually not the desired way to square every element.

Use:

```matlab
y = x.^2;
```

This becomes especially important when translating equations into array-based MATLAB code.

## Quick Reference

| Operation | Matrix | Element-Wise |
|---|---|---|
| Multiply | `A * B` | `A .* B` |
| Divide | `A / B` | `A ./ B` |
| Left divide | `A \ B` | `A .\ B` (same as `A ./ B`)|
| Power | `A^n` | `A.^n` |
| Add | `A + B` | Same syntax |
| Subtract | `A - B` | Same syntax |
| Transpose | `A'` | N/A |
| Nonconjugate transpose | `A.'` | N/A |
