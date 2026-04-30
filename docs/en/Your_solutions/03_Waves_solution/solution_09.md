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

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Damped Oscillator</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      color: #111;
      padding: 20px;
    }

    h1, h2 {
      text-align: center;
    }

    .container {
      max-width: 1100px;
      margin: auto;
      background: white;
      padding: 20px;
      border-radius: 12px;
      box-shadow: 0 0 15px rgba(0,0,0,0.15);
    }

    .controls {
      text-align: center;
      margin-bottom: 20px;
    }

    input[type="range"] {
      width: 400px;
    }

    canvas {
      display: block;
      margin: 20px auto;
      background: #ffffff;
      border: 2px solid #111;
    }

    .info {
      text-align: center;
      font-size: 18px;
      margin: 10px;
    }
  </style>
</head>
<body>

<div class="container">
  <h1>Damped Harmonic Oscillator</h1>

  <div class="controls">
    <label for="bSlider">Damping coefficient b:</label>
    <input type="range" id="bSlider" min="0" max="15" step="0.1" value="1">
    <span id="bValue">1.0</span>
  </div>

  <div class="info">
    <p id="caseText"></p>
    <p>Equation: m x'' + b x' + k x = 0</p>
  </div>

  <h2>Oscillator Animation</h2>
  <canvas id="animationCanvas" width="900" height="180"></canvas>

  <h2>Graph of x(t)</h2>
  <canvas id="graphCanvas" width="900" height="300"></canvas>

  <h2>Phase Portrait v(x)</h2>
  <canvas id="phaseCanvas" width="900" height="300"></canvas>
</div>

<script>
  const m = 1;
  const k = 10;

  let b = 1;
  let x0 = 1;
  let v0 = 0;

  const dt = 0.02;
  const totalTime = 20;

  const bSlider = document.getElementById("bSlider");
  const bValue = document.getElementById("bValue");
  const caseText = document.getElementById("caseText");

  const animationCanvas = document.getElementById("animationCanvas");
  const graphCanvas = document.getElementById("graphCanvas");
  const phaseCanvas = document.getElementById("phaseCanvas");

  const animCtx = animationCanvas.getContext("2d");
  const graphCtx = graphCanvas.getContext("2d");
  const phaseCtx = phaseCanvas.getContext("2d");

  let solution = [];
  let animationIndex = 0;

  function acceleration(x, v, b) {
    return -(b / m) * v - (k / m) * x;
  }

  function rk4Step(x, v, t, dt, b) {
    let k1x = v;
    let k1v = acceleration(x, v, b);

    let k2x = v + 0.5 * dt * k1v;
    let k2v = acceleration(x + 0.5 * dt * k1x, v + 0.5 * dt * k1v, b);

    let k3x = v + 0.5 * dt * k2v;
    let k3v = acceleration(x + 0.5 * dt * k2x, v + 0.5 * dt * k2v, b);

    let k4x = v + dt * k3v;
    let k4v = acceleration(x + dt * k3x, v + dt * k3v, b);

    let newX = x + (dt / 6) * (k1x + 2 * k2x + 2 * k3x + k4x);
    let newV = v + (dt / 6) * (k1v + 2 * k2v + 2 * k3v + k4v);

    return {x: newX, v: newV};
  }

  function solveSystem() {
    solution = [];

    let x = x0;
    let v = v0;
    let t = 0;

    while (t <= totalTime) {
      solution.push({t: t, x: x, v: v});

      let next = rk4Step(x, v, t, dt, b);
      x = next.x;
      v = next.v;
      t += dt;
    }
  }

  function classifyCase() {
    const criticalB = 2 * Math.sqrt(m * k);
    const eps = 0.05;

    if (Math.abs(b - criticalB) < eps) {
      return "Critically damped: fastest return without oscillation";
    } else if (b < criticalB) {
      return "Underdamped: oscillation with decreasing amplitude";
    } else {
      return "Overdamped: no oscillation, slow return to equilibrium";
    }
  }

  function drawAnimation() {
    animCtx.clearRect(0, 0, animationCanvas.width, animationCanvas.height);

    const centerY = animationCanvas.height / 2;
    const wallX = 80;
    const scale = 180;

    const point = solution[animationIndex % solution.length];
    const massX = 450 + point.x * scale;

    animCtx.lineWidth = 3;

    animCtx.beginPath();
    animCtx.moveTo(wallX, centerY);
    animCtx.lineTo(massX - 40, centerY);
    animCtx.stroke();

    animCtx.fillStyle = "#222";
    animCtx.fillRect(wallX - 20, centerY - 60, 20, 120);

    animCtx.fillStyle = "#2563eb";
    animCtx.fillRect(massX - 40, centerY - 30, 80, 60);

    animCtx.fillStyle = "#111";
    animCtx.font = "16px Arial";
    animCtx.fillText("x = " + point.x.toFixed(3), massX - 35, centerY + 55);

    animationIndex++;
  }

  function drawGraph() {
    graphCtx.clearRect(0, 0, graphCanvas.width, graphCanvas.height);

    const width = graphCanvas.width;
    const height = graphCanvas.height;
    const margin = 40;

    graphCtx.strokeStyle = "#aaa";
    graphCtx.lineWidth = 1;

    graphCtx.beginPath();
    graphCtx.moveTo(margin, height / 2);
    graphCtx.lineTo(width - margin, height / 2);
    graphCtx.stroke();

    graphCtx.beginPath();
    graphCtx.moveTo(margin, margin);
    graphCtx.lineTo(margin, height - margin);
    graphCtx.stroke();

    graphCtx.strokeStyle = "#2563eb";
    graphCtx.lineWidth = 2;
    graphCtx.beginPath();

    for (let i = 0; i < solution.length; i++) {
      const px = margin + (solution[i].t / totalTime) * (width - 2 * margin);
      const py = height / 2 - solution[i].x * 100;

      if (i === 0) {
        graphCtx.moveTo(px, py);
      } else {
        graphCtx.lineTo(px, py);
      }
    }

    graphCtx.stroke();

    graphCtx.fillStyle = "#111";
    graphCtx.font = "16px Arial";
    graphCtx.fillText("t", width - 30, height / 2 - 10);
    graphCtx.fillText("x(t)", margin + 10, 25);
  }

  function drawPhasePortrait() {
    phaseCtx.clearRect(0, 0, phaseCanvas.width, phaseCanvas.height);

    const width = phaseCanvas.width;
    const height = phaseCanvas.height;
    const centerX = width / 2;
    const centerY = height / 2;

    phaseCtx.strokeStyle = "#aaa";
    phaseCtx.lineWidth = 1;

    phaseCtx.beginPath();
    phaseCtx.moveTo(40, centerY);
    phaseCtx.lineTo(width - 40, centerY);
    phaseCtx.stroke();

    phaseCtx.beginPath();
    phaseCtx.moveTo(centerX, 30);
    phaseCtx.lineTo(centerX, height - 30);
    phaseCtx.stroke();

    phaseCtx.strokeStyle = "#dc2626";
    phaseCtx.lineWidth = 2;
    phaseCtx.beginPath();

    for (let i = 0; i < solution.length; i++) {
      const px = centerX + solution[i].x * 200;
      const py = centerY - solution[i].v * 60;

      if (i === 0) {
        phaseCtx.moveTo(px, py);
      } else {
        phaseCtx.lineTo(px, py);
      }
    }

    phaseCtx.stroke();

    phaseCtx.fillStyle = "#111";
    phaseCtx.font = "16px Arial";
    phaseCtx.fillText("x", width - 30, centerY - 10);
    phaseCtx.fillText("v", centerX + 10, 25);
  }

  function update() {
    b = parseFloat(bSlider.value);
    bValue.textContent = b.toFixed(1);

    solveSystem();
    animationIndex = 0;

    caseText.textContent = classifyCase();

    drawGraph();
    drawPhasePortrait();
  }

  bSlider.addEventListener("input", update);

  function animate() {
    drawAnimation();
    requestAnimationFrame(animate);
  }

  update();
  animate();
</script>

</body>
</html>
```

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
