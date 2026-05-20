# 5. Kirchhoff's Laws

Using Kirchhoff’s laws, find the currents $I_1$, $I_2$, $I_3$ (going through the resistors $R_1$, $R_2$, $R_3$ respectively) in the following two-loop circuit:

- Left loop: ammeter $A$, top resistor $R_1 = 20\,\Omega$, and bottom source $\mathcal{E}_1 = 4.5\,\text{V}$ in series with internal resistance $r_w = 1\,\Omega$.
- Right loop: source $\mathcal{E}_2 = 9\,\text{V}$ in series with internal resistance $r_w = 1\,\Omega$.
- Shared branch: resistor $R_2 = 10\,\Omega$ connecting the top-right node to the bottom node.
<img width="554" height="400" alt="image" src="https://github.com/user-attachments/assets/43477c66-ec57-4aec-a67d-1c9463cdc259" />

---

## Useful definitions and formulas

Kirchhoff's Current Law:

$$I_1+I_2+I_3=0$$

Kirchhoff's Voltage Law:

$$\sum V=0$$

Ohm's Law:

$$V=IR$$

We take currents from the top node to the bottom node as positive.

---

## Step-by-step solution

Given:

$$R_1=20\,\Omega$$

$$R_2=10\,\Omega$$

$$r_w=1\,\Omega$$

$$\mathcal{E}_1=4.5\,V$$

$$\mathcal{E}_2=9\,V$$

Let the voltage between the top and bottom nodes be:

$$V$$

---

## Current through left branch

The left branch has $R_1$ and internal resistance $r_w$ in series:

$$R_{left}=20+1=21\,\Omega$$

So:

$$I_1=\frac{V-\mathcal{E}_1}{21}$$

$$I_1=\frac{V-4.5}{21}$$

---

## Current through middle branch

$$I_2=\frac{V}{R_2}$$

$$I_2=\frac{V}{10}$$

---

## Current through right branch

The right branch has internal resistance $r_w=1\,\Omega$ and source $\mathcal{E}_2=9\,V$:

$$I_3=\frac{V-\mathcal{E}_2}{1}$$

$$I_3=V-9$$

---

## Apply Kirchhoff's Current Law

$$I_1+I_2+I_3=0$$

$$\frac{V-4.5}{21}+\frac{V}{10}+V-9=0$$

Solving:

$$V=8.03\,V$$

---

## Calculate currents

### Current through $R_1$

$$I_1=\frac{8.03-4.5}{21}$$

$$I_1=0.168\,A$$

### Current through $R_2$

$$I_2=\frac{8.03}{10}$$

$$I_2=0.803\,A$$

### Current through right branch

$$I_3=8.03-9$$

$$I_3=-0.971\,A$$

The negative sign means the real direction of $I_3$ is opposite to our chosen direction.

---

## Final answer

$$I_1=0.168\,A$$

$$I_2=0.803\,A$$

$$I_3=-0.971\,A$$

So, $I_1$ and $I_2$ flow from the top node to the bottom node, but $I_3$ actually flows from the bottom node to the top node.

Magnitude of the third current:

$$|I_3|=0.971\,A$$
