# Contributing to TouchDesigner Audio-Reactive Mesh

Thank you for considering contributing to this project! We welcome contributions, bug reports, visual enhancement proposals, and performance optimizations. 

Please take a moment to review these guidelines before getting started.

---

## 1. Development Setup

To work on this repository locally:

1. **Prerequisites**:
   * **TouchDesigner**: Ensure you have TouchDesigner 2022.20000 or 2023+ installed (Non-Commercial, Educational, or Commercial edition).
   * **Git**: Make sure Git is installed on your local system.
2. **Fork & Clone**:
   ```bash
   git clone [https://github.com/YOUR-USERNAME/touchdesigner-audio-reactive-mesh.git](https://github.com/YOUR-USERNAME/touchdesigner-audio-reactive-mesh.git)
   cd touchdesigner-audio-reactive-mesh
   ```
   3. **Opening the Project**:
   * Open `audioReactive.toe` inside TouchDesigner.
   * If referencing external assets (audio files, textures, custom GLSL scripts), keep all file paths **relative** to the project root directory so the network remains fully portable.

---

## 2. How to Run Tests & Verification

TouchDesigner projects rely on real-time execution stability rather than standard unit tests. Before submitting a contribution, run through the following performance and network verification checks:

* **FPS & Cooking Performance**: Press **`Alt + f`** (or check the main header bar) to display the frame rate. Verify that the network maintains a stable **60 FPS** without major dropouts during audio playback.
* **Operator Error Check**: Inspect the network node hierarchy to ensure no operators display red error flags or missing asset path warnings.
* **Audio Pipeline Verification**: Verify that audio input switches cleanly between live input (`audioIn`) and local files (`audiofilein1`), and that CHOP signal mapping responds across low, mid, and high frequency bands.
* **Playback Mode**: Ensure the timeline play mode at the bottom bar is set to **Sequential** before saving your `.toe` file.

---

## 3. How to File a Bug

Before opening a bug report, please check existing GitHub Issues to avoid duplicate submissions.

When reporting a bug, use the **Bug Report** issue template and include:
* **System Specifications**: OS (macOS/Windows), GPU model, and exact TouchDesigner build version.
* **Steps to Reproduce**: Detailed sequence of actions leading to the crash, broken CHOP parameter, or visual defect.
* **Expected vs. Actual Behavior**: Describe what should happen versus what actually occurred.
* **Visual Evidence**: Screenshots or short video screen-captures showing node networks or error dialogs.

---

## 4. Pull Request Conventions

We follow **Conventional Commits** to keep commit history clean and facilitate automated semantic versioning.

### Branch Naming Strategy
Name your working branch according to the type of change:
* `feat/short-description` (e.g., `feat/add-highpass-filter`)
* `fix/short-description` (e.g., `fix/broken-feedback-top`)
* `docs/short-description` (e.g., `docs/update-setup-instructions`)

### Commit Message Format
Structure your commit messages using the standard prefix format:
* `feat: add dynamic bloom pass to visual output`
* `fix: correct CHOP scaling parameter on bass transient`
* `docs: fix typo in CONTRIBUTING guidelines`
* `refactor: clean up SOP network layout`

### PR Submission Requirements
* Make sure your PR targets the `main` branch.
* Use the provided PR Template.
* Attach a screenshot, GIF, or brief screen recording showcasing any visual changes or network UI additions.

---

## 5. Review Expectations

All incoming Pull Requests undergo review before being merged into `main`.

* **Review Scope**: PRs will be evaluated for node cleanliness, relative file path usage, clear commit messages, and frame-rate stability (maintaining 60 FPS).
* **Feedback Process**: If changes or optimizations are needed, constructive feedback will be left directly on the PR conversation thread.
* **Response Timeline**: Expect an initial review or feedback within 48–72 hours.

---

*Thank you for helping improve the TouchDesigner Audio-Reactive Mesh!*
