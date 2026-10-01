# 03 - Scripts, Editor, and Debugging

Interactive commands are useful for exploration. Repeated or structured work should usually be placed in code files.

## Creating a Script

Example:

```matlab
A = [2 4;
     3 5];

B = [2 6;
     3 1];

C = A + B;
```

Save it as:

```text
matrix_demo.m
```

Run the script from the Editor or Command Window.

## Script Naming

Use MATLAB-compatible identifiers.

Good:

```text
matrix_demo.m
vehicle_controller.m
example2.m
```

Avoid:

```text
2example.m
matrix demo.m
my-script.m
```

A practical naming rule is:

- Begin with a letter
- Use letters, numbers, and underscores
- Avoid spaces
- Avoid MATLAB keywords

## Comments

Use `%` for comments:

```matlab
% Define vehicle speed in meters per second
vehicleSpeed = 15;
```

Inline comments are also possible:

```matlab
gravity = 9.81; % m/s^2
```

Use comments to explain intent, assumptions, units, or non-obvious reasoning.

## Code Sections

Create sections using `%%`.

```matlab
%% Define Parameters

mass = 10;
acceleration = 2;

%% Calculate Force

force = mass * acceleration;
```

Sections improve readability and can be executed independently from the Editor.

## Running Selected Code

You can highlight selected lines and execute only those lines.

This is useful while developing and testing.

Before considering a script complete, it should generally run correctly from beginning to end without requiring manual execution order.

## Error Messages

When MATLAB encounters an error, read the entire message.

It may identify:

- File name
- Line number
- Column number
- Error category
- Suggested cause

Do not focus only on the highlighted line. The actual cause can appear earlier in the program.

## Breakpoints

A breakpoint pauses execution at a selected line.

Once execution is paused, you can:

- Inspect variables
- Enter commands interactively
- Step one line at a time
- Step into functions
- Step out of functions
- Continue execution
- Stop execution

Breakpoints are one of the most useful debugging tools in MATLAB.

## Example Debugging Workflow

Suppose:

```matlab
radius = 5;
area = pi * radius^2;
circumference = 2 * pi * raduis;
```

MATLAB reports an undefined variable because `raduis` is misspelled.

A useful workflow is:

1. Read the error message.
2. Identify the reported variable or operation.
3. Inspect nearby values.
4. Fix the actual cause.
5. Run again.

## Autocomplete and Editor Assistance

MATLAB may suggest:

- Function names
- Variables
- Properties
- Methods
- Argument options

These suggestions are useful, but documentation should be used when behavior is unclear.

## Quick Reference

| Task | Syntax / Tool |
|---|---|
| Single-line comment | `% comment` |
| Code section | `%% Section Name` |
| Suppress output | End statement with `;` |
| Set breakpoint | Click breakpoint margin in Editor |
| Run script | Run button or script name |
| Execute selected code | Select code and evaluate selection |
| Open documentation | `doc functionName` |
