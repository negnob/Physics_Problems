## 9. Damped Oscillator

### Useful definitions and formulas

The equation of a damped harmonic oscillator is:

$$m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=0$$

where:

- $m$ is the mass of the object
- $b$ is the damping coefficient
- $k$ is the spring constant
- $x(t)$ is the displacement
- $\frac{dx}{dt}=v(t)$ is the velocity
- $\frac{d^2x}{dt^2}=a(t)$ is the acceleration

This equation describes motion where the object oscillates, but the amplitude decreases because of damping.

---

### 1. General solution

We start from the equation:

$$m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=0$$

We try the solution:

$$x(t)=e^{rt}$$

Then:

$$\frac{dx}{dt}=re^{rt}$$

$$\frac{d^2x}{dt^2}=r^2e^{rt}$$

Substitute into the equation:

$$mr^2e^{rt}+bre^{rt}+ke^{rt}=0$$

Factor out $e^{rt}$:

$$e^{rt}(mr^2+br+k)=0$$

Since $e^{rt}\neq0$, we get the characteristic equation:

$$mr^2+br+k=0$$

The roots are:

$$r=\frac{-b\pm\sqrt{b^2-4mk}}{2m}$$

The type of motion depends on the discriminant:

$$D=b^2-4mk$$

---

### 2. Classification of cases

#### Underdamped case

If:

$$b^2<4mk$$

then the roots are complex, and the system oscillates while slowly losing energy.

The solution is:

$$x(t)=e^{-\frac{b}{2m}t}(C_1\cos(\omega_dt)+C_2\sin(\omega_dt))$$

where:

$$\omega_d=\sqrt{\frac{k}{m}-\left(\frac{b}{2m}\right)^2}$$

Here:

- $\omega_d$ is the damped angular frequency
- $C_1$ and $C_2$ depend on initial conditions
- the exponential part $e^{-\frac{b}{2m}t}$ makes the amplitude decrease

---

#### Critically damped case

If:

$$b^2=4mk$$

then the system returns to equilibrium as fast as possible without oscillating.

The solution is:

$$x(t)=(C_1+C_2t)e^{-\frac{b}{2m}t}$$

---

#### Overdamped case

If:

$$b^2>4mk$$

then the system returns to equilibrium slowly without oscillating.

The solution is:

$$x(t)=C_1e^{r_1t}+C_2e^{r_2t}$$

where:

$$r_1=\frac{-b+\sqrt{b^2-4mk}}{2m}$$

$$r_2=\frac{-b-\sqrt{b^2-4mk}}{2m}$$

---

### 3. Numerical solution using RK4

To solve the equation numerically, we rewrite it as a system of first-order equations.

Let:

$$v=\frac{dx}{dt}$$

Then:

$$\frac{dx}{dt}=v$$

From the original equation:

$$m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=0$$

we get:

$$m\frac{dv}{dt}+bv+kx=0$$

so:

$$\frac{dv}{dt}=-\frac{b}{m}v-\frac{k}{m}x$$

Therefore, the system is:

$$\frac{dx}{dt}=v$$

$$\frac{dv}{dt}=-\frac{b}{m}v-\frac{k}{m}x$$

This system is solved using the RK4 method.

RK4 is used because it is more accurate than the simple Euler method. It estimates the next position and velocity using four intermediate slopes.

---

### 4. Investigation of parameter $b$

The parameter $b$ controls damping:

- small $b$ means weak damping, so the oscillator keeps moving for longer
- critical $b$ gives the fastest return to equilibrium without oscillation
- large $b$ means strong damping, so the motion becomes slow and does not oscillate

The critical value is:

$$b_c=2\sqrt{mk}$$

For example, if:

$$m=1$$

and:

$$k=10$$

then:

$$b_c=2\sqrt{10}\approx6.32$$

So:

- if $b<6.32$, the system is underdamped
- if $b=6.32$, the system is critically damped
- if $b>6.32$, the system is overdamped

---

### 5–6. Interactive HTML animation, graph of $x(t)$, and phase portrait

The code below creates an interactive HTML page.  
It uses a slider for the damping coefficient $b$.  
It shows:

- animation of the oscillator
- graph of displacement $x(t)$
- phase portrait $v(x)$
- classification of the current case


---

### Final explanation

This HTML program solves the damped oscillator equation numerically using RK4.  
The slider changes the damping coefficient $b$.

When $b$ is small, the oscillator is underdamped and moves back and forth.  
When $b$ is close to:

$$b_c=2\sqrt{mk}$$

the oscillator becomes critically damped.  
When $b$ is larger than this value, the oscillator is overdamped and returns slowly without oscillation.

The graph $x(t)$ shows how displacement changes over time.  
The phase portrait shows the relation between displacement $x$ and velocity $v$.
