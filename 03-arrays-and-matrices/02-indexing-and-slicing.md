# 02 - Indexing and Slicing

Indexing selects or modifies specific array elements.

MATLAB uses 1-based indexing.

## 1-Based Indexing

```matlab
A = [10 20 30 40];
```

First element:

```matlab
A(1)
```

Fourth element:

```matlab
A(4)
```

`A(0)` is invalid.

## Matrix Indexing

For:

```matlab
A = [1 2 3;
     4 5 6;
     7 8 9];
```

use:

```matlab
A(row, column)
```

Example:

```matlab
A(2,3)
```

returns:

```text
6
```

## Modify One Element

```matlab
A(2,3) = 100;
```

## Entire Rows and Columns

The colon `:` means all elements along that dimension.

Second row:

```matlab
A(2,:)
```

Second column:

```matlab
A(:,2)
```

## Index Ranges

Rows 1 through 2:

```matlab
A(1:2,:)
```

Columns 2 through 3:

```matlab
A(:,2:3)
```

Submatrix:

```matlab
A(1:2,2:3)
```

## Step Sizes in Indices

Every second element:

```matlab
A(1:2:end)
```

General form:

```matlab
start:step:end
```

## `end`

Last element:

```matlab
A(end)
```

Second-to-last:

```matlab
A(end-1)
```

Last row:

```matlab
A(end,:)
```

Last column:

```matlab
A(:,end)
```

## Replace an Entire Row

```matlab
A(2,:) = 0;
```

MATLAB expands the scalar `0` across the selected row.

## Replace an Entire Column

```matlab
A(:,3) = 0;
```

or:

```matlab
A(:,3) = [10;
          20;
          30];
```

## Logical Indexing

```matlab
A = [2 8 3 10 4 12];

A(A > 5)
```

returns:

```text
8 10 12
```

Modify matching elements:

```matlab
A(A < 0) = 0;
```

This is one of MATLAB's most powerful data-processing patterns.

## Linear Indexing

MATLAB stores arrays in column-major order.

For:

```matlab
A = [1 2 3;
     4 5 6;
     7 8 9];
```

the linear order is:

```text
1, 4, 7, 2, 5, 8, 3, 6, 9
```

Therefore:

```matlab
A(2)
```

returns `4`.

## Flatten to a Column

```matlab
A(:)
```

returns all elements as a column vector using linear-index order.

## Convert Between Linear and Subscript Indices

Linear index to row/column:

```matlab
[row, column] = ind2sub(size(A), index);
```

Row/column to linear index:

```matlab
index = sub2ind(size(A), row, column);
```

## Quick Reference

| Goal | Syntax |
|---|---|
| Element at row `r`, column `c` | `A(r,c)` |
| Entire row `r` | `A(r,:)` |
| Entire column `c` | `A(:,c)` |
| Row range | `A(2:5,:)` |
| Column range | `A(:,2:4)` |
| Last element | `A(end)` |
| Last row | `A(end,:)` |
| All elements as column | `A(:)` |
| Values meeting condition | `A(A > threshold)` |
| Replace matching values | `A(A < 0) = 0` |
| Linear to subscripts | `ind2sub(...)` |
| Subscripts to linear | `sub2ind(...)` |
