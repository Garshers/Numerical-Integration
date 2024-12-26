# Numerical Integration Exercises: Trapezoidal and Simpson's Rules

This repository contains exercises that demonstrate the use of numerical integration methods to approximate definite integrals. Specifically, it focuses on the Composite Trapezoidal Rule and the Composite Simpson's Rule, which are both widely used methods in numerical analysis for approximating the integral of a function over a specified interval.

## Exercises Overview

### Trapezoidal Rule

The **Composite Trapezoidal Rule** is a method for approximating the integral of a function by dividing the area under the curve into trapezoids and summing their areas.

- **Objective**: Approximate the integral of the function `f(x)` over the interval `[a, b]` using the composite trapezoidal rule with `n` subintervals.
- **Functionality**: The function `compositeTrapezoidalRule` takes a function `f`, the limits of integration `a` and `b`, and the number of subintervals `n`. It then calculates the approximate value of the integral using the trapezoidal rule formula.

### Simpson's Rule

The **Composite Simpson's Rule** is another method for approximating the integral of a function, which improves upon the trapezoidal rule by fitting quadratic polynomials over each pair of adjacent intervals.

- **Objective**: Approximate the integral of the function `f(x)` over the interval `[a, b]` using the composite Simpson's rule with `n` subintervals (where `n` must be even).
- **Functionality**: The function `compositeSimpsonsRule` performs the integration using Simpson's rule, requiring an even number of subintervals (`n`). It returns the approximate value of the integral.

### Plotting the Approximation

To help visualize the results, the `plotIntegral` function is used to plot the function and the approximation over the specified interval. The plot shows the function, the sampled points, and the segments of the approximation used in Simpson’s Rule.

## Example Usage

Here's an example of how to use the functions to approximate the integral of a quadratic function:

1. Define the function `f(x)` to be integrated.
2. Set the integration limits `a` and `b`.
3. Specify the number of subintervals `n`.
4. Use both the Trapezoidal and Simpson's rules to compute the approximated integrals.
5. Plot the integral approximation.

For example, to approximate the integral of the function `f(x) = x^2 - x + 1` over the interval `[1, 4]` with 10 subintervals:

```matlab
f = @(x) x.^2 - x + 1;  % Function to integrate
a = 1;  % Lower limit
b = 4;  % Upper limit
n = 10;  % Number of subintervals

% Trapezoidal Rule
I = compositeTrapezoidalRule(f, a, b, n);
disp(['The approximate integral is (Trapezoidal rule): ', num2str(I)]);

% Simpson's Rule
I = compositeSimpsonsRule(f, a, b, n);
disp(['The approximate integral is (Simpson rule): ', num2str(I)]);

% Plot the results
plotIntegral(f, a, b, n);
"# Numerical-Integration" 
