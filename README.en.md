# Math Exam Function Plotter

A zero-dependency, single-file (pure HTML/CSS/JavaScript) math plotting tool designed for **math exam illustrations**: open it in a browser to draw function curves, implicit equations, inequality regions and marked points, then export high-resolution PNG / vector SVG / vector PDF with one click.

> 中文版：[README.md](./README.md)

## ✨ Features

- **Zero-dependency single file**: no install, no network needed; just open it.
- **Curves**: explicit functions `y=f(x)`, implicit equations (circles, ellipses, ...), parametric equations.
- **Inequality regions**: shading for `<`, `<=`, `>`, `>=` inequalities.
- **Region intersection mode**: highlight the intersection of multiple inequality regions with one click (toggleable). Boundaries are located by binary-search interpolation, so curve edges stay smooth with no jagged pixels.
- **Marked points**: arbitrary coordinates, super/subscript labels (e.g. `F_1` → F₁), custom colors, 360° draggable label placement.
- **Infinite viewport**: drag to pan, mouse-wheel zoom centered on the cursor, always locked to a true 1:1 scale.
- **Exam style**: math-italic fonts (Latin Modern / Times / STIX), ready for typesetting into papers.
- **Multiple exports**: high-res PNG, vector SVG, vector PDF (A4 landscape print).
- **Input safety**: expressions are validated with a character whitelist and dangerous-identifier blocking.

## 🚀 Quick Start

Open `数学试卷函数图像绘制工具.html` directly in any modern browser (Chrome / Edge / Firefox).

The canvas starts with only the coordinate axes; click **Load Example** (加载示例图) in the sidebar to see a sample ellipse, circle and line.

## 📖 Usage

### Canvas Interaction

| Action | Effect |
| ------ | ------ |
| Drag on empty space | Pan the canvas |
| Mouse wheel | Zoom centered on the cursor |
| Drag a point label | Rotate/position the label 360° |

### Curves & Regions

Click **+ Add** (添加) in the "Curves, Equations & Inequality Regions" card, choose a type and enter an expression:

- **Explicit**: `x^2 - 3*x` or `y = 2*sin(x)`
- **Implicit / Region**: `x^2/9 + y^2/4 = 1` (contour) or `x^2 + y^2 <= 4` (shaded inequality)
- **Parametric**: comma-separated, e.g. `2*cos(t), sin(t)` (t-range configurable, default 0–2π)

Each curve supports line style (solid / dashed / dotted / dash-dot), color, stroke width and domain / t-range.

### Expression Syntax

- Multiplication must be explicit: `2*x` (not `2x`)
- Power with `^`: `x^2`
- Built-in functions: `sin, cos, tan, cot, sec, csc, arcsin, arccos, arctan, sinh, cosh, tanh, arcsinh, arccosh, arctanh, sqrt, exp, ln, lg, log2, abs`
- Constants: `pi`, `e`
- Variables: `x`, `y` (`t` for parametric equations)
- At most one relation operator (`<` `<=` `>` `>=` `=`)

### Marked Points

Click **+ Add** in the "Marked Points" (标记点) card, then set coordinates and label:

- Subscript with `_`, superscript with `^`: `F_1` renders as F₁, `x^2` as x²
- Multiple characters in braces: `A_{in}`
- "Offset (px)" and "Angle (°)" control the label position relative to the point; you can also drag the label directly

### Region Intersection Mode

1. Add two or more **inequality regions** (e.g. `x^2+y^2<=4`, `x>=0`, `y>=0`);
2. Tick the **Region Intersection Mode** (区域交集模式) checkbox — the **intersection** of all regions is highlighted (green by default; pick a custom color with the swatch on the right);
3. Untick it to restore each region's independent shading.

> The intersection boundary is located by binary-search interpolation along grid edges, so curve edges are smooth with no aliasing.

### Export

| Button | Description |
| ------ | ----------- |
| Export High-Res PNG | White-background PNG at ~3000px wide |
| Export Vector SVG | Lossless vector SVG |
| Generate Vector PDF | A4 landscape print-style vector PDF |

## 🛠 Technical Notes

- Pure static single file, zero third-party dependencies; everything runs locally in the browser.
- Rendering is SVG-based; implicit equations and regions are extracted with a marching-squares contour algorithm; inequality regions are shaded when `fnR <= 0`; intersection mode computes the boolean intersection of multiple regions.
- Expressions are compiled via `new Function` with a whitelisted context, and dangerous identifiers (`window`/`document`/`eval`/`Function`/`this`) and illegal characters are blocked.

## 📄 Files

- `数学试卷函数图像绘制工具.html` — the tool itself (single file, independently distributable)