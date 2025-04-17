### Getting Started

The most important concept in control theory and engineering is the **transfer function**.

### Example Differential Equation

Let’s say we have the following differential equation with all initial conditions being zero. Let \( x \) be the input and \( y \) be the output:

$$
\ddot{y} + 2\dot{y} + y = \dot{x} + 2x
$$

Taking the Laplace transform:

$$
Y(s)s^2 + 2Y(s)s + Y(s) = X(s)s + 2X(s)
$$

$$
Y(s)(s^2 + 2s + 1) = X(s)(s + 2)
$$

$$
\frac{Y(s)}{X(s)} = \frac{s + 2}{s^2 + 2s + 1} = T(s)
$$

### Definition

The **transfer function** is the ratio of the output (the response of a system) to the input (any sort of function) in the Laplace domain, assuming all initial conditions are zero.

### General Case

For a general differential equation:

$$
a_0 \ddot{y} + a_1 y^{(n)} + \ldots + a_n y = b_0 \dot{x} + b_1 x^{(n-1)} + \ldots + b_m x
$$

The transfer function in the Laplace domain is:

$$
\frac{Y(s)}{X(s)} = \frac{b_0 s^m + b_1 s^{m-1} + \ldots + b_m}{a_0 s^n + a_1 s^{n-1} + \ldots + a_n}
$$

---

## Implementing in MATLAB

We can represent transfer functions in MATLAB using the `tf()` function:

```
num = [ ]; % numerator coefficients
den = [ ]; % denominator coefficients
sys = tf(num, den);
sys
```

---

## Block Diagram Representation

### Better Representation

Block diagrams in the Laplace domain provide a better way to represent transfer functions.

### MATLAB Code for Connections

- `parallel(sys1, sys2)`  
- `series(sys1, sys2)`  
- `feedback(sys1, sys2)`  
