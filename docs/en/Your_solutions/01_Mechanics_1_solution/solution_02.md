## 2. Range Optimization

For projectile motion, the range is given by

$$R(\theta)=\frac{v_0^2\sin(2\theta)}{g}$$

We need to show analytically that the maximum range is achieved at a launch angle of

$$45^\circ$$

for a given initial velocity.

---

## Useful Definitions and Formulas

For this problem, $v_0$ and $g$ are constants.  
So the only part of the formula that changes with $\theta$ is

$$\sin(2\theta)$$

That means maximizing $R(\theta)$ is the same as maximizing

$$\sin(2\theta)$$

We also use the fact that:

- the maximum value of $\sin x$ is $1$
- this happens when

$$x=90^\circ$$

We can also confirm the result using differentiation.

---

## Step-by-Step Solution

### Step 1. Write the range formula

The range is

$$R(\theta)=\frac{v_0^2\sin(2\theta)}{g}$$

Since $\frac{v_0^2}{g}$ is constant, the range depends only on $\sin(2\theta)$.

So to get the maximum range, we need the maximum value of

$$\sin(2\theta)$$

---

### Step 2. Use the maximum value of sine

We know that

$$\sin(2\theta)\leq1$$

and the maximum value is reached when

$$\sin(2\theta)=1$$

This happens when

$$2\theta=90^\circ$$

Now divide both sides by $2$:

$$\theta=45^\circ$$

So the range is maximum when the launch angle is

$$\boxed{45^\circ}$$

---

### Step 3. Confirm by differentiation

Start with

$$R(\theta)=\frac{v_0^2\sin(2\theta)}{g}$$

Differentiate with respect to $\theta$:

$$R'(\theta)=\frac{v_0^2}{g}\cdot2\cos(2\theta)$$

So

$$R'(\theta)=\frac{2v_0^2\cos(2\theta)}{g}$$

To find critical points, set the derivative equal to zero:

$$\frac{2v_0^2\cos(2\theta)}{g}=0$$

Since $\frac{2v_0^2}{g}\neq0$, we get

$$\cos(2\theta)=0$$

This happens when

$$2\theta=90^\circ$$

Therefore

$$\theta=45^\circ$$

---

### Step 4. Show that this is a maximum

Differentiate again:

$$R''(\theta)=\frac{2v_0^2}{g}\cdot(-2\sin(2\theta))$$

So

$$R''(\theta)=-\frac{4v_0^2\sin(2\theta)}{g}$$

Now substitute

$$\theta=45^\circ$$

Then

$$2\theta=90^\circ$$

and

$$\sin(90^\circ)=1$$

So

$$R''(45^\circ)=-\frac{4v_0^2}{g}<0$$

Since the second derivative is negative, the range is maximum at

$$\boxed{45^\circ}$$

---

## Final Answer

For a given initial velocity, the range

$$R(\theta)=\frac{v_0^2\sin(2\theta)}{g}$$

is maximized when

$$\boxed{\theta=45^\circ}$$
