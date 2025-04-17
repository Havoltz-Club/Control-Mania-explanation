# Introduction to Control Theory

## What is Control Theory?

> "In engineering and mathematics, control theory deals with the behaviour of dynamical systems."  
>$$ --{S. Simrock}$$

> "It is a field of engineering and mathematics that deals with the control of dynamical systems in engineered processes and machines."  
> $$ --Wikipedia$$

> "The basic idea behind control theory is to understand a process or a system by developing a model for it that represents the relationships between inputs and outputs, and using that model to adjust the inputs however you need to get whatever output you want to achieve."  
>  $$--ANC\_themeE,\ teddit.com$$

**Summary**:  
>Control theory is the attempt to understand real-world systems, their dynamics, and exert forces to achieve desired outputs.

---

## Core Concepts

### Foundational Terms
>1. **Plants**  
- Definition: A piece of equipment or set of machine parts functioning together  
   - Example: A bike's components (gears, transmission, engine)  
   - Mathematical representation: $P(s) = \frac{Y(s)}{U(s)}$

>2. **Processes**  
- Definition: A natural, progressively continuing operation that changes
- gradually to produce a result  
- Example: Rotation of a bike's wheels  
   - Equation: $\dot{x}(t) = f(x(t), u(t))$

>3. **Systems**  
- Definition: Combination of plants and processes to perform an objective  
- Example: The entire bike as a system  
- State-space: $\begin{cases} \dot{x} = Ax + Bu \\ y = Cx + Du \end{cases}$

>4. **Disturbances**  
- Definition: Signals that affect the system output  
- Example: Road bumps, wind resistance  
- Model: $d(t) \in \mathcal{D}$

>5. **Feedback**  
- Types:  
    - Positive feedback: $u(t) = +K\cdot e(t)$  
    - Negative feedback: $u(t) = -K\cdot e(t)$  

---

## Control System Design Methodology

1. **Modelling**  
   - Transfer functions: $G(s) = \frac{b_0s^m + \cdots + b_m}{s^n + \cdots + a_n}$  
   - Nonlinear systems: $\dot{x} = f(x,u)$

2. **Analysis**  
   - Stability criteria:  
     - Routh-Hurwitz  
     - Nyquist: $Z = N + P$  
   - Performance metrics:  
     - Rise time ($t_r$)  
     - Settling time ($t_s$)  
     - Overshoot ($M_p\%$)

3. **Synthesis**  
   - Controller design:  
     - PID: $u(t) = K_p e(t) + K_i \int e(t)dt + K_d \frac{de(t)}{dt}$  
     - State feedback: $u = -Kx$  
   - Observer design (Luenberger): $\dot{\hat{x}} = A\hat{x} + Bu + L(y - C\hat{x})$

---

## Applications in Electrical Engineering

### Speed Control Systems
- **DC Motor Control**:  
  $$\tau = K_t i_a$$  
  $$\omega = \frac{V_a - i_a R_a}{K_e}$$

- **Governor Systems**:  
  $$\frac{\Delta \omega(s)}{\Delta T(s)} = \frac{1}{Js + B}$$

### Temperature Control
- Thermal dynamics:  
  $$C\frac{dT}{dt} = q_{in} - \frac{T-T_\infty}{R}$$

### Power System Stability
- Swing equation:  
  $$M\frac{d^2\delta}{dt^2} + D\frac{d\delta}{dt} = P_m - P_e$$
---

# Control System Design Process

The design of a control system involves three fundamental stages:

## 1. Modelling
Develop mathematical representations of the system:
- **Transfer Function Approach**:
  $$G(s) = \frac{Y(s)}{U(s)} = \frac{b_0s^m + \cdots + b_m}{a_0s^n + \cdots + a_n}$$
  
- **State-Space Representation**:
  $$\begin{cases}
  \dot{x}(t) = Ax(t) + Bu(t) \\
  y(t) = Cx(t) + Du(t)
  \end{cases}$$
  
- **Nonlinear Systems**:
  $$\dot{x} = f(x,u,t)$$

## 2. Analysis
Evaluate system properties:

### Stability
- **Routh-Hurwitz Criterion**:
  $$\text{All coefficients } a_i > 0$$
- **Nyquist Criterion**:
  $$Z = N + P$$


## 3. Synthesis
Design controllers to meet specifications:

### Controller Types
- **PID Control**:
  $$u(t) = K_p e(t) + K_i \int_0^t e(\tau)d\tau + K_d \frac{de(t)}{dt}$$
  
- **State Feedback**:
  $$u = -Kx$$
  
- **Optimal Control (LQR)**:
  $$J = \int_0^\infty (x^\top Qx + u^\top Ru)dt$$
