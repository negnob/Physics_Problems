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

---

### HTML animation

Save this as `wave_sources.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Wave Sources</title>
  <style>
    body {
      background: #111;
      color: #eee;
      font-family: Arial, sans-serif;
      margin: 20px;
    }
    canvas {
      border: 1px solid #555;
      background: black;
      display: block;
    }
    .panel {
      margin-bottom: 15px;
      background: #1b1b1b;
      padding: 12px;
      border-radius: 10px;
      max-width: 750px;
    }
  </style>
</head>
<body>
  <h2>Wave Source Superposition</h2>

  <div class="panel">
    <label>Alpha: <span id="alphaValue">1.0</span></label>
    <input type="range" id="alphaSlider" min="0" max="2" step="0.1" value="1.0" style="width:250px;">
    <button id="clearBtn">Clear Sources</button>
    <p>Click on the canvas to place wave sources.</p>
  </div>

  <canvas id="canvas" width="700" height="500"></canvas>

<script>
const canvas = document.getElementById("canvas");
const ctx = canvas.getContext("2d");
const alphaSlider = document.getElementById("alphaSlider");
const alphaValue = document.getElementById("alphaValue");
const clearBtn = document.getElementById("clearBtn");

let sources = [];
let t = 0;

const A = 1;
const lambda = 40;
const f = 0.08;
const k = 2 * Math.PI / lambda;
const omega = 2 * Math.PI * f;

canvas.addEventListener("click", function(e) {
  const rect = canvas.getBoundingClientRect();
  const x = e.clientX - rect.left;
  const y = e.clientY - rect.top;
  sources.push({x, y});
});

clearBtn.addEventListener("click", function() {
  sources = [];
});

function draw() {
  const alpha = parseFloat(alphaSlider.value);
  alphaValue.textContent = alpha.toFixed(1);

  const image = ctx.createImageData(canvas.width, canvas.height);
  const data = image.data;

  for (let y = 0; y < canvas.height; y += 2) {
    for (let x = 0; x < canvas.width; x += 2) {
      let u = 0;

      for (const s of sources) {
        const dx = x - s.x;
        const dy = y - s.y;
        let r = Math.sqrt(dx*dx + dy*dy);
        if (r < 1) r = 1;

        u += (A / Math.pow(r, alpha)) * Math.sin(k * r - omega * t);
      }

      const color = Math.max(0, Math.min(255, 128 + u * 2000));

      for (let yy = 0; yy < 2; yy++) {
        for (let xx = 0; xx < 2; xx++) {
          const px = x + xx;
          const py = y + yy;

          if (px < canvas.width && py < canvas.height) {
            const index = (py * canvas.width + px) * 4;
            data[index] = color;
            data[index + 1] = color;
            data[index + 2] = 255 - color;
            data[index + 3] = 255;
          }
        }
      }
    }
  }

  ctx.putImageData(image, 0, 0);

  ctx.fillStyle = "yellow";
  for (const s of sources) {
    ctx.beginPath();
    ctx.arc(s.x, s.y, 4, 0, 2 * Math.PI);
    ctx.fill();
  }

  t += 1;
  requestAnimationFrame(draw);
}

draw();
</script>
</body>
</html>
