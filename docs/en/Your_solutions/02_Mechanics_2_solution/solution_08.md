## 8. Work of a Variable Force

Given

$$F(x)=-kx$$

We need:
- the equation of motion and its solution
- the work from $0$ to $x_0$
- the potential energy
- verify $F=-\frac{dU}{dx}$
- describe the graphs

---

## Useful Definitions and Formulas

Newton's second law:

$$m\frac{d^2x}{dt^2}=F(x)$$

Work of a variable force:

$$W=\int_{x_1}^{x_2}F(x)\,dx$$

Potential energy satisfies:

$$F=-\frac{dU}{dx}$$

---

## Step-by-Step Solution

### Step 1. Equation of motion

Since

$$F=-kx$$

Newton's law gives

$$m\frac{d^2x}{dt^2}=-kx$$

or

$$\frac{d^2x}{dt^2}+\frac{k}{m}x=0$$

Let

$$\omega=\sqrt{\frac{k}{m}}$$

Then the equation becomes

$$x''+\omega^2x=0$$

Its general solution is

$$\boxed{x(t)=A\cos(\omega t)+B\sin(\omega t)}$$

This is simple harmonic motion.

---

### Step 2. Work from $0$ to $x_0$

$$W=\int_0^{x_0}(-kx)\,dx$$

$$W=-k\int_0^{x_0}x\,dx=-k\left[\frac{x^2}{2}\right]_0^{x_0}$$

$$W=-\frac{1}{2}kx_0^2$$

So

$$\boxed{W=-\frac{1}{2}kx_0^2}$$

The work is negative because the restoring force opposes the displacement.

---

### Step 3. Potential energy

We define potential energy by

$$U(x)=-\int F(x)\,dx$$

Since $F(x)=-kx$,

$$U(x)=-\int(-kx)\,dx=\int kx\,dx=\frac{1}{2}kx^2+C$$

Choosing $U(0)=0$ gives $C=0$, so

$$\boxed{U(x)=\frac{1}{2}kx^2}$$

---

### Step 4. Verify $F=-\frac{dU}{dx}$

Differentiate:

$$\frac{dU}{dx}=\frac{d}{dx}\left(\frac{1}{2}kx^2\right)=kx$$

Therefore

$$-\frac{dU}{dx}=-kx=F(x)$$

Verified.

---

### Step 5. Graphs

- $F(x)=-kx$ is a straight line through the origin with negative slope.
- $U(x)=\frac{1}{2}kx^2$ is an upward-opening parabola.

---

## Final Answer

Equation of motion:

$$\boxed{m\frac{d^2x}{dt^2}=-kx}$$

Solution:

$$\boxed{x(t)=A\cos\left(\sqrt{\frac{k}{m}}t\right)+B\sin\left(\sqrt{\frac{k}{m}}t\right)}$$

Work from $0$ to $x_0$:

$$\boxed{W=-\frac{1}{2}kx_0^2}$$

Potential energy:

$$\boxed{U(x)=\frac{1}{2}kx^2}$$

And indeed,

$$\boxed{F=-\frac{dU}{dx}}$$
