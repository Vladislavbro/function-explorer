# Function Explorer

An interactive single-page tool for exploring common mathematical functions and how the parameters `a`, `b`, `c`, `d` in `a · f(b·x + c) + d` reshape their graphs.

## Features

- **Function catalog** grouped by category: polynomials, exponential & logarithm, trigonometry, hyperbolic, piecewise/special, and ML activations (sigmoid, ReLU, Leaky ReLU, softplus, Swish, GELU, ELU).
- **Live transformations** — drag sliders for `a` (y-scale), `b` (x-scale), `c` (x-shift), `d` (y-shift) and see the curve update in real time.
- **Multi-overlay** — `Shift+click` a function in the sidebar to overlay it on top of the current selection. Each curve gets its own tab and color.
- **Formula readout** — shows both the base formula and the current transformed expression, simplified (e.g. `2·sin(x − 1) + 0.5`).
- **Properties card** — domain, range, parity, asymptotes, derivative, and short notes for each function.
- **Pan / zoom / autoscale** via the Plotly modebar (appears in the top-right corner on hover).

## Usage

Open `function_explorer.html` in any modern browser. No build step, no dependencies to install — Plotly and Tailwind are loaded from CDN.

```
open function_explorer.html
```

### Controls

- **Click** a function in the left sidebar to select it.
- **Shift+click** to add it as an overlay.
- **Click the × on a tab** to remove that overlay.
- **Drag the plot** to pan, scroll to zoom, or use the Plotly buttons in the top-right (autoscale, reset, etc.).
- **Reset** button restores `a=1, b=1, c=0, d=0` for the active function.

## Tech

- [Plotly.js](https://plotly.com/javascript/) for the chart.
- [Tailwind CSS](https://tailwindcss.com/) (via CDN Play script) for layout.
- Vanilla JS, no build pipeline.
