# 04 - Random Number Generation

Random numbers are widely used in simulation, statistics, testing, machine learning, and numerical experiments.

MATLAB uses pseudorandom number generators.

## Uniform Random Values

```matlab
A = rand(3);
```

creates a 3-by-3 matrix of values drawn from a uniform distribution between 0 and 1.

Rectangular:

```matlab
A = rand(2,5);
```

## Standard Normal Random Values

```matlab
A = randn(3);
```

creates normally distributed random values with:

```text
mean approximately 0
standard deviation approximately 1
```

The values are not restricted to -1 through 1.

## Large-Sample Behavior

```matlab
x = randn(1,100000);

mean(x)
std(x)
```

The results should be close to:

```text
mean = 0
std = 1
```

but not exactly equal.

## Reproducibility

Set the random generator state:

```matlab
rng(0);
A = rand(3);
```

Running:

```matlab
rng(0);
A = rand(3);
```

again reproduces the same sequence.

This is useful for:

- Debugging
- Tests
- Research experiments
- Simulations
- Reproducible examples

## Generate Normal Data with Different Mean and Standard Deviation

For desired mean `mu` and standard deviation `sigma`:

```matlab
mu = 5;
sigma = 2;

x = mu + sigma*randn(1000,1);
```

## Example: Simulated Sensor Noise

```matlab
rng(1);

trueValue = 10;
noiseStd = 0.2;

measurements = trueValue + noiseStd*randn(1000,1);
```

## Quick Reference

| Goal | Syntax |
|---|---|
| Uniform random scalar | `rand` |
| Uniform random matrix | `rand(m,n)` |
| Standard normal scalar | `randn` |
| Standard normal matrix | `randn(m,n)` |
| Set reproducible seed | `rng(seed)` |
| Reset reproducibly | `rng(0)` |
| Normal data with mean/std | `mu + sigma*randn(...)` |
