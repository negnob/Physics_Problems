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

---

### HTML animation

Save this as `damped_oscillator.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Damped Oscillator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #111;
      color: #eee;
      margin: 20px;
    }
    h2, h3 {
      margin-bottom: 10px;
    }
    .controls {
      background: #1c1c1c;
      padding: 15px;
      border-radius: 10px;
      margin-bottom: 20px;
      max-width: 700px;
    }
    canvas {
      background: white;
      border: 1px solid #666;
      display: block;
      margin-bottom: 20px;
    }
    .row {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }
  </style>
</head>
<body>
  <h2>Damped Harmonic Oscillator</h2>

  <div class="controls">
    <label for="bSlider">Damping coefficient b:</label>
    <input type="range" id="bSlider" min="0" max="20" step="0.1" value="1.0" style="width:300px;">
    <span id="bValue">1.0</span>
    <p id="caseText"></p>
  </div>

  <div class="row">
    <div>
      <h3>x(t)</h3>
      <canvas id="xtCanvas" width="600" height="300"></canvas>
    </div>
    <div>
      <h3>Phase Portrait</h3>
      <canvas id="phaseCanvas" width="600" height="300"></canvas>
    </div>
  </div>

<script>
const m = 1;
const k = 9;
const x0 = 1;
const v0 = 0;
const dt = 0.02;
const T = 20;

const bSlider = document.getElementById("bSlider");
const bValue = document.getElementById("bValue");
const caseText = document.getElementById("caseText");

const xtCanvas = document.getElementById("xtCanvas");
const xtCtx = xtCanvas.getContext("2d");

const phaseCanvas = document.getElementById("phaseCanvas");
const phaseCtx = phaseCanvas.getContext("2d");

function derivatives(state, b) {
  const x = state[0];
  const v = state[1];
  const dxdt = v;
  const dvdt = -(b/m) * v - (k/m) * x;
  return [dxdt, dvdt];
}

function rk4Step(state, b, h) {
  const k1 = derivatives(state, b);

  const s2 = [
    state[0] + 0.5 * h * k1[0],
    state[1] + 0.5 * h * k1[1]
  ];
  const k2 = derivatives(s2, b);

  const s3 = [
    state[0] + 0.5 * h * k2[0],
    state[1] + 0.5 * h * k2[1]
  ];
  const k3 = derivatives(s3, b);

  const s4 = [
    state[0] + h * k3[0],
    state[1] + h * k3[1]
  ];
  const k4 = derivatives(s4, b);

  return [
    state[0] + (h/6) * (k1[0] + 2*k2[0] + 2*k3[0] + k4[0]),
    state[1] + (h/6) * (k1[1] + 2*k2[1] + 2*k3[1] + k4[1])
  ];
}

function simulate(b) {
  let state = [x0, v0];
  const data = [];

  for (let t = 0; t <= T; t += dt) {
    data.push({ t: t, x: state[0], v: state[1] });
    state = rk4Step(state, b, dt);
  }

  return data;
}

function classify(b) {
  const bCritical = 2 * Math.sqrt(m * k);

  if (Math.abs(b - bCritical) < 0.05) {
    return "Critically damped";
  } else if (b < bCritical) {
    return "Underdamped";
  } else {
    return "Overdamped";
  }
}

function drawXT(data) {
  const w = xtCanvas.width;
  const h = xtCanvas.height;

  xtCtx.clearRect(0, 0, w, h);

  xtCtx.strokeStyle = "#aaa";
  xtCtx.beginPath();
  xtCtx.moveTo(40, h/2);
  xtCtx.lineTo(w - 10, h/2);
  xtCtx.moveTo(40, 10);
  xtCtx.lineTo(40, h - 10);
  xtCtx.stroke();

  xtCtx.strokeStyle = "blue";
  xtCtx.beginPath();

  for (let i = 0; i < data.length; i++) {
    const px = 40 + (data[i].t / T) * (w - 50);
    const py = h/2 - data[i].x * 100;

    if (i === 0) xtCtx.moveTo(px, py);
    else xtCtx.lineTo(px, py);
  }

  xtCtx.stroke();
}

function drawPhase(data) {
  const w = phaseCanvas.width;
  const h = phaseCanvas.height;

  phaseCtx.clearRect(0, 0, w, h);

  phaseCtx.strokeStyle = "#aaa";
  phaseCtx.beginPath();
  phaseCtx.moveTo(40, h/2);
  phaseCtx.lineTo(w - 10, h/2);
  phaseCtx.moveTo(w/2, 10);
  phaseCtx.lineTo(w/2, h - 10);
  phaseCtx.stroke();

  phaseCtx.strokeStyle = "red";
  phaseCtx.beginPath();

  for (let i = 0; i < data.length; i++) {
    const px = w/2 + data[i].x * 120;
    const py = h/2 - data[i].v * 40;

    if (i === 0) phaseCtx.moveTo(px, py);
    else phaseCtx.lineTo(px, py);
  }

  phaseCtx.stroke();
}

function update() {
  const b = parseFloat(bSlider.value);
  bValue.textContent = b.toFixed(1);
  caseText.textContent = "Case: " + classify(b);

  const data = simulate(b);
  drawXT(data);
  drawPhase(data);
}

bSlider.addEventListener("input", update);
update();
</script>
</body>
</html>
