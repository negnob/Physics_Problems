## 9. Optimization Problem

A rectangle is under the curve

$$y=3-x^2$$

in the first quadrant. We need to find the dimensions of the rectangle with the maximum area.

---

## Useful Definitions and Formulas

### 1. Area of a rectangle
The area of a rectangle is

$$A=\text{width}\cdot\text{height}$$

So to maximize the rectangle, we need a formula for its width and height.

---

### 2. First quadrant
The first quadrant means

$$x\geq0,\qquad y\geq0$$

So we only work with positive values of $x$ and $y$.

---

### 3. Optimization idea
To solve an optimization problem:

1. write the quantity to maximize as a function
2. differentiate it
3. find critical points by setting the derivative equal to zero
4. check which point gives the maximum value

---

### 4. Derivative test
If

$$A'(x)=0$$

at some point, that point is a critical point.

Then we check whether it gives a maximum.

---

## Step-by-Step Solution

### Step 1. Describe the rectangle

Let the upper-right corner of the rectangle be at the point

$$(x,y)$$

on the curve

$$y=3-x^2$$

Because the rectangle is in the first quadrant and its sides are along the axes:

- the width is $x$
- the height is $y=3-x^2$

So the area is

$$A(x)=x(3-x^2)$$

---

### Step 2. Simplify the area function

Multiply out:

$$A(x)=3x-x^3$$

This is the function we want to maximize.

---

### Step 3. Find the derivative

Differentiate:

$$A'(x)=3-3x^2$$

---

### Step 4. Find critical points

Set the derivative equal to zero:

$$3-3x^2=0$$

Divide both sides by $3$:

$$1-x^2=0$$

$$x^2=1$$

$$x=1$$

We take $x=1$ because we are in the first quadrant.

---

### Step 5. Find the corresponding height

Substitute $x=1$ into the curve:

$$y=3-x^2$$

$$y=3-1^2$$

$$y=3-1=2$$

So the height is

$$2$$

---

### Step 6. Confirm that this gives a maximum

The second derivative is

$$A''(x)=-6x$$

At $x=1$:

$$A''(1)=-6<0$$

So the area is maximized at this point.

---

## Final Answer

The rectangle with maximum area has dimensions

$$\boxed{1\times2}$$

So:
- width $=1$
- height $=2$

The maximum area is

$$\boxed{2}$$
