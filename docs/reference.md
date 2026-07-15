# Network architecture & operator reference

This document details the primary operators and critical parameter adjustments used to build the audio-reactive mesh.

## Key operator configurations

Instead of default settings, the following parameters were modified to achieve clean audio-to-geometry routing:

| Operator | Parameter | Value | Why it was changed |
| :--- | :--- | :--- | :--- |
| `Math CHOP` | **Multiply** | `2.0` | Boosts the incoming audio spectrum amplitude so the mesh displaces visibly. |
| `Lag CHOP` | **Lag 1 / Lag 2** | `0.15 / 0.15` | Adds deceleration to smooth out jittery audio spikes and create fluid motion. |
| `Noise SOP` | **Amplitude** | `1.5` | Sets the maximum distance vertices can be displaced by the audio feed. |
| `Noise SOP` | **Period** | `0.5` | Adjusts the frequency of the 3D noise waves across the geometry surface. |

## Core operator

### Audio Analysis
* **Audio Spectrum CHOP:** Converts time-domain audio signals into frequency-domain amplitude buckets using Fast Fourier Transform (FFT).
* **Lag CHOP:** Applies logarithmic deceleration to the frequency channels to prevent jitter in the visual rendering.

### Geometry Rendering
* **Sphere SOP:** Generates the base 3D polygon mesh with a frequency resolution of 100 rows and 100 columns.
* **Noise SOP:** Deforms the sphere's vertex normals based on the incoming CHOP amplitude data.