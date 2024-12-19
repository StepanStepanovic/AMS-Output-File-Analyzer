# AMS Output File Analyzer

This Python script simplifies the analysis of AMS (SCM) output files, providing essential insights for geometry optimizations, transition state (TS) searches, and potential energy surface (PES) scans (LT), along with frequency calculations. It is especially useful for students working on cluster environments where the AMS GUI is slow or unavailable.

## Features
- **Geometry Extraction**:
  - Extracts the last geometry, even for non-converged cases, and provides gradients for further analysis.
  - Saves geometry from single-point calculations for consistency checks and follow-up calculations.

- **Optimization Insights**:
  - **Geometry Optimization**:
    - Plots step vs. energy vs. gradient, showing optimization progress.
  - **Transition State Search (TS)**:
    - Plots reaction coordinate vs. gradient vs. step, enabling easy identification of convergence issues in TS searches.
  - **Potential Energy Surface Scans (LT)**:
    - Plots LT steps vs. energy vs. gradient for each step, providing clear insight into PES scans.

- **Frequency Analysis**:
  - Produces a `frq.molden` file for easy visualization in Chemcraft.
  - Resolves compatibility issues with newer AMS versions and semiempirical drivers.

- **Cluster-Friendly**:
  - Designed for command-line usage, bypassing the need for AMS GUI on clusters.
  - Avoids reliance on local AMS licenses for personal laptops.

## Visualization
- Generates clear plots (`opt.png`) showing:
  - **Geometry Optimization**:
    - Energy and gradient per step.
  - **Transition State Search**:
    - Reaction coordinate, gradient, and step.
  - **Potential Energy Surface Scan**:
    - Energy and gradient per LT step.

## Usage
The script works with AMS output files (`test.out`) and creates:
- `last.xyz` and `last.angs`: Final geometries.
- `opt.xyz`: Geometry trajectory for optimization or PES scan.
- `frq.molden`: Frequency data for visualization.

## Example Outputs
- **Geometry Optimization**:
  - Step vs. energy and gradient plot.
- **Transition State Search**:
  - Reaction coordinate vs. gradient vs. step plot.
- **LT Scans**:
  - LT steps vs. energy vs. gradient plot.

## Installation
Clone the repository and run the script with an AMS output file as input.

```bash
git clone https://github.com/<your-repo>/AMS-Output-Analyzer.git
cd AMS-Output-Analyzer
python analyze_ams.py
```

## Requirements
Python 3.x
Libraries: numpy, matplotlib, os, re
Contribution
Feel free to submit issues or contribute improvements via pull requests.

