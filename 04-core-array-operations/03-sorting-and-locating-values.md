# 03 - Sorting and Locating Values

MATLAB can sort array values and return indices that identify where values occur.

## Sorting

For a matrix:

```matlab
sort(A)
```

sorts along the first nonsingleton dimension.

For an ordinary matrix, each column is sorted independently in ascending order.

Descending:

```matlab
sort(A, "descend")
```

## Sort and Preserve Original Indices

```matlab
[sortedValues, indices] = sort(A);
```

`indices` tells you where the sorted values came from.

## Overall Minimum Location

```matlab
[minValue, linearIndex] = min(A(:));
```

Convert the linear index to row and column:

```matlab
[row, column] = ind2sub(size(A), linearIndex);
```

## Overall Maximum Location

```matlab
[maxValue, linearIndex] = max(A(:));
[row, column] = ind2sub(size(A), linearIndex);
```

## Find Values Matching a Condition

```matlab
indices = find(A > 10);
```

For many operations, logical indexing is simpler:

```matlab
values = A(A > 10);
```

Use `find` when the numeric indices themselves are needed.

## Find Row and Column Indices

For a matrix condition:

```matlab
[row, column] = find(A > 10);
```

## Example

```matlab
A = [4 9 2;
     8 1 7;
     6 3 5];

[minValue, idx] = min(A(:));
[minRow, minCol] = ind2sub(size(A), idx);

[maxValue, idx] = max(A(:));
[maxRow, maxCol] = ind2sub(size(A), idx);
```

## Quick Reference

| Goal | Syntax |
|---|---|
| Sort ascending | `sort(A)` |
| Sort descending | `sort(A,"descend")` |
| Sorted values and indices | `[B,I] = sort(A)` |
| Overall minimum and index | `[v,i] = min(A(:))` |
| Overall maximum and index | `[v,i] = max(A(:))` |
| Linear index to row/column | `[r,c] = ind2sub(size(A),i)` |
| Find matching indices | `find(A > threshold)` |
| Extract matching values | `A(A > threshold)` |
