## 10. Infinite Series

An ant starts at the origin and moves in the pattern:

- $1$ m east
- $\frac{1}{2}$ m north
- $\frac{1}{3}$ m west
- $\frac{1}{4}$ m south
- $\frac{1}{5}$ m east
- and so on.

We need to determine its final position.

---

## Useful Definitions and Formulas

### 1. Position in the plane
The ant’s final position can be written as

$$\left(x,y\right)$$

where:
- $x$ is the total horizontal displacement
- $y$ is the total vertical displacement

---

### 2. Alternating series
An alternating series is a series whose terms change sign:

$$a_1-a_2+a_3-a_4+\dots$$

A very important example is the alternating harmonic series:

$$1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\frac{1}{5}-\dots=\ln2$$

We will use this idea, but split the motion into horizontal and vertical parts.

---

### 3. Separate horizontal and vertical motion
Since east/west affects only $x$, and north/south affects only $y$, we can calculate:

- the total $x$-displacement separately
- the total $y$-displacement separately

Then combine them into the final point.

---

## Step-by-Step Solution

### Step 1. Write the horizontal displacement

Horizontal moves happen on the $1$st, $3$rd, $5$th, $7$th, ... steps:

- $1$ m east
- $\frac{1}{3}$ m west
- $\frac{1}{5}$ m east
- $\frac{1}{7}$ m west
- and so on

So the horizontal displacement is

$$x=1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\dots$$

This is the well-known series

$$1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\dots=\frac{\pi}{4}$$

Therefore

$$x=\frac{\pi}{4}$$

---

### Step 2. Write the vertical displacement

Vertical moves happen on the $2$nd, $4$th, $6$th, $8$th, ... steps:

- $\frac{1}{2}$ m north
- $\frac{1}{4}$ m south
- $\frac{1}{6}$ m north
- $\frac{1}{8}$ m south
- and so on

So the vertical displacement is

$$y=\frac{1}{2}-\frac{1}{4}+\frac{1}{6}-\frac{1}{8}+\dots$$

Factor out $\frac{1}{2}$:

$$y=\frac{1}{2}\left(1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\dots\right)$$

But we know that

$$1-\frac{1}{2}+\frac{1}{3}-\frac{1}{4}+\dots=\ln2$$

So

$$y=\frac{1}{2}\ln2$$

---

### Step 3. Write the final position

Now combine the horizontal and vertical components:

$$\left(x,y\right)=\left(\frac{\pi}{4},\frac{1}{2}\ln2\right)$$

---

## Final Answer

The ant’s final position is

$$\boxed{\left(\frac{\pi}{4},\frac{1}{2}\ln2\right)}$$

So it ends:
- $\frac{\pi}{4}$ m to the east
- $\frac{1}{2}\ln2$ m to the north
