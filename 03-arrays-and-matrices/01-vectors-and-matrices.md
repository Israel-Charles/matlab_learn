# 01 - Vectors and Matrices

MATLAB is fundamentally array-oriented.

## Scalars

A scalar is a 1-by-1 numeric array.

```matlab
x = 5;
size(x)
```

## Row Vectors

Create a row vector using spaces:

```matlab
A = [1 2 3 4 5];
```

Commas are also valid:

```matlab
A = [1, 2, 3, 4, 5];
```

Check:

```matlab
size(A)
```

Result:

```text
1 5
```

## Column Vectors

Separate rows with semicolons:

```matlab
B = [1;
     2;
     3;
     4;
     5];
```

Check:

```matlab
size(B)
```

Result:

```text
5 1
```

## Vectors Are Stored as 2-D Arrays

A row vector has size:

```text
1 x N
```

A column vector has size:

```text
N x 1
```

For example:

```matlab
A = [1 2 3];
ndims(A)
```

returns `2`.

> `ndims(A)` The ndims function in MATLAB returns the number of dimensions in an array (always 2 or more)

## Matrices

Use spaces between columns and semicolons between rows:

```matlab
A = [1 2 3;
     4 5 6;
     7 8 9];
```

This is a 3-by-3 matrix.

## Row Lengths Must Match

Invalid:

```matlab
A = [1 2 3;
     4 5;
     6 7 8];
```

A numeric matrix must be rectangular.

## Concatenation

Horizontal:

```matlab
A = [1 2];
B = [3 4];

C = [A B];
```

Result:

```text
1 2 3 4
```

Vertical:

```matlab
C = [A;
     B];
```

Result:

```text
1 2
3 4
```

Dimensions must be compatible along the concatenation direction.

## Transpose

For a row vector:

```matlab
A = [1 2 3 4];
B = A.';
```

`B` is a column vector.

MATLAB also supports:

```matlab
A'
```

but the two transpose operators differ for complex data.

- `A.'` is the nonconjugate transpose
- `A'` is the complex-conjugate transpose

For real values, they produce the same numeric values.

## Quick Reference

| Goal | Syntax |
|---|---|
| Row vector | `[1 2 3]` |
| Column vector | `[1; 2; 3]` |
| Matrix | `[1 2; 3 4]` |
| Horizontal concatenate | `[A B]` |
| Vertical concatenate | `[A; B]` |
| Nonconjugate transpose | `A.'` |
| Conjugate transpose | `A'` |
| Get size | `size(A)` |
| Number of dimensions | `ndims(A)` |
