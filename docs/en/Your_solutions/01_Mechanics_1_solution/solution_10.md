## 10. Kinematics

The position vector is

$$\vec r(t)=(a\cos(\omega t),b\sin(\omega t),bt)$$

where $a,b,\omega>0$.

We need:

- the trajectory
- the path length from $t=0$ to $t=t_0$
- a Python plot
- special cases

---

## Useful Definitions and Formulas

The coordinates are

$$x=a\cos(\omega t),\qquad y=b\sin(\omega t),\qquad z=bt$$

The path length is

$$s=\int_0^{t_0}|\vec v(t)|\,dt$$

where

$$\vec v(t)=\frac{d\vec r}{dt}$$

---

## Step-by-Step Solution

### a) Find the trajectory

From

$$x=a\cos(\omega t),\qquad y=b\sin(\omega t)$$

we get

$$\frac{x^2}{a^2}+\frac{y^2}{b^2}=\cos^2(\omega t)+\sin^2(\omega t)=1$$

Also

$$z=bt$$

So the point moves upward while its projection in the $xy$-plane is an ellipse.

Therefore the trajectory is an **elliptical helix**:

$$\boxed{\frac{x^2}{a^2}+\frac{y^2}{b^2}=1,\qquad z=bt}$$

---

### b) Compute the path length

Differentiate:

$$\vec v(t)=(-a\omega\sin(\omega t),b\omega\cos(\omega t),b)$$

Its magnitude is

$$|\vec v(t)|=\sqrt{a^2\omega^2\sin^2(\omega t)+b^2\omega^2\cos^2(\omega t)+b^2}$$

So the path length is

$$\boxed{s=\int_0^{t_0}\sqrt{a^2\omega^2\sin^2(\omega t)+b^2\omega^2\cos^2(\omega t)+b^2}\,dt}$$

This is the required exact formula.

---

### c) Python code to draw the trajectory

```python
import numpy as np
import matplotlib.pyplot as plt

a = 3
b = 2
omega = 1
t0 = 10

t = np.linspace(0, t0, 1000)
x = a * np.cos(omega * t)
y = b * np.sin(omega * t)
z = b * t

fig = plt.figure(figsize=(8, 6))
ax = fig.add_subplot(111, projection='3d')
ax.plot(x, y, z)
ax.set_xlabel('x')
ax.set_ylabel('y')
ax.set_zlabel('z')
ax.set_title('Elliptical Helix')
plt.show()
```

---

### d) Special cases

If

$$a=b$$

then the projection in the $xy$-plane becomes a circle, so the trajectory is a **circular helix**.

If

$$b=0$$

then $y=0$ and $z=0$, so the motion reduces to oscillation along the $x$-axis.

If $\omega$ increases, the point winds around faster.

---

## Final Answer

Trajectory:

$$\boxed{\frac{x^2}{a^2}+\frac{y^2}{b^2}=1,\qquad z=bt}$$

Velocity:

$$\boxed{\vec v(t)=(-a\omega\sin(\omega t),b\omega\cos(\omega t),b)}$$

Path length:

$$\boxed{s=\int_0^{t_0}\sqrt{a^2\omega^2\sin^2(\omega t)+b^2\omega^2\cos^2(\omega t)+b^2}\,dt}$$

The curve is an **elliptical helix**.
