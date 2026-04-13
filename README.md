# EditorialCanvas PRO ✍️⚡

A high-performance JavaScript typography engine that allows text to fluidly wrap around complex geometric shapes, transparent PNGs (Alpha Channel), and hollow figures (SDF) at 60 FPS, with zero DOM Layout Thrashing.

## 🚀 Features

* **Zero Dependencies:** Pure Vanilla JS and HTML5 Canvas API.
* **Alpha Channel Scanning:** Wraps text around transparent PNGs natively.
* **Multi-Segment Support:** Text can flow *through* hollow shapes (like donuts or rings).
* **Memory Cached Typography:** Eliminates `measureText` bottlenecks for extreme performance.
* **Mathematical Justification:** Pixel-perfect text justification without stretching words.

## 🛠️ Quick Start

**1. Add the canvas container to your HTML:**
```html
<div id="magazine-layout" style="width: 100%; height: 600px;">
    <canvas id="my-canvas"></canvas>
</div>

2. Import the script:

HTML
<script src="path/to/EditorialCanvasV3.js"></script>

3. Initialize the engine:

JavaScript
const engine = new EditorialCanvasV3('my-canvas', {
    tipoForma: 'imagen',
    imgSrc: 'assets/my-transparent-logo.png',
    texto: "Your long editorial text goes here...",
    exX: 300, 
    exY: 250,
    exclusionRadio: 150,
    margenExclusion: 20,
    altoLinea: 28,
    justificado: true,
    colorTexto: "#1e293b",
    bgCanvas: "#ffffff"
});

// Optional: Make it responsive
window.addEventListener('resize', () => engine.ajustarResolucion());
