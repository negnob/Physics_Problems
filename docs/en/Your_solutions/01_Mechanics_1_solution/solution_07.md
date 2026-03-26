## 7. Elimination of Time and Interpretation of Acceleration

The path is given by

$$x(t)=2t^2,\qquad y(t)=3t^3$$

We need to eliminate $t$, describe the trajectory, and find velocity and acceleration.

---

## Useful Definitions and Formulas

Velocity vector:

$$\vec v(t)=\left(\frac{dx}{dt},\frac{dy}{dt}\right)$$

Speed:

$$|\vec v(t)|=\sqrt{\left(\frac{dx}{dt}\right)^2+\left(\frac{dy}{dt}\right)^2}$$

Acceleration vector:

$$\vec a(t)=\left(\frac{d^2x}{dt^2},\frac{d^2y}{dt^2}\right)$$

Magnitude of acceleration:

$$|\vec a(t)|=\sqrt{a_x^2+a_y^2}$$

---

## Step-by-Step Solution

### Step 1. Eliminate the parameter

From

$$x=2t^2$$

we get

$$t^2=\frac{x}{2}$$

Now square $y$:

$$y=3t^3$$

$$y^2=9t^6$$

But

$$t^6=(t^2)^3=\left(\frac{x}{2}\right)^3$$

So

$$y^2=9\left(\frac{x}{2}\right)^3=\frac{9x^3}{8}$$

Therefore the trajectory is

$$\boxed{y^2=\frac{9x^3}{8}}$$

---

### Step 2. Describe the trajectory

This is a semicubical parabola.  
Since $x=2t^2\geq0$, the curve lies only in the right half-plane.  
For positive $t$, $y>0$; for negative $t$, $y<0$.

---

### Step 3. Find velocity vector

Differentiate:

$$\frac{dx}{dt}=4t$$

$$\frac{dy}{dt}=9t^2$$

So

$$\boxed{\vec v(t)=(4t,9t^2)}$$

---

### Step 4. Find speed

$$|\vec v(t)|=\sqrt{(4t)^2+(9t^2)^2}$$

$$|\vec v(t)|=\sqrt{16t^2+81t^4}$$

$$|\vec v(t)|=\boxed{\sqrt{16t^2+81t^4}}$$

---

### Step 5. Find acceleration vector

Differentiate again:

$$\frac{d^2x}{dt^2}=4$$

$$\frac{d^2y}{dt^2}=18t$$

So

$$\boxed{\vec a(t)=(4,18t)}$$

---

### Step 6. Find acceleration magnitude

$$|\vec a(t)|=\sqrt{4^2+(18t)^2}$$

$$|\vec a(t)|=\sqrt{16+324t^2}$$

So

$$\boxed{|\vec a(t)|=\sqrt{16+324t^2}}$$

---

### Step 7. Is the acceleration constant?

No, because

$$\vec a(t)=(4,18t)$$

depends on $t$ through the second component.  
So the acceleration is **not constant**.

---

## Final Answer

$$\boxed{y^2=\frac{9x^3}{8}}$$

$$\boxed{\vec v(t)=(4t,9t^2)}$$

$$\boxed{|\vec v(t)|=\sqrt{16t^2+81t^4}}$$

$$\boxed{\vec a(t)=(4,18t)}$$

$$\boxed{|\vec a(t)|=\sqrt{16+324t^2}}$$

Acceleration is **not constant**.
