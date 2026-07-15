# 0001. Build custom lightweight audio analysis network instead of using the audioAnalysis palette tool

## Status
Accepted, 2026-07-15.

## Context
The interactive visual mesh must maintain a stable framerate during live rendering without crashing or dropping frames. TouchDesigner's pre-built `audioAnalysis` palette component relies on heavy processing and specific GPU hardware acceleration, which throws errors and fails to execute reliably on systems with integrated graphics or limited hardware capabilities. We need a signal processing architecture that runs seamlessly across lower-end hardware without sacrificing real-time reactivity.

## Decision
We will build a custom, lightweight audio analysis network using core native operators (`Audio Spectrum CHOP`, `Math CHOP`, `Lag CHOP`, and `Limit CHOP`) rather than importing the pre-built `audioAnalysis` component from the TouchDesigner palette.

## Consequences
+ Eliminates GPU dependency errors, ensuring the project opens and runs reliably on integrated graphics and limited hardware.
+ Reduces CPU and GPU overhead, reserving system resources for 3D geometry deformation and rendering.
+ Provides full transparency and modular control over frequency math, signal damping, and noise thresholds.
- Sacrifices out-of-the-box advanced acoustic feature extraction (such as automated tempo tracking and beat detection).
- Requires manual math and lag calibration to achieve clean visual separation for low, mid, and high frequency bands.
