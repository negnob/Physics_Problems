## 8. Definite Integrals

Calculate the area under the curve of the function

$$f(x)=\sin(x)$$

$$from$$

$$x=0$$

$$to$$

$$x=\pi$$

---

## Useful Definitions and Formulas

### 1. Definite integral
A **definite integral** gives the signed area under a curve between two limits.

For a function $f(x)$ from $x=a$ to $x=b$:

$$\int_a^bf(x)\,dx$$

If the function is above the $x$-axis on that interval, then this integral is the actual area.

---

### 2. Antiderivative
To evaluate a definite integral, we first find the **antiderivative** of the function.

For $\sin(x)$:

$$\int\sin(x)\,dx=-\cos(x)+C$$

---

### 3. Fundamental Theorem of Calculus
If $F(x)$ is an antiderivative of $f(x)$, then

$$\int_a^bf(x)\,dx=F(b)-F(a)$$

This means:
- find the antiderivative
- plug in the upper limit
- subtract the value at the lower limit

---

## Step-by-Step Solution

We want to calculate

$$\int_0^\pi\sin(x)\,dx$$

---

### Step 1. Find the antiderivative of $\sin(x)$

We know that

$$\int\sin(x)\,dx=-\cos(x)$$

So

$$\int_0^\pi\sin(x)\,dx=\left[-\cos(x)\right]_0^\pi$$

---

### Step 2. Substitute the limits

Now evaluate at the upper and lower limits:

$$\left[-\cos(x)\right]_0^\pi=-\cos(\pi)-\left(-\cos(0)\right)$$

---

### Step 3. Use the cosine values

Recall that

$$\cos(\pi)=-1$$

$$\cos(0)=1$$

Substitute these values:

$$-\cos(\pi)-\left(-\cos(0)\right)=-(-1)-(-1)$$

$$=1+1$$

$$=2$$

---

## Final Answer

The area under the curve is

$$\boxed{2}$$