## 11. Dynamics with a Time-Dependent Force

A particle has mass

$$m=3\text{ kg}$$

and force

$$\vec F=(15t,\;3t-12,\;-6t^2)$$

with initial conditions

$$\vec r(0)=(5,2,-3),\qquad \vec v(0)=(2,0,1)$$

We need position and velocity as functions of time.

---

## Useful Definitions and Formulas

By Newton's second law,

$$\vec F=m\vec a$$

So

$$\vec a=\frac{\vec F}{m}$$

Then integrate acceleration to get velocity, and integrate velocity to get position.

---

## Step-by-Step Solution

### Step 1. Find acceleration

$$\vec a(t)=\frac{1}{3}(15t,\;3t-12,\;-6t^2)$$

$$\vec a(t)=(5t,\;t-4,\;-2t^2)$$

---

### Step 2. Find velocity

Integrate componentwise.

For $x$:

$$v_x=\int5t\,dt=\frac{5}{2}t^2+C_1$$

Use $v_x(0)=2$:

$$C_1=2$$

So

$$v_x=\frac{5}{2}t^2+2$$

For $y$:

$$v_y=\int(t-4)\,dt=\frac{1}{2}t^2-4t+C_2$$

Use $v_y(0)=0$:

$$C_2=0$$

So

$$v_y=\frac{1}{2}t^2-4t$$

For $z$:

$$v_z=\int(-2t^2)\,dt=-\frac{2}{3}t^3+C_3$$

Use $v_z(0)=1$:

$$C_3=1$$

So

$$v_z=-\frac{2}{3}t^3+1$$

Thus

$$\boxed{\vec v(t)=\left(\frac{5}{2}t^2+2,\;\frac{1}{2}t^2-4t,\;-\frac{2}{3}t^3+1\right)}$$

---

### Step 3. Find position

Integrate velocity.

For $x$:

$$x=\int\left(\frac{5}{2}t^2+2\right)dt=\frac{5}{6}t^3+2t+C_4$$

Use $x(0)=5$:

$$C_4=5$$

So

$$x=\frac{5}{6}t^3+2t+5$$

For $y$:

$$y=\int\left(\frac{1}{2}t^2-4t\right)dt=\frac{1}{6}t^3-2t^2+C_5$$

Use $y(0)=2$:

$$C_5=2$$

So

$$y=\frac{1}{6}t^3-2t^2+2$$

For $z$:

$$z=\int\left(-\frac{2}{3}t^3+1\right)dt=-\frac{1}{6}t^4+t+C_6$$

Use $z(0)=-3$:

$$C_6=-3$$

So

$$z=-\frac{1}{6}t^4+t-3$$

Thus

$$\boxed{\vec r(t)=\left(\frac{5}{6}t^3+2t+5,\;\frac{1}{6}t^3-2t^2+2,\;-\frac{1}{6}t^4+t-3\right)}$$

---

## Final Answer

Velocity:

$$\boxed{\vec v(t)=\left(\frac{5}{2}t^2+2,\;\frac{1}{2}t^2-4t,\;-\frac{2}{3}t^3+1\right)}$$

Position:

$$\boxed{\vec r(t)=\left(\frac{5}{6}t^3+2t+5,\;\frac{1}{6}t^3-2t^2+2,\;-\frac{1}{6}t^4+t-3\right)}$$
