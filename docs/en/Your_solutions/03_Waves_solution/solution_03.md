## 3. Superposition Principle

### Useful definitions and formulas

We are given two waves:

$$y_1(x,t)=A\sin(kx-\omega t)$$

$$y_2(x,t)=A\sin(kx+\omega t)$$

The total displacement is the sum of the two waves:

$$y(x,t)=y_1(x,t)+y_2(x,t)$$

To combine the two sine functions, we use the identity:

$$\sin\alpha+\sin\beta=2\sin\frac{\alpha+\beta}{2}\cos\frac{\alpha-\beta}{2}$$

A standing wave usually has the form:

$$y(x,t)=\text{space part}\cdot\text{time part}$$

Nodes are points where the displacement is always zero.

---

### Step-by-step solution

We add the two waves:

$$y(x,t)=A\sin(kx-\omega t)+A\sin(kx+\omega t)$$

Factor out $A$:

$$y(x,t)=A\Big[\sin(kx-\omega t)+\sin(kx+\omega t)\Big]$$

Now use the identity.

Let:

$$\alpha=kx-\omega t$$

$$\beta=kx+\omega t$$

Then:

$$\frac{\alpha+\beta}{2}=\frac{(kx-\omega t)+(kx+\omega t)}{2}=\frac{2kx}{2}=kx$$

and

$$\frac{\alpha-\beta}{2}=\frac{(kx-\omega t)-(kx+\omega t)}{2}=\frac{-2\omega t}{2}=-\omega t$$

So:

$$\sin\alpha+\sin\beta=2\sin(kx)\cos(-\omega t)$$

Since cosine is an even function:

$$\cos(-\omega t)=\cos(\omega t)$$

So the result becomes:

$$y(x,t)=2A\sin(kx)\cos(\omega t)$$

---

### Resulting standing wave

$$y(x,t)=2A\sin(kx)\cos(\omega t)$$

Explanation:

- $\sin(kx)$ depends only on position
- $\cos(\omega t)$ depends only on time
- this is the standard form of a standing wave

---

### Find the positions of the nodes

Nodes are the points where the displacement is always zero.

From

$$y(x,t)=2A\sin(kx)\cos(\omega t)$$

the displacement is always zero if:

$$\sin(kx)=0$$

This happens when:

$$kx=n\pi$$

where:

- $n=0,1,2,3,\dots$

Now solve for $x$:

$$x=\frac{n\pi}{k}$$

We also know:

$$k=\frac{2\pi}{\lambda}$$

Substitute into the formula for $x$:

$$x=\frac{n\pi}{2\pi/\lambda}$$

Dividing by a fraction means multiplying by its reciprocal:

$$x=n\pi\cdot\frac{\lambda}{2\pi}$$

Now $\pi$ cancels:

$$x=\frac{n\lambda}{2}$$

---

### Final answer

The standing wave is:

$$y(x,t)=2A\sin(kx)\cos(\omega t)$$

The nodes are at:

$$x=\frac{n\lambda}{2},\qquad n=0,1,2,3,\dots$$
