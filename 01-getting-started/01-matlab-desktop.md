# 01 - The MATLAB Desktop

MATLAB combines a programming language with an interactive numerical computing environment.

The exact desktop layout can be customized, but beginners should understand four core areas:

1. Command Window
2. Workspace
3. Editor
4. Current Folder

## Command Window

The Command Window is an interactive prompt.

Enter:

```matlab
a = 5
```

MATLAB evaluates the expression immediately.

You can use the Command Window to:

- Test expressions
- Inspect variables
- Call functions
- Run scripts
- Check documentation
- Debug calculations interactively

## Workspace

The Workspace shows variables currently available in memory.

For example:

```matlab
a = 5;
b = 10;
c = a + b;
```

creates `a`, `b`, and `c`.

The Workspace can display information such as:

- Variable name
- Size
- Value
- Class

Double-clicking many array variables opens them in the Variable Editor.

## Editor

The Editor is used to create and modify MATLAB code files.

Common code files use the `.m` extension.

Example:

```text
motion_model.m
```

The Editor supports:

- Syntax highlighting
- Autocomplete
- Code sections
- Breakpoints
- Error indicators
- Running selected code
- Running complete files

## Current Folder

The Current Folder shows the directory MATLAB is currently working from.

Display it programmatically:

```matlab
pwd
```

The Current Folder matters because MATLAB searches for scripts, functions, and data files using the current location and MATLAB's search path.

## Documentation

Use quick command-line help:

```matlab
help sqrt
```

Open detailed documentation:

```matlab
doc sqrt
```

Find which file MATLAB will use:

```matlab
which sqrt
```

> [!TIP]
> Do not try to memorize every MATLAB function. Learn how to find and read documentation efficiently.

## Quick Reference

| Task | Command |
|---|---|
| Show current folder | `pwd` |
| Quick function help | `help functionName` |
| Open documentation | `doc functionName` |
| Locate a function/file | `which functionName` |
| List workspace variables | `who` |
| Detailed variable list | `whos` |
