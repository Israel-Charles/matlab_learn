# 04 - Files, Folders, and the MATLAB Search Path

MATLAB must be able to locate scripts, functions, and data files before it can use them.

## Current Folder

Display the Current Folder:

```matlab
pwd
```

Change it:

```matlab
cd("C:\path\to\project")
```

On macOS or Linux:

```matlab
cd("/path/to/project")
```

## Why File Location Matters

If MATLAB cannot find a script or function, you may see an error indicating that the name is undefined or unavailable.

MATLAB can locate code from places including:

- Current Folder
- Folders on the MATLAB search path
- Project-managed locations
- Packages and class folders

You do not need to put every project file into one folder.

## Determine Which File MATLAB Will Use

```matlab
which myFunction
```

To see all matching locations:

```matlab
which myFunction -all
```

This is especially useful when multiple files have the same name.

## MATLAB Search Path

Display the current search path:

```matlab
path
```

Temporarily add a folder:

```matlab
addpath("utilities")
```

Add a folder and its subfolders:

```matlab
addpath(genpath("utilities"))
```

Remove a folder:

```matlab
rmpath("utilities")
```

> [!CAUTION]
> Avoid adding large unrelated directory trees to the MATLAB path. Name conflicts become harder to diagnose.

## File Types

### `.m`

Standard MATLAB source code.

Can contain:

- Scripts
- Functions
- Class definitions

### `.mlx`

MATLAB Live Script.

Useful for documents that combine:

- Code
- Formatted text
- Equations
- Output
- Plots
- Interactive controls

### `.asv`

Autosave or backup file that MATLAB may create depending on configuration.

Treat the `.m` or `.mlx` source as the primary file, not the `.asv` backup.

## Recommended Repository Layout

For a larger project:

```text
project/
|-- scripts/
|-- functions/
|-- data/
|-- tests/
|-- results/
`-- README.md
```

The best structure depends on the project, but explicit organization scales better than placing every file in one directory.

## Quick Reference

| Task | Command |
|---|---|
| Show Current Folder | `pwd` |
| Change folder | `cd("path")` |
| Show search path | `path` |
| Add folder to path | `addpath("folder")` |
| Add folder tree | `addpath(genpath("folder"))` |
| Remove folder from path | `rmpath("folder")` |
| Find file used by MATLAB | `which name` |
| Find all matches | `which name -all` |
