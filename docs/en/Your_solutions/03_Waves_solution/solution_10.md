## 10. Animation: Wave Sources

### Useful definitions and formulas

Each point source produces a wave:

$$u(\vec{r},t)=\frac{A}{|\vec{r}-\vec{r_0}|^\alpha}\sin(k|\vec{r}-\vec{r_0}|-\omega t)$$

where:

- $\vec{r}$ is the observation point
- $\vec{r_0}$ is the source position
- $A$ is amplitude
- $\alpha$ controls how strongly the amplitude decreases with distance
- $k=\frac{2\pi}{\lambda}$ is wave number
- $\omega=2\pi f$ is angular frequency

Important meaning of $\alpha$:

- if $\alpha=0$, there is no decay with distance
- if $\alpha=1$, amplitude decreases like $\frac{1}{r}$
- if $\alpha=2$, amplitude decreases faster

If there are many sources, we use superposition:

$$u_{\text{total}}(\vec{r},t)=\sum_i \frac{A}{|\vec{r}-\vec{r_i}|^\alpha}\sin(k|\vec{r}-\vec{r_i}|-\omega t)$$

That means:
- calculate the wave from each source
- add all contributions together
- the result is the total displacement

---

### What the animation should do

The animation should allow the user to:
- click and place dots on the screen
- treat each dot as a wave source
- choose the value of $\alpha$ from $0$ to $2$
- see the superposition pattern update in real time
