## 1. Projectile Motion

A projectile is fired from the ground with initial speed

$$v_0=100\text{ m/s}$$

at an angle

$$\theta=37^\circ$$

above the horizontal. Assume no air resistance.

We need to:

- derive the differential equations of motion
- determine the time of flight
- determine the maximum height
- determine the range

---

## Useful Definitions and Formulas

In projectile motion, the initial velocity is split into two components:

$$v_{0x}=v_0\cos\theta$$

$$v_{0y}=v_0\sin\theta$$

Without air resistance, the accelerations are:

$$a_x=0$$

$$a_y=-g$$

where

$$g=9.8\text{ m/s}^2$$

Since acceleration is the second derivative of position, the differential equations are:

$$\frac{d^2x}{dt^2}=0$$

$$\frac{d^2y}{dt^2}=-g$$

After integration, the position equations are:

$$x(t)=v_{0x}t$$

$$y(t)=v_{0y}t-\frac{1}{2}gt^2$$

Useful formulas:

$$T=\frac{2v_{0y}}{g}$$

$$H=\frac{v_{0y}^2}{2g}$$

$$R=v_{0x}T$$

---

## Step-by-Step Solution

### Step 1. Resolve the initial velocity into components

Given:

$$v_0=100\text{ m/s}$$

$$\theta=37^\circ$$

Horizontal component:

$$v_{0x}=100\cos37^\circ$$

Vertical component:

$$v_{0y}=100\sin37^\circ$$

Using approximate values

$$\cos37^\circ\approx0.799$$

$$\sin37^\circ\approx0.602$$

we get

$$v_{0x}\approx100(0.799)=79.9\text{ m/s}$$

$$v_{0y}\approx100(0.602)=60.2\text{ m/s}$$

---

### Step 2. Derive the differential equations of motion

In the horizontal direction there is no acceleration, so

$$\frac{d^2x}{dt^2}=0$$

In the vertical direction the acceleration is due to gravity, so

$$\frac{d^2y}{dt^2}=-g$$

These are the required differential equations.

---

### Step 3. Write the equations of motion

Horizontal position:

$$x(t)=v_{0x}t$$

So

$$x(t)=100\cos37^\circ\cdot t\approx79.9t$$

Vertical position:

$$y(t)=v_{0y}t-\frac{1}{2}gt^2$$

So

$$y(t)=100\sin37^\circ\cdot t-\frac{1}{2}gt^2$$

$$y(t)\approx60.2t-4.9t^2$$

---

### Step 4. Determine the time of flight

The projectile lands when it returns to the ground, so

$$y(t)=0$$

Using the formula

$$T=\frac{2v_{0y}}{g}$$

we get

$$T=\frac{2(60.2)}{9.8}$$

$$T=\frac{120.4}{9.8}\approx12.29\text{ s}$$

So the time of flight is

$$\boxed{T\approx12.29\text{ s}}$$

---

### Step 5. Determine the maximum height

Use

$$H=\frac{v_{0y}^2}{2g}$$

Substitute the values:

$$H=\frac{(60.2)^2}{2(9.8)}$$

$$H=\frac{3624.04}{19.6}\approx184.90\text{ m}$$

So the maximum height is

$$\boxed{H\approx184.90\text{ m}}$$

---

### Step 6. Determine the range

Use

$$R=v_{0x}T$$

Substitute the values:

$$R\approx79.9\times12.29$$

$$R\approx981.97\text{ m}$$

So the range is

$$\boxed{R\approx981.97\text{ m}}$$

---

## Final Answers

Differential equations:

$$\boxed{\frac{d^2x}{dt^2}=0}$$

$$\boxed{\frac{d^2y}{dt^2}=-g}$$

Time of flight:

$$\boxed{T\approx12.29\text{ s}}$$

Maximum height:

$$\boxed{H\approx184.90\text{ m}}$$

Range:

$$\boxed{R\approx981.97\text{ m}}$$

...
