## Problem 1. Vector Algebra for the L6 Physcics Basics

Given  
$\vec{a}=[2,1,-3]$ and $\vec{b}=[4,-2,1]$.

---

### a) Magnitude of each vector

Magnitude in 3D:

$$
|\vec{v}|=\sqrt{v_x^2+v_y^2+v_z^2}.
$$

For $\vec{a}$:

$$
|\vec{a}|=\sqrt{2^2+1^2+(-3)^2}
=\sqrt{4+1+9}
=\sqrt{14}.
$$

For $\vec{b}$:

$$
|\vec{b}|=\sqrt{4^2+(-2)^2+1^2}
=\sqrt{16+4+1}
=\sqrt{21}.
$$

So:

$$
|\vec{a}|=\sqrt{14},\qquad|\vec{b}|=\sqrt{21}.
$$

---

### b) Dot product $\vec{a}\cdot\vec{b}$

Dot product:

$$
\vec{a}\cdot\vec{b}=a_xb_x+a_yb_y+a_zb_z.
$$

Compute:

$$
\vec{a}\cdot\vec{b}=2\cdot4+1\cdot(-2)+(-3)\cdot1
=8-2-3
=3.
$$

So:

$$
\vec{a}\cdot\vec{b}=3.
$$

---

### c) Cross product $\vec{a}\times\vec{b}$

Use the determinant:

$$
\vec{a}\times\vec{b}=
\begin{vmatrix}
\hat{i}&\hat{j}&\hat{k}\\
2&1&-3\\
4&-2&1
\end{vmatrix}.
$$

Expand along the first row:

$$
\vec{a}\times\vec{b}
=\hat{i}
\begin{vmatrix}
1&-3\\
-2&1
\end{vmatrix}
-\hat{j}
\begin{vmatrix}
2&-3\\
4&1
\end{vmatrix}
+\hat{k}
\begin{vmatrix}
2&1\\
4&-2
\end{vmatrix}.
$$

Now calculate each $2\times2$ determinant:

$$
\begin{vmatrix}
1&-3\\
-2&1
\end{vmatrix}
=1\cdot1-(-3)(-2)
=1-6
=-5,
$$

$$
\begin{vmatrix}
2&-3\\
4&1
\end{vmatrix}
=2\cdot1-(-3)\cdot4
=2+12
=14,
$$

$$
\begin{vmatrix}
2&1\\
4&-2
\end{vmatrix}
=2\cdot(-2)-1\cdot4
=-4-4
=-8.
$$

So:

$$
\vec{a}\times\vec{b}
=-5\hat{i}-14\hat{j}-8\hat{k}.
$$

Or in vector form:

$$
\vec{a}\times\vec{b}=[-5,-14,-8].
$$

---

### d) Angle between the vectors

Use the formula:

$$
\cos\theta=\frac{\vec{a}\cdot\vec{b}}{|\vec{a}||\vec{b}|}.
$$

Substitute the values:

$$
\cos\theta=\frac{3}{\sqrt{14}\sqrt{21}}
=\frac{3}{\sqrt{294}}.
$$

Therefore:

$$
\theta=\cos^{-1}\left(\frac{3}{\sqrt{294}}\right).
$$

Approximate value:

$$
\theta\approx79.9^\circ.
$$

---

## Final answers

$$
|\vec{a}|=\sqrt{14},\qquad|\vec{b}|=\sqrt{21}
$$

$$
\vec{a}\cdot\vec{b}=3
$$

$$
\vec{a}\times\vec{b}=[-5,-14,-8]
$$

$$
\theta=\cos^{-1}\left(\frac{3}{\sqrt{294}}\right)\approx79.9^\circ
$$
