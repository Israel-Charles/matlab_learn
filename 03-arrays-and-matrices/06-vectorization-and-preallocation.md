# 06 - Vectorization and Preallocation

MATLAB functions are often designed to operate directly on complete arrays.

This makes many programs shorter and more expressive.

## Loop-Based Calculation

Suppose:

```matlab
x = 1:1000;
```

A loop could compute squares:

```matlab
for i = 1:length(x)
    y(i) = x(i)^2;
end
```

## Vectorized Calculation

The same operation can be written:

```matlab
y = x.^2;
```

This applies the operation to all elements.

## Indexing Is Not the Same as Vectorization

Indexing selects elements:

```matlab
A(:,3)
```

Vectorization expresses operations over entire arrays:

```matlab
y = sin(x);
```

The concepts often work together, but they are not identical.

## Logical Vectorization

Instead of checking each value manually:

```matlab
A(A < 0) = 0;
```

sets every negative element to zero in one expression.

## Preallocation

Sometimes loops are the clearest approach.

If a loop grows an array repeatedly:

```matlab
for i = 1:1000
    x(i) = i^2;
end
```

MATLAB may need to repeatedly resize storage.

Preallocate first:

```matlab
x = zeros(1,1000);

for i = 1:1000
    x(i) = i^2;
end
```

## Prefer Clarity

Vectorization is often:

- Compact
- Readable
- Mathematically expressive

Modern MATLAB also optimizes many loops well.

Do not make code harder to understand merely to eliminate a loop.

Use the clearest correct approach, and optimize only when performance matters.

## Example: Thresholding

Loop-based:

```matlab
for i = 1:numel(A)
    if A(i) < 0
        A(i) = 0;
    end
end
```

Vectorized:

```matlab
A(A < 0) = 0;
```

## Example: Function Evaluation

```matlab
x = linspace(0,10,1000);
y = x.^2 + 3*x + 5;
```

Because `x` is a vector, the power must be element-wise:

```matlab
x.^2
```

## Quick Reference

| Goal | Pattern |
|---|---|
| Square every element | `x.^2` |
| Apply function to array | `sin(x)` |
| Filter values | `x(x > 0)` |
| Replace matching values | `x(x < 0) = 0` |
| Preallocate row vector | `zeros(1,N)` |
| Preallocate matrix | `zeros(m,n)` |
| Total number of loop elements | `numel(A)` |
