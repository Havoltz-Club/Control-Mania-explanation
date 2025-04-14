#  Modelling Electrical Systems

## Time Domain Representation

$$
L \frac{di}{dt} + Ri + \frac{1}{C} \int i \, dt = e_i
$$

$$
\frac{1}{C} \int i \, dt = e_o
$$

---

## Circuit Diagram


---

## Laplace Domain Representation

$$
E_i(s) = Ls I(s) + R I(s) + \frac{1}{C} \cdot \frac{1}{s} I(s)
$$

$$
E_i(s) = \left( Ls + R + \frac{1}{Cs} \right) I(s)
$$

$$
E_o(s) = \frac{1}{Cs} I(s)
$$


$$
\frac{E_o(s)}{E_i(s)} = \frac{1/Cs}{Ls + R + \frac{1}{Cs}}
$$

$$
\frac{E_o(s)}{E_i(s)} = \frac{1}{LCs^2 + RCs + 1}
$$

## Rearranged:

$$
E_o(s) \left( LCs^2 + RCs + 1 \right) = E_i(s)
$$

---

## Time Domain (Differential Equation):

$$
\ddot{e}_o + \dot{e}_o \frac{R}{L} + \frac{e_o}{LC} = \frac{e_i}{LC}
$$


Let:

$$-  x_1 = e_o$$
$$-  x_2 = \dot{e}_o $$

$$
\begin{bmatrix}
\dot{x}_1 \\
\dot{x}_2
\end{bmatrix}
= 
\begin{bmatrix}
x_2 \\
- \frac{R}{L} x_2 - \frac{1}{LC} x_1 + \frac{1}{LC} e_i
\end{bmatrix}
$$

$$
\dot{x} = A x + B u \\
y = C x + D u
$$

$$
sX(s) = A X(s) + B U(s) \\
Y(s) = C X(s) + D U(s)
$$
$$
X(s)(sI - A) = B U(s)
$$

$$
X(s) = (sI - A)^{-1} B U(s)
$$

$$
Y(s) = \left[ C(sI - A)^{-1} B + D \right] U(s)
$$

$$
\frac{Y(s)}{U(s)} = C(sI - A)^{-1} B = TF(s)
$$
