## Problem 1. Vector Algebra for the L6 Physcics Basics

Given  
$\vec{a}=[2,1,-3]$ and $\vec{b}=[4,-2,1]$.

---

### a) Magnitude of each vector

The **magnitude** (or length) of a vector tells us how long the vector is in space.  
For a 3D vector

$$
\vec{v}=[v_x,v_y,v_z]
$$

the magnitude is calculated using the formula

$$
|\vec{v}|=\sqrt{v_x^2+v_y^2+v_z^2}.
$$

This formula comes from the **3D Pythagorean theorem**.  
We square each component, add them together, and then take the square root.

---

#### Magnitude of $\vec{a}$

Vector $\vec{a}$ has components

$$
\vec{a}=[2,1,-3].
$$

Substitute these values into the formula:

$$
|\vec{a}|=\sqrt{2^2+1^2+(-3)^2}.
$$

Now compute each square:

$$
2^2=4,\qquad1^2=1,\qquad(-3)^2=9.
$$

Add them together:

$$
4+1+9=14.
$$

Therefore

$$
|\vec{a}|=\sqrt{14}.
$$

---

#### Magnitude of $\vec{b}$

Vector $\vec{b}$ is

$$
\vec{b}=[4,-2,1].
$$

Use the same formula:

$$
|\vec{b}|=\sqrt{4^2+(-2)^2+1^2}.
$$

Compute the squares:

$$
4^2=16,\qquad(-2)^2=4,\qquad1^2=1.
$$

Add them:

$$
16+4+1=21.
$$

So

$$
|\vec{b}|=\sqrt{21}.
$$

---

### b) Dot product $\vec{a}\cdot\vec{b}$

The **dot product** measures how much two vectors point in the same direction.

For vectors

$$
\vec{a}=[a_x,a_y,a_z],\qquad
\vec{b}=[b_x,b_y,b_z]
$$

the dot product is

$$
\vec{a}\cdot\vec{b}=a_xb_x+a_yb_y+a_zb_z.
$$

This means we multiply the corresponding components and then add the results.

Substitute the components:

$$
\vec{a}\cdot\vec{b}=2\cdot4+1\cdot(-2)+(-3)\cdot1.
$$

Compute each multiplication:

$$
2\cdot4=8
$$

$$
1\cdot(-2)=-2
$$

$$
(-3)\cdot1=-3
$$

Now add them:

$$
8-2-3=3.
$$

So

$$
\vec{a}\cdot\vec{b}=3.
$$

---

### c) Cross product $\vec{a}\times\vec{b}$

The **cross product** produces a new vector that is **perpendicular to both vectors**.

It can be calculated using the determinant:

$$
\vec{a}\times\vec{b}=
\begin{vmatrix}
\hat{i}&\hat{j}&\hat{k}\\
2&1&-3\\
4&-2&1
\end{vmatrix}.
$$

Here:

- $\hat{i}$ is the unit vector in the $x$ direction
- $\hat{j}$ is the unit vector in the $y$ direction
- $\hat{k}$ is the unit vector in the $z$ direction

---

#### Expand the determinant

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

Now compute each small determinant.

First:

$$
\begin{vmatrix}
1&-3\\
-2&1
\end{vmatrix}
=1\cdot1-(-3)(-2)
=1-6
=-5.
$$

Second:

$$
\begin{vmatrix}
2&-3\\
4&1
\end{vmatrix}
=2\cdot1-(-3)\cdot4
=2+12
=14.
$$

Third:

$$
\begin{vmatrix}
2&1\\
4&-2
\end{vmatrix}
=2\cdot(-2)-1\cdot4
=-4-4
=-8.
$$

Substitute back:

$$
\vec{a}\times\vec{b}
=-5\hat{i}-14\hat{j}-8\hat{k}.
$$

In coordinate form:

$$
\vec{a}\times\vec{b}=[-5,-14,-8].
$$

---

### d) Angle between the vectors

The angle between two vectors can be found using the formula

$$
\cos\theta=\frac{\vec{a}\cdot\vec{b}}{|\vec{a}||\vec{b}|}.
$$

From earlier calculations we know:

$$
\vec{a}\cdot\vec{b}=3
$$

$$
|\vec{a}|=\sqrt{14}
$$

$$
|\vec{b}|=\sqrt{21}.
$$

Substitute these values:

$$
\cos\theta=\frac{3}{\sqrt{14}\sqrt{21}}.
$$

Combine the square roots:

$$
\sqrt{14}\sqrt{21}=\sqrt{294}.
$$

So

$$
\cos\theta=\frac{3}{\sqrt{294}}.
$$

Now take the inverse cosine:

$$
\theta=\cos^{-1}\left(\frac{3}{\sqrt{294}}\right).
$$

Approximate value:

$$
\theta\approx79.9^\circ.
$$

This means the vectors form an angle of about **80 degrees**, so they are almost perpendicular.

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
