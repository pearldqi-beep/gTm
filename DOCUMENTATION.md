# Documentation — Fonctions de Référence

## Overview

This project is a static HTML educational document produced as a team assignment
for a French secondary-school mathematics course (Seconde, approximately Grade 10).
It presents, graphs, and summarises the four **fonctions de référence** (reference
functions) that form the foundation of the Seconde curriculum.

**File:** `fonctions_reference.html`  
**Technology:** Plain HTML5 with embedded CSS and SVG — no JavaScript, no server,
no build step.  
**How to open:** Load `fonctions_reference.html` directly in any web browser.

---

## Purpose

The document gives students a single self-contained reference sheet that covers:

- The algebraic expression of each function.
- Its domain of definition (ensemble de définition).
- A graphical representation that mimics a GeoGebra capture.
- A colour-coded mind map summarising the key facts.

It is intended for academic review, printing, or upload to a learning-management
system.

---

## Document Structure

The HTML file is organised into three clearly labelled sections.

### Part I — Observation and Information Recording

A table with one row per function. Each row contains:

| Column | Content |
|--------|---------|
| Function name | French label (e.g. *fonction carrée*) |
| Algebraic expression | Formula using standard notation |
| Domain of definition | Set notation with Unicode math symbols |
| Graphical representation | Inline SVG graph (160 × 140 px viewport) |

### Part II — Software Installation

A short note confirming that **XMind** was downloaded and installed to create the
mind map required for Part III.

### Part III — Mind Map

An inline SVG (820 × 560 px) mind map built in XMind. It has:

- A central node labelled **"Fonctions de référence"**.
- Four colour-coded branches, one per function.
- Sub-branches for the domain of definition and the key graphical characteristic
  of each function.

---

## The Four Reference Functions

### 1. Fonction carrée — f(x) = x²

| Property | Value |
|----------|-------|
| Expression | f(x) = x² |
| Domain | ℝ (all real numbers) |
| Graph shape | Parabola opening upward (∪) |
| Colour code | Blue `#1a7fd4` |

**Why the domain is ℝ:** any real number can be squared, so no value needs to be
excluded.

**SVG graph notes:** the polyline is pre-computed with x ranging from −3.75 to
3.75; each unit maps to 20 px on both axes (`x_px = x·20`, `y_px = −x²·20`).

---

### 2. Fonction cube — g(x) = x³

| Property | Value |
|----------|-------|
| Expression | g(x) = x³ |
| Domain | ℝ (all real numbers) |
| Graph shape | S-shaped curve (odd function) |
| Colour code | Orange `#e05c00` |

**Why the domain is ℝ:** any real number can be cubed, so no exclusion applies.

**SVG graph notes:** x ranges from −3.5 to 3.5; scale factors are 20 px per unit
on the x-axis and 6 px per unit on the y-axis (`y_px = −x³·6`) to keep the tall
curve inside the viewport.

---

### 3. Fonction racine carrée — h(x) = √x

| Property | Value |
|----------|-------|
| Expression | h(x) = √x |
| Domain | [0 ; +∞) = ℝ⁺ |
| Graph shape | Half-parabola (concave, increasing) |
| Colour code | Green `#2aaa44` |

**Why the domain excludes negatives:** the square root of a negative real number
is not defined in ℝ, so only x ≥ 0 is valid.

**SVG graph notes:** only x ≥ 0 is plotted; scale is 10 px per unit on the x-axis
and 20 px per unit on the y-axis (`y_px = −√x · 20`).

---

### 4. Fonction inverse — k(x) = 1/x

| Property | Value |
|----------|-------|
| Expression | k(x) = 1/x |
| Domain | ℝ* = ℝ \ {0} (all reals except zero) |
| Graph shape | Hyperbola with two branches |
| Colour code | Purple `#9b27af` |

**Why zero is excluded:** division by zero is undefined, so x = 0 must be removed
from the domain.

**SVG graph notes:** two separate polylines are drawn (x > 0 and x < 0); scale is
15 px per unit on both axes (`y_px = −(1/x)·15`).

---

## Visual Design

### Layout

- Maximum content width: **900 px**, centred on the page.
- Font family: **Arial, sans-serif**.
- Section headers use a blue `#1a7fd4` accent; table headers use a light blue
  background `#d0e4f7`.

### Colour System

Each function has a dedicated colour applied consistently across the table borders,
the SVG graph stroke, and the mind-map branch:

| Function | Colour | Hex |
|----------|--------|-----|
| Carrée | Blue | `#1a7fd4` |
| Cube | Orange | `#e05c00` |
| Racine carrée | Green | `#2aaa44` |
| Inverse | Purple | `#9b27af` |

### SVG Graphs

All four graphs share the same conventions:

- **Viewport:** 160 × 140 px with a ±3–4 unit visible range.
- **Axes:** grey lines with small tick marks every unit.
- **Axis labels:** `x` and `y` positioned at the tips of the axes.
- **Curve:** a `<polyline>` element with no fill and a 2 px coloured stroke.
- A watermark label *"Capture Géogébra"* indicates the graphs are styled to
  resemble GeoGebra exports.

### Mind Map SVG

- Central rectangle with rounded corners, centred at (410, 280).
- Curved `<path>` elements connect the centre to four main branch nodes.
- Each branch node connects to two leaf nodes (domain and graph characteristic).
- All paths and nodes use the same four-colour system described above.

---

## Mathematical Notation

The document uses Unicode characters throughout so that no external fonts or MathML
are required:

| Symbol | Meaning |
|--------|---------|
| 𝔻 | Domain of definition (ensemble de définition) |
| ℝ | The set of all real numbers |
| ℝ⁺ | Non-negative real numbers |
| ℝ* | Non-zero real numbers |
| `[a ; b]` | Closed interval from a to b |
| `[a ; +∞)` | Unbounded interval starting at a |

---

## Submission Information

| Field | Value |
|-------|-------|
| Course level | Seconde (French Grade 10) |
| Assignment type | Team work (équipe de maximum 3 élèves) |
| Submission date | Tuesday 21 April 2026 |
| Tools used | GeoGebra (graph reference), XMind (mind map) |

---

## File Reference

```
gTm/
└── fonctions_reference.html   # Complete self-contained educational document
```

The entire application is this single HTML file. Open it in a browser to view
the formatted document with all graphs and the mind map.
