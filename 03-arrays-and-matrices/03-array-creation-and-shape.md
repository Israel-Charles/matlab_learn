# 03 - Array Creation and Shape

MATLAB provides compact tools for generating arrays without manually typing every element.

## Colon Operator

Create consecutive values:

```matlab
x = 1:5;
```

Result:

```text
1 2 3 4 5
```

Specify a step:

```matlab
x = 0:2:10;
```

Result:

```text
0 2 4 6 8 10
```

Negative step:

```matlab
x = 10:-2:0;
```

## `linspace`

Create a specified number of evenly spaced samples:

```matlab
x = linspace(0, 10, 6);
```

This produces six points including both endpoints.

`linspace` is commonly used for:

- Time vectors
- Plotting
- Trajectories
- Sampling
- Numerical experiments

## Zeros

```matlab
A = zeros(3);
```

creates a 3-by-3 matrix.

Rectangular:

```matlab
A = zeros(4,7);
```

Specify data type:

```matlab
A = zeros(100,100,"uint8");
```

## Ones

```matlab
A = ones(3);
```

Rectangular:

```matlab
A = ones(4,7);
```

Specify type:

```matlab
A = ones(10,10,"single");
```

## Identity Matrix

```matlab
I = eye(4);
```

Rectangular form:

```matlab
I = eye(3,5);
```

## Reshape

```matlab
A = 1:12;
B = reshape(A,3,4);
```

The number of elements must remain unchanged.

Check:

```matlab
numel(A)
numel(B)
```

## Repeat an Array

```matlab
A = [1 2;
     3 4];

B = repmat(A,2,3);
```

This repeats `A` in a 2-by-3 tiling pattern.

## Concatenate with `cat`

```matlab
C = cat(1, A, B);
```

concatenates along dimension 1.

```matlab
C = cat(2, A, B);
```

concatenates along dimension 2.

Square-bracket syntax is often clearer for ordinary 2-D concatenation.

## Quick Reference

| Goal | Syntax |
|---|---|
| Consecutive vector | `1:10` |
| Vector with step | `0:0.5:5` |
| N evenly spaced points | `linspace(a,b,N)` |
| Zeros | `zeros(m,n)` |
| Ones | `ones(m,n)` |
| Identity matrix | `eye(n)` |
| Reshape | `reshape(A,m,n)` |
| Repeat array | `repmat(A,m,n)` |
| Concatenate dimension `d` | `cat(d,A,B)` |
