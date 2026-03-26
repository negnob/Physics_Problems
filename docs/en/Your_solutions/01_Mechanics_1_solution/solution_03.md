## 3. Path Intersection

Alice moves along

$$A(t)=(2+t,8-3t)$$

and Bob moves along

$$B(t)=(2t-1,2t+2)$$

We need to check whether they collide. If not, we find the minimum distance and when it occurs.

---

## Useful Definitions and Formulas

Two moving points collide if their positions are equal at the same time:

$$A(t)=B(t)$$

If they do not collide, the distance between them is found from the difference vector:

$$D(t)=A(t)-B(t)$$

and the squared distance is

$$d^2(t)=|D(t)|^2$$

It is easier to minimize $d^2(t)$ than $d(t)$.

---

## Step-by-Step Solution

### Step 1. Write the coordinates

Alice:

$$x_A=2+t,\qquad y_A=8-3t$$

Bob:

$$x_B=2t-1,\qquad y_B=2t+2$$

---

### Step 2. Check for collision

For a collision, both coordinates must be equal at the same time.

From the $x$-coordinates:

$$2+t=2t-1$$

$$3=t$$

From the $y$-coordinates:

$$8-3t=2t+2$$

$$6=5t$$

$$t=\frac{6}{5}$$

The two times are different, so they do **not** collide.

---

### Step 3. Find the distance between them

Difference vector:

$$D(t)=A(t)-B(t)$$

$$D(t)=\left((2+t)-(2t-1),(8-3t)-(2t+2)\right)$$

$$D(t)=\left(3-t,6-5t\right)$$

So the squared distance is

$$d^2(t)=(3-t)^2+(6-5t)^2$$

Expand:

$$d^2(t)=9-6t+t^2+36-60t+25t^2$$

$$d^2(t)=26t^2-66t+45$$

---

### Step 4. Minimize the squared distance

Differentiate:

$$\frac{d}{dt}d^2(t)=52t-66$$

Set equal to zero:

$$52t-66=0$$

$$t=\frac{66}{52}=\frac{33}{26}$$

So the minimum distance occurs at

$$\boxed{t=\frac{33}{26}}$$

---

### Step 5. Find the minimum distance

Substitute into the difference vector:

$$3-\frac{33}{26}=\frac{45}{26}$$

$$6-5\cdot\frac{33}{26}=6-\frac{165}{26}=-\frac{9}{26}$$

So

$$d_{\min}^2=\left(\frac{45}{26}\right)^2+\left(-\frac{9}{26}\right)^2$$

$$d_{\min}^2=\frac{2025}{676}+\frac{81}{676}=\frac{2106}{676}=\frac{81}{26}$$

Therefore

$$d_{\min}=\sqrt{\frac{81}{26}}=\frac{9}{\sqrt{26}}$$

So the minimum distance is

$$\boxed{\frac{9}{\sqrt{26}}}$$

---

## Final Answer

They do **not** collide.

The minimum distance occurs at

$$\boxed{t=\frac{33}{26}}$$

and the minimum distance is

$$\boxed{d_{\min}=\frac{9}{\sqrt{26}}}$$
