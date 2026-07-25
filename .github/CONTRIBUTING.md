# Contributing to TouchDesigner Audio-Reactive Mesh

Thank you for considering contributing! Here are guidelines to help you get started.

## How to Contribute

1. **Report Bugs**: Open an issue detailing your TouchDesigner build version, OS, GPU, and steps to reproduce.
2. **Suggest Features**: Submit an issue describing the visual effect, pipeline, or performance improvement you'd like to see.
3. **Submit Code / Assets**:
   * Fork the repository.
   * Create a feature branch (`git checkout -b feature/feature-name`).
   * Keep external assets (audio files, textures) light or host them externally when possible.
   * Format any custom Python scripts cleanly.
   * Open a Pull Request referencing your issue.

## Pull Request Guidelines

* Ensure your `.toe` file opens cleanly without missing file paths (use relative paths for assets).
* Keep custom Python scripts or GLSL shaders in external files (`/scripts`, `/shaders`) if they are referenced by external operators.
* Summarize network structure changes in your PR description.
