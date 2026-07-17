<h1 align="center">⭓ Audio Reactive Mesh ⯂</h1>

https://github.com/user-attachments/assets/3e0f9c2f-3adc-4a22-b9db-dabe966e395b

[![Documentation](https://img.shields.io/badge/docs-MkDocs_Material-indigo.svg)](https://mariamanbar.github.io/touchdesigner-audio-reactive-mesh/)  
A real-time, audio-reactive geometric visualizer built in TouchDesigner.  
The network processes live audio data to drive the scale and motion of a wireframe mandala, creating an immersive, fluid tunnel effect.

Developed as an exploration of procedural geometry and real-time data integration.

## ★ Features
* **Frequency Isolation:** Separates low-end bass transients and high frequencies to dynamically control independent geometric layers.
* **Fluid Dynamics:** Avoids geometry rebuild bottlenecks by mapping processed CHOP signals directly to floating-point scaling parameters for smooth, high-FPS rendering.
* **Feedback Stacks:** Uses TOP-layer post-processing feedback loops to create soft, evolving motion trails.

## ★ How to Run
### Option 1: Download the Stable Release (Recommended)
1. Go to the **Releases** section on the right side of this repository page and download the latest `release.tar.gz`.
2. Extract the archive on your local machine.

### Option 2:
Alternatively,
1. Clone or download this repository to your local machine.
2. Open `audioReactive.toe` inside TouchDesigner.
3. Import your audio:
   * Select the **`audiofilein1`** node on the far left.
   * In the top-right parameter window, click the **`+`** icon next to the **File** field.
   * Select the included `Consciousness - Anyma .mp3` track (or drop in your own audio file).
4. Ensure the TouchDesigner timeline play mode at the bottom is set to **Sequential** and press the **Spacebar** to play.  

## ★ Security & Software Supply Chain Verification

This repository follows secure distribution practices. The release artifacts are cryptographically signed using **Sigstore (cosign)** via keyless authentication linked to GitHub OIDC[cite: 1].

To verify the integrity and authenticity of the downloaded release artifact, make sure you have `cosign` installed and run the following command:

```bash
cosign verify-blob \
  --certificate release.tar.gz.pem \
  --signature release.tar.gz.sig \
  --certificate-identity '[https://github.com/mariamanbar](https://github.com/mariamanbar)' \
  --certificate-oidc-issuer '[https://github.com/login/oauth](https://github.com/login/oauth)' \
  ./release.tar.gz
