# 01 - Size and Inspection

Several MATLAB functions report different properties of an array.

Understanding the distinction prevents many indexing mistakes.

## `size`

```matlab
A = zeros(3,4);
size(A)
```

returns:

```text
3 4
```

Capture dimensions:

```matlab
[rows, columns] = size(A);
```

Query one dimension:

```matlab
rows = size(A,1);
columns = size(A,2);
```

## `length`

```matlab
length(A)
```

returns the largest array dimension.

For a 3-by-4 matrix:

```text
4
```

`length` does not mean total number of elements.

## `numel`

```matlab
numel(A)
```

returns the total element count.

For a 3-by-4 matrix:

```text
12
```

## `ndims`

```matlab
ndims(A)
```

returns the number of array dimensions.

## `whos`

```matlab
whos A
```

reports:

- Name
- Size
- Bytes
- Class
- Attributes

## Rule of Thumb

Use:

```text
size    -> shape
length  -> largest dimension
numel   -> total number of elements
ndims   -> number of dimensions
```

For general array code, `size` and `numel` are usually more explicit than `length`.

## Example

```matlab
A = rand(5,8,3);

size(A)
numel(A)
ndims(A)
length(A)
```

Interpret the outputs independently rather than treating them as interchangeable.

## Quick Reference

| Question | Function |
|---|---|
| What is the full shape? | `size(A)` |
| How many rows? | `size(A,1)` |
| How many columns? | `size(A,2)` |
| What is the largest dimension? | `length(A)` |
| How many total elements? | `numel(A)` |
| How many dimensions? | `ndims(A)` |
| What type and memory size? | `whos A` |
