## 9. Damped Oscillator

### Useful definitions and formulas

The equation is:

$$m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=0$$

where:

- $m$ is the mass
- $b$ is the damping coefficient
- $k$ is the spring constant
- $x$ is the displacement
- $\frac{dx}{dt}$ is velocity
- $\frac{d^2x}{dt^2}$ is acceleration

This equation describes an oscillator with damping, which means:
- the mass moves back and forth
- but some energy is lost
- so the motion gradually decreases

---

### 1) General solution

We solve the equation using the standard method for linear differential equations.

We try a solution of the form:

$$x(t)=e^{rt}$$

Then:

$$\frac{dx}{dt}=re^{rt}$$

$$\frac{d^2x}{dt^2}=r^2e^{rt}$$

Substitute into the differential equation:

$$m(r^2e^{rt})+b(re^{rt})+k(e^{rt})=0$$

Factor out $e^{rt}$:

$$e^{rt}(mr^2+br+k)=0$$

Since $e^{rt}\neq0$, we get the characteristic equation:

$$mr^2+br+k=0$$

Use the quadratic formula:

$$r=\frac{-b\pm\sqrt{b^2-4mk}}{2m}$$

Now the type of solution depends on the discriminant:

$$\Delta=b^2-4mk$$

---

### 2) Classification of cases

#### Underdamped case

If:

$$b^2<4mk$$

then the roots are complex.

The solution is:

$$x(t)=e^{-\frac{b}{2m}t}\Big(C_1\cos(\omega_d t)+C_2\sin(\omega_d t)\Big)$$

where:

$$\omega_d=\sqrt{\frac{k}{m}-\frac{b^2}{4m^2}}$$

Explanation:

- the system still oscillates
- but the amplitude gets smaller with time
- this is oscillation with decay

---

#### Critically damped case

If:

$$b^2=4mk$$

then the roots are equal.

The solution is:

$$x(t)=(C_1+C_2 t)e^{-\frac{b}{2m}t}$$

Explanation:

- the system does not oscillate
- it returns to equilibrium as fast as possible without overshooting

---

#### Overdamped case

If:

$$b^2>4mk$$

then the roots are real and different:

$$r_{1,2}=\frac{-b\pm\sqrt{b^2-4mk}}{2m}$$

The solution is:

$$x(t)=C_1e^{r_1 t}+C_2e^{r_2 t}$$

Explanation:

- the system does not oscillate
- it returns to equilibrium more slowly than the critically damped case

---

### 3) Numerical solution using RK4

To solve numerically, we change the second-order equation into two first-order equations.

Let:

$$v=\frac{dx}{dt}$$

Then:

$$\frac{dx}{dt}=v$$

and from the original equation:

$$m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=0$$

divide every term by $m$:

$$\frac{d^2x}{dt^2}+\frac{b}{m}\frac{dx}{dt}+\frac{k}{m}x=0$$

Since $\frac{d^2x}{dt^2}=\frac{dv}{dt}$ and $\frac{dx}{dt}=v$, we get:

$$\frac{dv}{dt}=-\frac{b}{m}v-\frac{k}{m}x$$

So the system becomes:

$$\frac{dx}{dt}=v$$

$$\frac{dv}{dt}=-\frac{b}{m}v-\frac{k}{m}x$$

These are the equations used in the RK4 method.

---

### 4) Effect of parameter $b$

The parameter $b$ controls damping.

- small $b$ $\rightarrow$ weak damping $\rightarrow$ oscillations continue for a long time
- medium $b$ $\rightarrow$ critical damping $\rightarrow$ fastest return without oscillation
- large $b$ $\rightarrow$ strong damping $\rightarrow$ slow return without oscillation

So when $b$ increases:
- oscillations become weaker
- the phase portrait changes shape
- the graph of $x(t)$ changes from oscillating to non-oscillating

---

### 5) Graph of $x(t)$

The graph of $x(t)$ shows:
- how the position changes with time
- whether the system oscillates
- how fast the amplitude decreases

---

### 6) Phase portrait

The phase portrait is a graph of:

$$v\text{ versus }x$$

This shows:
- the relation between position and velocity
- how the system moves in phase space
- spirals for underdamped motion
- direct decay for critical and overdamped motion
