# 3. Mixed Circuit
Calculate the equivalent resistance for the circuit shown in the figure. All resistors have a resistance of $5\ \Omega$.

<img width="431" height="350" alt="image" src="https://github.com/user-attachments/assets/741d2165-d77c-4a91-8758-f951b6af4376" />


---
## Useful definitions and formulas

All resistors have:

$$R=5\,\Omega$$

For resistors in series:

$$R_{eq}=R_1+R_2+...$$

For resistors in parallel:

$$\frac{1}{R_{eq}}=\frac{1}{R_1}+\frac{1}{R_2}+...$$

or for two resistors:

$$R_{eq}=\frac{R_1R_2}{R_1+R_2}$$

---

## Step-by-step solution

There is one resistor directly at the bottom between the two terminals:

$$R_{bottom}=5\,\Omega$$

Now calculate the upper part of the circuit.

### Left path to the top node

Two resistors are in series:

$$R_{left}=5+5=10\,\Omega$$

### Middle path to the top node

There is one horizontal resistor and two vertical resistors in series:

$$R_{middle}=5+5+5=15\,\Omega$$

These two paths are in parallel:

$$R_{A\to top}=\frac{10\cdot15}{10+15}$$

$$R_{A\to top}=\frac{150}{25}=6\,\Omega$$

### Right side path

Two resistors are in series:

$$R_{right}=5+5=10\,\Omega$$

So the whole upper branch is:

$$R_{upper}=6+10=16\,\Omega$$

Now the upper branch is in parallel with the bottom resistor:

$$R_{eq}=\frac{5\cdot16}{5+16}$$

$$R_{eq}=\frac{80}{21}$$

$$R_{eq}=3.81\,\Omega$$

---

## Final answer

$$R_{eq}=3.81\,\Omega$$
