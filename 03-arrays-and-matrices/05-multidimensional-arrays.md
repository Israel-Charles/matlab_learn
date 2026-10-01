# 05 - Multidimensional Arrays

MATLAB arrays can have more than two dimensions.

## 3-D Arrays

Create pages explicitly:

```matlab
A(:,:,1) = [1 2 3;
            4 5 6;
            7 8 9];

A(:,:,2) = ones(3);

A(:,:,3) = zeros(3);
```

Check size:

```matlab
size(A)
```

Result:

```text
3 3 3
```

You can think of dimension 3 as a sequence of pages or layers.

## Access One Page

```matlab
A(:,:,1)
```

or:

```matlab
A(:,:,2)
```

## Higher Dimensions

MATLAB supports 4-D and higher-dimensional arrays.

Possible interpretations include:

```text
row x column x channel x frame
```

or:

```text
state x sample x experiment x trial
```

The meaning of each dimension depends on the application.

## Useful Functions

Number of dimensions:

```matlab
ndims(A)
```

Shape:

```matlab
size(A)
```

Reshape:

```matlab
B = reshape(A, newSize);
```

Reorder dimensions:

```matlab
B = permute(A, order);
```

Remove singleton dimensions:

```matlab
B = squeeze(A);
```

## Example: RGB Images

A color image is commonly stored as:

```text
height x width x 3
```

where the third dimension corresponds to color channels.

This is one reason multidimensional indexing is important for image processing.

## Example: Multiple Frames

A sequence of RGB images might be represented conceptually as:

```text
height x width x channel x frame
```

## Quick Reference

| Goal | Syntax |
|---|---|
| Access page `k` | `A(:,:,k)` |
| Check dimensions | `size(A)` |
| Count dimensions | `ndims(A)` |
| Reshape | `reshape(A,...)` |
| Reorder dimensions | `permute(A,order)` |
| Remove singleton dimensions | `squeeze(A)` |
