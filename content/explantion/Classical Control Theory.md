## What is Classical Control Theory?

- In engineering and mathematics, control theory deals with the behaviour of dynamical systems.
$$--S. Simrack$$

  It is a field of engineering and mathematics that deals with the control of dynamical systems in engineered processes and machines
  $$-- Wikipedia$$
  
- The basic idea behind control theory is to understand a proscess o a system by developing a model for it that represents the relationships between inputs and outputs, and using that model to adjust the inputs however you need to get whatever output you want to achieve. 
$$ -- APC-Cheme $$

## What are the Main Components of Classical Control?

Here are the main components of classical control:

>1. Transfer Functions
>2. Stability Analysis
- Routh-Hurwitz Criterion 
- Root Locus
>3. Frequency-Domain Analysis
- Bode Plot
- Root Locus
>4. PID Controllers
>5. Compensator Design

## Where Do We Begin?

Let's start with the math one needs to know:

1. **Calculus**
2. **Differential Equations**
    - **What are differential equations?**  
      An equation which contains one or more derivatives of a function.
    - In simple terms, it is an equation which describes rates of change.

    **Example:**

    - Displacement, $y = 0\, \text{m}$
    - $\sum \text{forces} = ma$
    - $a = \frac{d^2y}{dt^2}$  (rate of change of velocity)
    - $W - \text{friction} = ma$
    - $mg - b \frac{dy}{dt} = m \frac{d^2y}{dt^2}$
    - $\Rightarrow mg = m\ddot{y} + b\dot{y}$

3. **Transforms**
    - **Why Laplace transform?**  
      Can you solve a differential equation? Probably not. So, to make it easier, we use Laplace transforms.
  
4. **Linear Algebra**
    - This won’t be helpful now, but we will get back to this.
