# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Running the Project

No build process required. Open `src/index.html` directly in a web browser. There are no dependencies, no compilation, and no server needed.

## Architecture

Single-file web application (`src/index.html`, ~3600+ lines) with embedded HTML, CSS, and JavaScript. No external libraries.

### Module Structure

Three self-contained IIFE modules, each implementing one algorithm:

- **`Part1`** — Matrix Chain Multiplication (Dynamic Programming). Core logic in `computeData(p)` which builds cost table `m[i][j]` and split table `s[i][j]`. Visualization via `drawSVG(idx)` and `renderStep(i)`.

- **`Part2`** — Parallel Merge Sort (Fork-Join model). `buildTree(arr)` constructs the recursion tree; `generateSteps()` creates animation frames. Includes a Gantt chart showing processor utilization and live Brent's theorem calculations (Tp ≤ W/p + D).

- **`Part3`** — Extended Euclidean Algorithm & Modular Inverse. `extGCD(a, b)` computes Bézout coefficients recursively; `modInverse(a, n)` derives the modular inverse for RSA/Diffie-Hellman applications.

### Global Controllers

- **`ThemeController`** — Dark/light theme toggle, persisted in `localStorage`.
- **`TabController`** — Navigation between Part 1/2/3 with per-part accent color switching.

### Consistent UI Pattern (all three parts)

Each part follows the same layout and state machine:
- SVG canvas for visualization
- Floating control pill: Build → Step / Play/Pause → Reset
- State object with `{ steps[], currentStep, playTimer, status }`
- Panels below the fold: pseudocode with line highlighting, step explanation, input/presets, statistics table, educational overview

### Visualization

All visualizations are SVG-rendered inline via JavaScript DOM manipulation. No canvas API is used.
