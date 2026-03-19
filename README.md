# Algorithms II — Midterm Project

**BSD 404 Algorithms II**
Canadian University Dubai

---

## Overview

This project is an interactive algorithm visualizer built as a single-page web application. It covers three algorithm topics as required by the midterm specification, each presented with step-by-step animation, pseudocode highlighting, and educational breakdowns.

The interface is designed to be clean and approachable — dark and light themes are supported, and no installation or build process is required to run it.

---

## Algorithms Covered

### Part 1 — Matrix Chain Multiplication
Dynamic programming approach to finding the optimal parenthesization of a matrix chain. The visualization shows the chain diagram alongside the DP cost and split tables, built bottom-up. Supports custom matrix dimension input and includes three presets (3, 4, and 6 matrices).

### Part 2 — Parallel Merge Sort
Fork-join model of merge sort across multiple processors. The visualization includes a recursion tree, a Gantt chart showing processor utilization over time, and a live calculation of Brent's theorem bound (T_p <= W/p + D). Includes an adjustable speed slider and a step history table.

### Part 3 — Extended Euclidean Algorithm
Recursive computation of Bezout coefficients and modular inverse, with applications to RSA and Diffie-Hellman key exchange. The visualization renders a vertical card stack showing each recursive call and the back-substitution phase.

---

## How to Run

No server, build tool, or internet connection is required.

1. Clone or download this repository.
2. Open `index.html` directly in any modern web browser.

That is all. Everything is self-contained in a single file with no external dependencies.

---

## Project Structure

```
Midterm_Project/
├── index.html                        Main application (HTML, CSS, JS — all embedded)
├── Canadian_University_Dubai_Logo.png University logo asset
├── Notes/
│   ├── CLAUDE.md                     Developer notes for AI-assisted workflow
│   └── notes.txt                     UI/UX design notes and feature ideas
└── README.md                         This file
```

---

## Features

- Three tabbed sections, each with its own accent color and independent state
- Step-by-step playback with play, pause, step forward, and reset controls
- Pseudocode panel with live line highlighting synchronized to the animation
- Collapsible panels for input, statistics, and educational overview
- Preset inputs for quick testing on known examples
- Dark and light theme toggle, persisted across sessions via localStorage
- Fully SVG-rendered visualizations — no canvas API, no external charting libraries

---

## Verified Test Cases

| Part | Input | Expected Output |
|------|-------|----------------|
| Matrix Chain | [10, 30, 5, 60] | 4,500 scalar multiplications |
| Matrix Chain | [40, 20, 30, 10, 30] | 26,000 scalar multiplications |
| Matrix Chain | [30, 35, 15, 5, 10, 20, 25] | 15,125 scalar multiplications |
| Extended GCD | Any valid (a, b) | Bezout identity: gcd = a*x + b*y |

---

## Course Information

| Field | Details |
|-------|---------|
| Course | BSD 404 — Algorithms II |
| Institution | Canadian University Dubai |
| Assessment | Midterm Project |

---

## Browser Compatibility

Tested and working in current versions of Chrome, Firefox, Edge, and Safari. JavaScript must be enabled.
