# 02 - Reductions and Statistics

Reduction functions summarize array values along one or more dimensions.

## `max`

For:

```matlab
A = [1 20 3;
     8  4 9;
     2 10 5];
```

```matlab
max(A)
```

returns one maximum per column:

```text
8 20 9
```

## Maximum of the Entire Array

```matlab
largestValue = max(A, [], "all");
```

A widely compatible alternative is:

```matlab
largestValue = max(A(:));
```

## `min`

Column-wise:

```matlab
min(A)
```

Whole array:

```matlab
smallestValue = min(A, [], "all");
```

or:

```matlab
smallestValue = min(A(:));
```

## `sum`

Column sums:

```matlab
sum(A)
```

Row sums:

```matlab
sum(A,2)
```

Whole array:

```matlab
total = sum(A, "all");
```

or:

```matlab
total = sum(A(:));
```

## `mean`

Column means:

```matlab
mean(A)
```

Row means:

```matlab
mean(A,2)
```

Whole array:

```matlab
mean(A, "all")
```

## Understanding Dimensions

For an ordinary matrix:

```matlab
operation(A)
```

often works down columns by default because dimension 1 is the first nonsingleton dimension.

Specifying a dimension makes intent clearer:

```matlab
sum(A,1)
sum(A,2)
```

Think of:

- Dimension 1 as moving down rows within each column
- Dimension 2 as moving across columns within each row

## Example

```matlab
A = [1 2 3;
     4 5 6];

columnTotals = sum(A,1);
rowTotals = sum(A,2);
overallTotal = sum(A,"all");
```

## Quick Reference

| Goal | Syntax |
|---|---|
| Column maximums | `max(A)` |
| Overall maximum | `max(A,[],"all")` |
| Column minimums | `min(A)` |
| Overall minimum | `min(A,[],"all")` |
| Column sums | `sum(A)` |
| Row sums | `sum(A,2)` |
| Overall sum | `sum(A,"all")` |
| Column means | `mean(A)` |
| Row means | `mean(A,2)` |
| Overall mean | `mean(A,"all")` |
