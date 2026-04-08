## 8. Waves

### Useful definitions and formulas

A function describes a traveling wave if it satisfies the wave equation:

$$\frac{\partial^2 y}{\partial x^2}=\frac{1}{v^2}\frac{\partial^2 y}{\partial t^2}$$

A very useful fact is this:

Any function of the form

$$y(x,t)=f(x-vt)$$

or

$$y(x,t)=f(x+vt)$$

describes a traveling wave.

Why?

Because the shape stays the same and just moves:
- $x-vt$ means the wave moves to the right
- $x+vt$ means the wave moves to the left

So in practice, we check whether the function depends only on:
- $x-vt$, or
- $x+vt$

---

### a) $y(x,t)=A\cos(kx^2-\omega t)$

Look at the inside:

$$kx^2-\omega t$$

This has $x^2$, not just $x$.

That means the function is **not** of the form:

$$f(x-vt)$$

or

$$f(x+vt)$$

So this is **not** a standard traveling wave solution.

#### Conclusion for a)

$$y(x,t)=A\cos(kx^2-\omega t)$$

**cannot describe a traveling wave**

---

### b) $y(x,t)=A(x-vt)^2$

This can be written as:

$$y(x,t)=f(x-vt)$$

where:

$$f(z)=Az^2$$

Since it depends only on $x-vt$, it is a traveling wave.

#### Conclusion for b)

$$y(x,t)=A(x-vt)^2$$

**can describe a traveling wave**

---

### c) $y(x,t)=A\log(x+vt)$

This can be written as:

$$y(x,t)=f(x+vt)$$

where:

$$f(z)=A\log z$$

Since it depends only on $x+vt$, it is also a traveling wave.

#### Conclusion for c)

$$y(x,t)=A\log(x+vt)$$

**can describe a traveling wave**

---

### Final answer

The functions that can describe a traveling wave are:

- **b)** $$y(x,t)=A(x-vt)^2$$
- **c)** $$y(x,t)=A\log(x+vt)$$

The function that cannot describe a traveling wave is:

- **a)** $$y(x,t)=A\cos(kx^2-\omega t)$$
