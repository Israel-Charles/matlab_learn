# 02 - Command Window and Workspace

The Command Window and Workspace form MATLAB's main interactive workflow.

## Interactive Execution

Enter:

```matlab
a = 5
b = 10
c = a + b
```

MATLAB executes each command as soon as you press Enter.

Variables are stored in the current workspace.

## Suppressing Output

A semicolon suppresses displayed output:

```matlab
a = 5;
```

The assignment still happens.

This is important:

> [!IMPORTANT]
> A semicolon does not stop a line from executing. It only suppresses the displayed result.

For example:

```matlab
a = 5;
b = 10;
c = a + b;
```

creates all three variables even though nothing is printed.

## Inspecting Variables

Type a variable name:

```matlab
c
```

or use:

```matlab
who
```

for variable names only.

For detailed information:

```matlab
whos
```

You can inspect one variable:

```matlab
whos c
```

## Command History

Use the keyboard Up Arrow to recall previous commands.

This is useful for:

- Repeating commands
- Editing previous expressions
- Testing different parameters
- Reusing long function calls

## Clearing the Command Window

```matlab
clc
```

This clears displayed text.

It does not delete variables.

## Clearing Variables

Remove one variable:

```matlab
clear a
```

or:

```matlab
clearvars a
```

Remove workspace variables:

```matlab
clearvars
```

Preserve selected variables:

```matlab
clearvars -except x y
```

## Closing Figures

```matlab
close all
```

closes open figure windows.

## A Practical Reset

For teaching examples or isolated experiments, this is common:

```matlab
clearvars
clc
close all
```

Do not automatically assume every script must begin this way. Larger programs are better organized using functions and controlled scope.

## Why `clear all` Is Usually Unnecessary

`clear all` does more than clear ordinary variables. It can also clear loaded functions and other cached state.

For ordinary workspace cleanup, prefer:

```matlab
clearvars
```

## Variable Editor

Many workspace variables can be opened in the Variable Editor.

This is useful for:

- Inspecting arrays
- Editing small test datasets
- Understanding matrix dimensions

For reproducible programs, values should usually be generated or modified through code rather than manual spreadsheet-style editing.

## Quick Reference

| Task | Command |
|---|---|
| Clear Command Window | `clc` |
| List variables | `who` |
| Detailed variable information | `whos` |
| Clear one variable | `clearvars x` |
| Clear workspace variables | `clearvars` |
| Keep selected variables | `clearvars -except x y` |
| Close all figures | `close all` |
| Display a variable | `x` |
