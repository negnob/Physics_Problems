# 4. Mixed Circuit

Calculate the equivalent resistance for the circuit shown in the figure. All resistors have a resistance of $10\ \Omega$.
<img width="751" height="350" alt="image" src="https://github.com/user-attachments/assets/2847ce15-9c78-4d38-8080-85833653eca7" />

---

## Useful definitions and formulas

All resistors have:

$$R=10\,\Omega$$

For resistors in series:

$$R_{eq}=R_1+R_2$$

For resistors in parallel:

$$R_{eq}=\frac{R_1R_2}{R_1+R_2}$$

---

## Step-by-step solution

## Top branch

There are two resistors in series:

$$R_{top}=10+10$$

$$R_{top}=20\,\Omega$$

---

## Bottom branch

First, there is one resistor:

$$10\,\Omega$$

Then two resistors are connected in parallel:

$$R_{parallel}=\frac{10\cdot10}{10+10}$$

$$R_{parallel}=5\,\Omega$$

So the bottom branch is:

$$R_{bottom}=10+5$$

$$R_{bottom}=15\,\Omega$$

---

## Combine top and bottom branches

The top and bottom branches are in parallel:

$$R_{main}=\frac{20\cdot15}{20+15}$$

$$R_{main}=\frac{300}{35}$$

$$R_{main}=8.57\,\Omega$$

---

## Add the final resistor on the right

The last resistor is in series with the whole circuit:

$$R_{eq}=8.57+10$$

$$R_{eq}=18.57\,\Omega$$

---

## Final answer

$$R_{eq}=18.57\,\Omega$$
