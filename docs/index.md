# TouchDesigner Audio-Reactive Mesh :sparkles:

[![GitHub repo](https://img.shields.io/badge/GitHub-mariamanbar%2Ftouchdesigner--audio--reactive--mesh-purple.svg)](https://github.com/mariamanbar/touchdesigner-audio-reactive-mesh)
[![TouchDesigner](https://img.shields.io/badge/TouchDesigner-2023%2B-5c5c5c.svg)](https://derivative.ca/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **A real-time, interactive 3D visual installation built in TouchDesigner that transforms audio frequencies into dynamic wireframe meshes and projection mapping environments.**

---

## Quick Start 

Explore the documentation based on what you want to achieve today:

* **[Tutorial: First Reactive Sphere](tutorial.md)** — **I want to learn.** Step-by-step guide to open the `.toe` network and drive geometry displacement from scratch.
* **[How-To: Live Microphone Routing](how-to.md)** — **I want to solve a problem.** Recipes for live mic routing, noise floor limits, and projection optimization.
* **[Reference: Architecture & CHOPs](reference.md)** — **I want technical specs.** Complete breakdown of operators, FFT analysis, and parameter tables.
* **[Source Code & Project Files](https://github.com/mariamanbar/touchdesigner-audio-reactive-mesh)** — **I want the `.toe` files.** Download raw project files directly from GitHub.

---


### Core Visual Capabilities
* **Zero-Latency Frequency Mapping:** Separates low, mid, and high audio frequencies into independent visual displacement drivers using Fast Fourier Transform (FFT) analysis.
* **Fluid Signal Smoothing:** Uses Lag CHOP deceleration algorithms to eliminate visual jitter and smooth out abrupt audio amplitude spikes.
* **Projection Mapping Optimization:** Built specifically for high-framerate live visual rendering and projection mapping installations.