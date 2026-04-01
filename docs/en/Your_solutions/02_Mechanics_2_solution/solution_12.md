## 12. Work and Energy with a Constant Force

A body has mass

$$m=2\text{ kg}$$

and constant force

$$\vec F=[6,2]\text{ N}$$

Initial conditions:

$$\vec v(0)=(1,-1)\text{ m/s}$$

$$\vec r(0)=(0,0)\text{ m}$$

We need:
- $\vec a(t)$
- $\vec v(t)$
- $\vec r(t)$
- trajectory
- work at $t=3\text{ s}$
- check work-energy theorem

---

## Useful Definitions and Formulas

Newton's second law:

$$\vec a=\frac{\vec F}{m}$$

Velocity:

$$\vec v(t)=\vec v_0+\vec a t$$

Position:

$$\vec r(t)=\vec r_0+\vec v_0t+\frac{1}{2}\vec a t^2$$

Work:

$$W=\vec F\cdot\Delta\vec r$$

Kinetic energy:

$$K=\frac{1}{2}mv^2$$

---

## Step-by-Step Solution

### Step 1. Acceleration

$$\vec a=\frac{1}{2}[6,2]=[3,1]$$

So

$$\boxed{\vec a(t)=(3,1)}$$

It is constant.

---

### Step 2. Velocity

$$\vec v(t)=\vec v_0+\vec a t=(1,-1)+(3,1)t$$

So

$$\boxed{\vec v(t)=(1+3t,\,-1+t)}$$

---

### Step 3. Position

$$\vec r(t)=\vec r_0+\vec v_0t+\frac{1}{2}\vec a t^2$$

$$\vec r(t)=(0,0)+(1,-1)t+\frac{1}{2}(3,1)t^2$$

So

$$\boxed{\vec r(t)=\left(t+\frac{3}{2}t^2,\;-t+\frac{1}{2}t^2\right)}$$

---

### Step 4. Trajectory

From

$$y=-t+\frac{1}{2}t^2$$

we get

$$t^2=2y+2t$$

From

$$x=t+\frac{3}{2}t^2$$

substitute $t^2$:

$$x=t+\frac{3}{2}(2y+2t)=t+3y+3t=4t+3y$$

So

$$t=\frac{x-3y}{4}$$

This gives the trajectory implicitly. It is a parabola.

---

### Step 5. Work at $t=3$

First find displacement:

$$\vec r(3)=\left(3+\frac{3}{2}\cdot9,\;-3+\frac{1}{2}\cdot9\right)=(16.5,1.5)$$

Since initial position is $(0,0)$,

$$\Delta\vec r=(16.5,1.5)$$

Work:

$$W=\vec F\cdot\Delta\vec r=(6,2)\cdot(16.5,1.5)$$

$$W=6(16.5)+2(1.5)=99+3=102\text{ J}$$

So

$$\boxed{W=102\text{ J}}$$

---

### Step 6. Check work-energy theorem

Initial kinetic energy:

$$K_i=\frac{1}{2}(2)\left(1^2+(-1)^2\right)=1\cdot2=2\text{ J}$$

Velocity at $t=3$:

$$\vec v(3)=(10,2)$$

Final kinetic energy:

$$K_f=\frac{1}{2}(2)(10^2+2^2)=1(100+4)=104\text{ J}$$

So

$$\Delta K=K_f-K_i=104-2=102\text{ J}$$

This matches the work:

$$W=\Delta K=102\text{ J}$$

So the work-energy theorem is verified.

---

## Final Answer

$$\boxed{\vec a(t)=(3,1)}$$

$$\boxed{\vec v(t)=(1+3t,\,-1+t)}$$

$$\boxed{\vec r(t)=\left(t+\frac{3}{2}t^2,\;-t+\frac{1}{2}t^2\right)}$$

Work at $t=3$:

$$\boxed{W=102\text{ J}}$$

And indeed,

$$\boxed{W=\Delta K}$$
