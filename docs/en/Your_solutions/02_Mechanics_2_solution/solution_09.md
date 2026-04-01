## 9. Vertical Throw with Drag

We are given

$$m\frac{dv}{dt}=-mg-kv$$

with

$$v(0)=v_0,\qquad x(0)=10$$

We need:
- the analytical solution
- the maximum height
- comparison with no drag

---

## Useful Definitions and Formulas

Rewrite the equation as

$$\frac{dv}{dt}+\frac{k}{m}v=-g$$

This is a first-order linear differential equation.

---

## Step-by-Step Solution

### Step 1. Solve for velocity

The solution of

$$\frac{dv}{dt}+\frac{k}{m}v=-g$$

is

$$v(t)=Ce^{-\frac{k}{m}t}-\frac{mg}{k}$$

Use $v(0)=v_0$:

$$v_0=C-\frac{mg}{k}$$

So

$$C=v_0+\frac{mg}{k}$$

Therefore

$$\boxed{v(t)=\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k}}$$

---

### Step 2. Solve for position

Since

$$\frac{dx}{dt}=v(t)$$

integrate:

$$x(t)=10+\int_0^t\left[\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}s}-\frac{mg}{k}\right]ds$$

This gives

$$\boxed{x(t)=10+\frac{m}{k}\left(v_0+\frac{mg}{k}\right)\left(1-e^{-\frac{k}{m}t}\right)-\frac{mg}{k}t}$$

---

### Step 3. Maximum height

Maximum height occurs when

$$v(t)=0$$

So:

$$\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k}=0$$

$$e^{-\frac{k}{m}t}=\frac{mg}{kv_0+mg}$$

Thus

$$\boxed{t_{\max}=\frac{m}{k}\ln\left(\frac{kv_0+mg}{mg}\right)}$$

Then substitute into $x(t)$ to get the maximum height:

$$\boxed{x_{\max}=10+\frac{m}{k}\left(v_0+\frac{mg}{k}\right)\left(1-e^{-\frac{k}{m}t_{\max}}\right)-\frac{mg}{k}t_{\max}}$$

---

### Step 4. Compare with no drag

Without drag, the equation is

$$\frac{dv}{dt}=-g$$

Then

$$v(t)=v_0-gt$$

and the maximum additional height is

$$\Delta h=\frac{v_0^2}{2g}$$

So drag makes the object:
- rise for a shorter time
- reach a lower maximum height

---

## Final Answer

Velocity:

$$\boxed{v(t)=\left(v_0+\frac{mg}{k}\right)e^{-\frac{k}{m}t}-\frac{mg}{k}}$$

Position:

$$\boxed{x(t)=10+\frac{m}{k}\left(v_0+\frac{mg}{k}\right)\left(1-e^{-\frac{k}{m}t}\right)-\frac{mg}{k}t}$$

Time of maximum height:

$$\boxed{t_{\max}=\frac{m}{k}\ln\left(\frac{kv_0+mg}{mg}\right)}$$

Drag gives a lower maximum height than the no-drag case.
