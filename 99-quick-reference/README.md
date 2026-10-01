# MATLAB Quick Reference

A compact reference for the concepts covered in the current repository.

## Environment

| Task | Command |
|---|---|
| Clear Command Window | `clc` |
| Clear variables | `clearvars` |
| Clear one variable | `clearvars x` |
| Close figures | `close all` |
| Current folder | `pwd` |
| Change folder | `cd("path")` |
| Show search path | `path` |
| Add folder to path | `addpath("folder")` |
| Locate function/file | `which name` |
| Quick help | `help name` |
| Full documentation | `doc name` |

## Workspace

| Task | Command |
|---|---|
| List variables | `who` |
| Detailed variables | `whos` |
| Inspect one variable | `whos x` |
| Check class | `class(x)` |

## Variables and Types

| Goal | Syntax |
|---|---|
| Assign value | `x = 5;` |
| Double | `double(x)` |
| Single | `single(x)` |
| Signed integer | `int8(x)`, `int16(x)`, `int32(x)`, `int64(x)` |
| Unsigned integer | `uint8(x)`, `uint16(x)`, `uint32(x)`, `uint64(x)` |
| Generic cast | `cast(x,"single")` |
| Min integer value | `intmin("int8")` |
| Max integer value | `intmax("uint8")` |

## Text and Logical Values

| Goal | Syntax |
|---|---|
| String | `"hello"` |
| Character vector | `'hello'` |
| Number to string | `string(x)` |
| Number to char text | `num2str(x)` |
| Logical true | `true` |
| Logical false | `false` |

## Arithmetic

| Operation | Scalar / Matrix Syntax | Element-Wise Syntax |
|---|---|---|
| Add | `A + B` | Same |
| Subtract | `A - B` | Same |
| Multiply | `A * B` | `A .* B` |
| Divide | `A / B` | `A ./ B` |
| Left divide | `A \ B` | `A .\ B` |
| Power | `A^n` | `A.^n` |

## Common Mathematical Functions

| Function | Purpose |
|---|---|
| `sqrt(x)` | Square root |
| `abs(x)` | Absolute value |
| `sin(x)` | Sine |
| `cos(x)` | Cosine |
| `tan(x)` | Tangent |
| `exp(x)` | Exponential |
| `log(x)` | Natural logarithm |
| `log10(x)` | Base-10 logarithm |

## Vector and Matrix Creation

| Goal | Syntax |
|---|---|
| Row vector | `[1 2 3]` |
| Column vector | `[1; 2; 3]` |
| Matrix | `[1 2; 3 4]` |
| Range | `1:10` |
| Range with step | `0:0.5:5` |
| N evenly spaced values | `linspace(a,b,N)` |
| Zeros | `zeros(m,n)` |
| Ones | `ones(m,n)` |
| Identity | `eye(n)` |
| Uniform random | `rand(m,n)` |
| Normal random | `randn(m,n)` |

## Indexing

| Goal | Syntax |
|---|---|
| Element | `A(r,c)` |
| Entire row | `A(r,:)` |
| Entire column | `A(:,c)` |
| Range | `A(2:5,:)` |
| Last element | `A(end)` |
| Last row | `A(end,:)` |
| All values as column | `A(:)` |
| Logical filter | `A(A > threshold)` |
| Replace matching values | `A(A < 0) = 0` |

## Array Shape

| Goal | Syntax |
|---|---|
| Full size | `size(A)` |
| Rows | `size(A,1)` |
| Columns | `size(A,2)` |
| Largest dimension | `length(A)` |
| Total elements | `numel(A)` |
| Number of dimensions | `ndims(A)` |
| Reshape | `reshape(A,...)` |
| Reorder dimensions | `permute(A,order)` |
| Remove singleton dimensions | `squeeze(A)` |

## Reductions

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

## Sorting and Location

| Goal | Syntax |
|---|---|
| Sort ascending | `sort(A)` |
| Sort descending | `sort(A,"descend")` |
| Sort with indices | `[B,I] = sort(A)` |
| Minimum and linear index | `[v,i] = min(A(:))` |
| Maximum and linear index | `[v,i] = max(A(:))` |
| Linear to row/column | `[r,c] = ind2sub(size(A),i)` |
| Find matching indices | `find(A > threshold)` |

## Random Numbers

| Goal | Syntax |
|---|---|
| Uniform samples | `rand(...)` |
| Standard normal samples | `randn(...)` |
| Set seed | `rng(seed)` |
| Normal data with mean/std | `mu + sigma*randn(...)` |

