# MATLAB Learning Resources

A structured, practical introduction to MATLAB for engineering, scientific computing, numerical programming, data analysis, modeling, and simulation.

This repository is organized as a sequence of learning sections. Each section has its own `README.md` that explains what to expect, what you should know before starting, and the recommended lesson order.

## Repository Structure

```text
matlab-learning/
|
|-- README.md
|-- 01-getting-started/
|   |-- README.md
|   |-- 01-matlab-desktop.md
|   |-- 02-command-window-and-workspace.md
|   |-- 03-scripts-editor-and-debugging.md
|   `-- 04-files-folders-and-search-path.md
|
|-- 02-language-fundamentals/
|   |-- README.md
|   |-- 01-variables-and-naming.md
|   |-- 02-arithmetic-expressions.md
|   |-- 03-data-types.md
|   |-- 04-type-conversion-and-integer-arithmetic.md
|   `-- 05-text-logical-and-structured-data.md
|
|-- 03-arrays-and-matrices/
|   |-- README.md
|   |-- 01-vectors-and-matrices.md
|   |-- 02-indexing-and-slicing.md
|   |-- 03-array-creation-and-shape.md
|   |-- 04-matrix-and-element-wise-operations.md
|   |-- 05-multidimensional-arrays.md
|   `-- 06-vectorization-and-preallocation.md
|
|-- 04-core-array-operations/
|   |-- README.md
|   |-- 01-size-and-inspection.md
|   |-- 02-reductions-and-statistics.md
|   |-- 03-sorting-and-locating-values.md
|   `-- 04-random-number-generation.md
|
`-- 99-quick-reference/
    `-- README.md
```

## Recommended Learning Path

1. [Getting Started](01-getting-started/README.md)
2. [Language Fundamentals](02-language-fundamentals/README.md)
3. [Arrays and Matrices](03-arrays-and-matrices/README.md)
4. [Core Array Operations](04-core-array-operations/README.md)
5. [Quick Reference](99-quick-reference/README.md)

The numbered filenames indicate the recommended order when one lesson builds on another.

## How to Use This Repository

For each lesson:

1. Read the concepts.
2. Type the examples in MATLAB yourself.
3. Predict results before executing code.
4. Modify the examples.
5. Use the quick reference at the end for review.

> [!TIP]
> Avoid learning MATLAB by memorizing commands in isolation. The goal is to understand how variables, arrays, indexing, functions, and the MATLAB environment work together.

## MATLAB Documentation

MATLAB includes extensive built-in documentation.

Quick help:

```matlab
help sqrt
```

Open the full documentation page:

```matlab
doc sqrt
```

Find the file MATLAB will execute:

```matlab
which sqrt
```

Learning to use the documentation is a core MATLAB skill.