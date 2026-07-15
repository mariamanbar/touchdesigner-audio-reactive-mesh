# Route live microphone audio into the mesh

This guide shows you how to replace static audio playback with a live microphone feed or system audio input.

## Configure system audio device

1. Delete or disconnect the existing **Audio File In CHOP** from the network.
2. Press **Tab** to open the operator creation menu, select **CHOP**, and create an **Audio Device In CHOP**.
3. In the operator parameters, click the **Device** dropdown and select your target microphone or virtual audio routing driver.

## Calibrate the noise floor

Live audio inputs contain background noise that causes unwanted mesh displacement during silent periods.

1. Create a **Limit CHOP** and place it immediately after your **Audio Device In CHOP**.
2. Set the **Minimum** parameter to `0.05` to clamp low-level background noise to zero or chsnge it as desired.
3. Connect the output of the **Limit CHOP** directly into your **Audio Spectrum CHOP**.

The mesh now responds exclusively to active vocal or instrumental inputs exceeding your threshold. 