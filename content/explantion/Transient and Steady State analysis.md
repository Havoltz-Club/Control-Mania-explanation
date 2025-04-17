- Making blocks in Simulink  
  Introduce transfer function and summer blocks.

---

## Time Domain Analysis

> This analysis is in the time domain.

Let:

$$
C(t) = C_{tr}(t) + C_{ss}(t)
$$

- $C_{tr}(t)$ → **Transient**: Initial to final state  
- $C_{ss}(t)$ → **Steady-State**: How the system behaves as $t \to \infty$

---

## How do we know how the system responds?

> Use **test signals**: `impulse()`, `step()`, `ramp()`  
> These can be simulated using MATLAB.

---

## Order of System

> Determined by the **highest power of 's'** in the denominator of the transfer function.

- First-order system:
  $$
  \frac{1}{s + 1}
  $$

- Second-order system:
  $$
  \frac{1}{s^2 + 2s + 1}
  $$

#  Second-Order System Analysis

Since a lot of systems are **second-order**, let's focus on them.

##  Transfer Function Form:
$$

\frac{C(s)}{R(s)} = \frac{\omega_n^2}{s^2 + 2\zeta\omega_n s + \omega_n^2}]
$$
>This denominator is called the **characteristic polynomial**.

$$
- \omega_n: Undamped natural frequency  
$$$$- \zeta: Damping ratio $$
$$- \sigma = 2\zeta \omega_n: Attenuation constant$$

---

## $$Based\ on\ \zeta\ value:$$

$$1. Undamped: \zeta = 0$$  
$$2. Underdamped: 0 < \zeta < 1$$  
$$3. Critically damped: \zeta = 1$$  
$$4. Overdamped: \zeta > 1$$

---

##  MATLAB Commands

You can observe responses in **MATLAB** using:

```matlab
impulse()
step()
ramp()
```
---

# Root Locus Analysis

> **Root locus method** is a graphical technique for examining how the poles of a closed-loop system vary with changes in gain $K$, providing insights into stability and transient response.

## Fundamental Concepts

### Characteristic Equation
For a system with open-loop transfer function $G(s)$:
$$1 + KG(s)H(s) = 0$$

### Construction Rules
1. **Number of branches** = Number of poles ($n$)
2. **Real-axis segments**: Exist to the left of odd-numbered poles/zeros
3. **Asymptotes**: 
   - Angles: $\theta = \frac{(2q+1)\pi}{n-m}$
   - Centroid: $\sigma = \frac{\sum p_i - \sum z_i}{n-m}$

## Electrical Engineering Applications

### DC Motor Speed Control
```
graph LR
  V_in[Input Voltage] --> G[Motor Transfer Function] --> ω[Output Speed]
  ω --> H[Feedback]
  H --> Compare[Comparator]
```
