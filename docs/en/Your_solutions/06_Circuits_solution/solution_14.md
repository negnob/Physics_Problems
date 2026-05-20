# 14. RLC Circuit

## Useful definitions and formulas

For a series RLC circuit, Kirchhoff's Voltage Law gives:

$$V_L+V_R+V_C=V(t)$$

where:

$$V_L=L\frac{dI}{dt}$$

$$V_R=RI$$

$$I=C\frac{dV_C}{dt}$$

---

## Step-by-step solution

Using Kirchhoff's Law:

$$L\frac{dI}{dt}+RI+V_C=V(t)$$

Since:

$$I=C\frac{dV_C}{dt}$$

then:

$$\frac{dI}{dt}=C\frac{d^2V_C}{dt^2}$$

Substitute into the equation:

$$LC\frac{d^2V_C}{dt^2}+RC\frac{dV_C}{dt}+V_C=V(t)$$

Divide by $LC$:

$$\frac{d^2V_C}{dt^2}+\frac{R}{L}\frac{dV_C}{dt}+\frac{1}{LC}V_C=\frac{V(t)}{LC}$$

---

## Comparison with damped harmonic oscillator

Equation of damped harmonic oscillator:

$$m\frac{d^2x}{dt^2}+b\frac{dx}{dt}+kx=F(t)$$

Comparison:

$$LC\frac{d^2V_C}{dt^2}+RC\frac{dV_C}{dt}+V_C=V(t)$$

Analogies:

$LC$ acts like mass $m$

$RC$ acts like damping coefficient $b$

$1$ acts like spring constant $k$

$V_C$ acts like displacement $x$

$V(t)$ acts like external force $F(t)$

---

## Final answer

The differential equation is:

$$LC\frac{d^2V_C}{dt^2}+RC\frac{dV_C}{dt}+V_C=V(t)$$

or:

$$\frac{d^2V_C}{dt^2}+\frac{R}{L}\frac{dV_C}{dt}+\frac{1}{LC}V_C=\frac{V(t)}{LC}$$

It has the same form as a damped forced harmonic oscillator.
