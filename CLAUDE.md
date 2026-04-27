# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains a single French-language high-school mathematics assignment (`fonctions_reference.html`) on the four reference functions studied in *Seconde* (Year 10):

- **Fonction carrée** – f(x) = x² (blue, parabola)
- **Fonction cube** – g(x) = x³ (orange, S-curve)
- **Fonction racine carrée** – h(x) = √x (green, half-parabola)
- **Fonction inverse** – k(x) = 1/x (purple, hyperbola)

There is no build system, package manager, or test suite. The document is a self-contained HTML5 file with all CSS and SVG inline.

## File Structure

`fonctions_reference.html` is organized into three parts:

| Section | Content |
|---|---|
| **Partie I** | Observation table — one row per function with algebraic expression, domain (𝔻), and an inline SVG graph |
| **Partie II** | Note about XMind download/installation |
| **Partie III** | SVG mind map (820×560 px) with four color-coded branches and a closing remarks paragraph |

## Conventions

### Language
All content is written in French. Mathematical notation uses standard French conventions:
- Domains written as `𝔻_f = ℝ` or interval notation `[0 ; +∞[` (French uses `;` inside intervals, not `,`)
- Unicode symbols: `ℝ`, `ℝ*`, `ℝ⁺`, `∞`, `√`, `𝔻`

### SVG Graphs (Partie I)
Each graph is a 160×140 SVG (`viewBox="-80 -70 160 140"`) with the origin at centre. Coordinate mapping:
- **x_px** = x_val × scale_x
- **y_px** = −f(x_val) × scale_y  (SVG y-axis is inverted)

Per-function colors and approximate scales:

| Function | Stroke | x scale | y scale |
|---|---|---|---|
| f(x) = x² | `#1a7fd4` | ×20 | ×1 (y_px = −x²×1) |
| g(x) = x³ | `#e05c00` | ×10 | ×6 |
| h(x) = √x | `#2aaa44` | ×10 | ×20 |
| k(x) = 1/x | `#9b27af` | ×15 | ×15 |

CSS classes used: `.axis`, `.curve`, `.grid`, `.tick`, `.arrowhead`.

### Mind Map SVG (Partie III)
The mind map is an 820×560 SVG. Each branch follows the same pattern:
1. A `<path>` connector from the central red rounded rectangle to the branch box
2. A branch `<rect>` with `rx="14"` and light fill / colored stroke
3. Two `<line>` connectors to sub-branch leaf `<rect>` elements (domain and shape description)

Branch colors match the graph colors above (blue, orange, green, purple).

## Editing Guidelines

- Preserve the self-contained nature — no external CSS, JS, or image files.
- When modifying SVG polyline points, recalculate pixel coordinates manually using the scale factors above.
- The document is intended for print/PDF export (max-width: 900px, white background), so avoid layout changes that break single-page rendering.
- Submission date appears at the bottom-right: `Travail rendu le mardi 21 avril 2026.`
