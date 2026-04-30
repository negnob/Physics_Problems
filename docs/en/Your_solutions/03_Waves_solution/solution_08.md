## 8. Waves
Which of the following functions can describe a traveling wave? Hint: check if it satisfies the wave equation 

$$\frac{\partial^2 y}{\partial x^2} = \frac{1}{v^2} \frac{\partial^2 y}{\partial t^2}$$

a) $y(x,t) = A \cos(kx^2 - \omega t)$

b) $y(x,t) = A(x-vt)^2$

c) $y(x,t) = A \log(x+vt)$

---

### Useful definitions and formulas

A traveling wave is a wave that moves through space without changing its shape.

The wave equation is:

$$\frac{\partial^2 y}{\partial x^2}=\frac{1}{v^2}\frac{\partial^2 y}{\partial t^2}$$

where:

- $y(x,t)$ is the displacement of the wave
- $x$ is position
- $t$ is time
- $v$ is the wave speed
- $\frac{\partial^2 y}{\partial x^2}$ shows how the wave changes in space
- $\frac{\partial^2 y}{\partial t^2}$ shows how the wave changes in time

A very useful rule is:

$$y(x,t)=f(x-vt)$$

or

$$y(x,t)=f(x+vt)$$

These forms describe traveling waves.

Why?

- $x-vt$ means the wave moves to the right
- $x+vt$ means the wave moves to the left

So, to solve this problem, we check whether each function can be written as a function of only $x-vt$ or only $x+vt$.

---

## a) $y(x,t)=A\cos(kx^2-\omega t)$

The expression inside the cosine is:

$$kx^2-\omega t$$

Here we have $x^2$, not just $x$.

A standard traveling wave should depend on:

$$x-vt$$

or

$$x+vt$$

But this function depends on $x^2$.

Because of this, it cannot be written as:

$$f(x-vt)$$

or

$$f(x+vt)$$

So the shape of the wave does not simply move without changing.

### Conclusion for a)

$$y(x,t)=A\cos(kx^2-\omega t)$$

cannot describe a standard traveling wave.

---

## b) $y(x,t)=A(x-vt)^2$

This function depends only on:

$$x-vt$$

We can write:

$$y(x,t)=f(x-vt)$$

where:

$$f(z)=Az^2$$

and:

$$z=x-vt$$

This is exactly the form of a traveling wave moving to the right.

### Conclusion for b)

$$y(x,t)=A(x-vt)^2$$

can describe a traveling wave.

It moves to the right.

---

## c) $y(x,t)=A\log(x+vt)$

This function depends only on:

$$x+vt$$

We can write:

$$y(x,t)=f(x+vt)$$

where:

$$f(z)=A\log z$$

and:

$$z=x+vt$$

This is exactly the form of a traveling wave moving to the left.

One small condition is that the logarithm is defined only when:

$$x+vt>0$$

But this condition does not change the fact that the function has the form of a traveling wave.

### Conclusion for c)

$$y(x,t)=A\log(x+vt)$$

can describe a traveling wave.

It moves to the left.

---

## Final answer

The functions that can describe traveling waves are:

### b)

$$y(x,t)=A(x-vt)^2$$

This wave moves to the right.

<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/14e0254d-68cb-43de-a18a-6cf70803e575" />


### c)

$$y(x,t)=A\log(x+vt)$$

This wave moves to the left.

<img width="565" height="455" alt="image" src="https://github.com/user-attachments/assets/3164a9fc-96dd-474c-b8b6-395304036551" />


The function that cannot describe a standard traveling wave is:

### a)

$$y(x,t)=A\cos(kx^2-\omega t)$$

because it contains $x^2$ and cannot be written as $f(x-vt)$ or $f(x+vt)$.

<img width="587" height="455" alt="image" src="https://github.com/user-attachments/assets/4405ee7e-c6a5-46d6-abee-0366ba41de8a" />

