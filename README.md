# Audio Reactive Mesh

A real-time, audio-reactive geometric visualizer built in TouchDesigner.  
The network processes live audio data to drive the scale and motion of a wireframe mandala, creating an immersive, fluid tunnel effect.

Developed as an exploration of procedural geometry and real-time data integration.

## ★ Features
* **Frequency Isolation:** Separates low-end bass transients and high frequencies to dynamically control independent geometric layers.
* **Fluid Dynamics:** Avoids geometry rebuild bottlenecks by mapping processed CHOP signals directly to floating-point scaling parameters for smooth, high-FPS rendering.
* **Feedback Stacks:** Uses TOP-layer post-processing feedback loops to create soft, evolving motion trails.

## ★ How to Run

1. Clone or download this repository to your local machine.
2. Open `audioReactive.toe` inside TouchDesigner.
3. Import your audio:
   * Select the **`audiofilein1`** node on the far left.
   * In the top-right parameter window, click the **`+`** icon next to the **File** field.
   * Select the included `Consciousness - Anyma .mp3` track (or drop in your own audio file).
4. Ensure the TouchDesigner timeline play mode at the bottom is set to **Sequential** and press the **Spacebar** to play.
