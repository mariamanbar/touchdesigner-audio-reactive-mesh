# Create your first audio-reactive sphere

This tutorial guides you through opening the project file, connecting an audio source, and mapping sound frequencies to geometry displacement.

## Prerequisites

Before starting, verify that you have TouchDesigner 2023 or later installed on your operating system.

## Step 1: Open the network

1. Launch TouchDesigner.
2. Open the `audio_reactive_mesh.toe` project file from your root directory.
3. Press **U** on your keyboard to navigate inside the primary `project1` container.

## Step 2: Connect an audio source

1. Locate the **Audio File In CHOP** on the left side of the network editor.
2. Click the plus icon inside the operator's parameter window to select an audio file from your computer.
3. Toggle the **Play** parameter to start audio playback.

## Step 3: Map frequencies to displacement

1. Connect the output of the **Audio Spectrum CHOP** into the input of the **Math CHOP**.
2. Select the **Math CHOP** and set the **Multiply** parameter to `1.5` to increase the visual gain.
3. Observe the viewport: the 3D sphere now distorts in real time with the audio frequencies.

You now have a functioning audio-reactive mesh. Explore our How-To guides to learn how to route live microphone inputs into this network.