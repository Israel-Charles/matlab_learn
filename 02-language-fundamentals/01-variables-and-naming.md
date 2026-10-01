# 01 - Variables and Naming

A variable stores a value or array so it can be reused later.

## Assignment

MATLAB uses `=` for assignment.

```matlab
speed = 15;
```

The left side is the variable name.

The right side is the value or expression.

## Reassignment

Variables can be replaced:

```matlab
x = 3;
x = 5;
```

The current value is now `5`.

You can use the existing value:

```matlab
x = 5;
x = x + 4;
```

Now `x` is `9`.

## No Implicit Increment Operator

Use:

```matlab
x = x + 1;
```

rather than C/C++-style operators such as:

```text
x++
```

## Variable Names

Good names:

```matlab
x = 10;
speed = 15;
vehicleSpeed = 20;
vehicle_speed = 25;
value2 = 30;
```

Avoid names that:

- Begin with a number
- Contain spaces
- Contain unsupported punctuation
- Match MATLAB keywords

## Case Sensitivity

MATLAB is case-sensitive.

```matlab
temperature = 25;
Temperature = 30;
```

These are different variables.

## Avoid Shadowing Built-In Functions

Avoid:

```matlab
sum = 10;
mean = 3;
plot = 4;
```

These names can hide MATLAB functions.

Check what MATLAB resolves:

```matlab
which sum
```

If you accidentally create a conflicting variable:

```matlab
clearvars sum
```

## Descriptive Naming

Prefer:

```matlab
samplingTime = 0.01;
vehicleSpeed = 12;
distanceTraveled = vehicleSpeed * samplingTime;
```

over:

```matlab
a = 0.01;
b = 12;
c = a * b;
```

Short mathematical names are appropriate when the meaning is conventional.

## Quick Reference

| Task | Example |
|---|---|
| Create variable | `x = 5;` |
| Reassign variable | `x = 10;` |
| Increment value | `x = x + 1;` |
| Inspect value | `x` |
| Inspect class | `class(x)` |
| Inspect details | `whos x` |
| Remove variable | `clearvars x` |
| Check naming conflict | `which name` |
