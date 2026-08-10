# 数学试卷函数图像绘制工具

一个零依赖、单文件（纯 HTML/CSS/JavaScript）的数学绘图工具，专为**数学试卷配图**设计：用浏览器打开即可绘制函数曲线、隐式方程、不等式阴影区域和标记点，并一键导出高清 PNG / 矢量 SVG / 矢量 PDF。

> English: [English Version](#math-exam-function-plotter)

## ✨ 功能特性

- **零依赖单文件**：无需安装、无需联网，双击即用。
- **曲线绘制**：显式函数 `y=f(x)`、隐式方程（圆、椭圆等）、参数方程。
- **不等式区域**：支持 `<`、`<=`、`>`、`>=` 不等式的阴影着色。
- **区域交集模式**：对多个不等式区域一键取交集并高亮显示，可随时取消；交集边界经二分插值平滑处理，曲线边缘无锯齿。
- **单击自动标记**：单击画布自动捕捉最近的曲线交点并标记，标签按 A、B、C… 自动编号，字母被占用时自动加下标（如已有 A 则标 A₁）。
- **标记点**：任意坐标标记，支持上下标标签（如 `F_1` → F₁）、自定义颜色、标签可 360° 拖拽排版。
- **无限视窗**：鼠标拖拽平移、滚轮以光标为中心无限缩放，始终保持 1:1 比例不变形。
- **试卷风格**：数学斜体字体（Latin Modern / Times / STIX），适合直接排版进试卷；坐标轴粗细、字体大小均可调。
- **多种导出**：高清 PNG、矢量 SVG、矢量 PDF（A4 横向打印）。
- **输入安全**：表达式经字符白名单与危险标识符拦截，防止注入。

## 🚀 快速开始

用浏览器（Chrome / Edge / Firefox 均可）直接打开 `数学试卷函数图像绘制工具.html` 即可。

初始画布只显示坐标轴；点击侧栏「加载示例图」可查看椭圆、圆与直线示例。

## 📖 使用说明

### 画布操作

| 操作           | 效果                                                         |
| -------------- | ------------------------------------------------------------ |
| 空白处拖拽     | 平移画布                                                     |
| 鼠标滚轮       | 以光标为中心缩放                                             |
| 单击画布       | 在最近的曲线交点/切点处自动添加标记点（点击其他位置不标记），标签自动编号 |
| 拖动标记点字母 | 360° 调整标签位置                                            |

### 曲线与区域

点击「曲线、方程与不等式区域」卡片中的「+ 添加」，选择类型并输入表达式：

- **显式函数**：`x^2 - 3*x` 或 `y = 2*sin(x)`
- **隐式 / 区域**：`x^2/9 + y^2/4 = 1`（等值线）或 `x^2 + y^2 <= 4`（不等式阴影）
- **参数方程**：逗号分隔，如 `2*cos(t), sin(t)`（可设置 t 范围，默认 0~2π）

每条曲线可设置线型（实线 / 虚线 / 点线 / 点划线）、颜色、线宽、定义域 / t 范围。

### 表达式语法

- 乘号必须显式写出：`2*x`（不能写 `2x`）
- 次方用 `^`：`x^2`
- 内置函数：`sin, cos, tan, cot, sec, csc, arcsin, arccos, arctan, sinh, cosh, tanh, arcsinh, arccosh, arctanh, sqrt, exp, ln, lg, log2, abs`
- 常量：`pi`、`e`
- 变量：`x`、`y`（参数方程用 `t`）
- 只能包含一个关系运算符（`<` `<=` `>` `>=` `=`）

### 自动标记与交点捕捉

- 单击画布：自动寻找点击位置附近（约 25px）最近的**曲线交点或切点**并吸附标记；点击非交点/切点位置不会产生标记。
- 自动标签：按 A、B、C… 字母顺序分配；字母已被图中点占用时自动加下标（有 A 则 A₁，有 A、A₁ 则 A₂），支持显式、参数、隐式等值线任意两两相交或相切。

### 标记点

点击「标记点」卡片「+ 添加」，设置坐标与标签：

- 下标用 `_`，上标用 `^`：`F_1` 显示为 F₁，`x^2` 显示为 x²
- 多字符用花括号：`A_{in}`
- 「偏离(px)」与「角度(°)」控制标签相对点的位置，也可以直接用鼠标拖动标签排版

### 区域交集模式

1. 添加两个或更多**不等式区域**（如 `x^2+y^2<=4`、`x>=0`、`y>=0`）；
2. 勾选「区域交集模式」复选框，所有区域的**交集**部分会高亮填充（默认绿色，可用右侧色块自定义颜色）；
3. 取消勾选即恢复各区域原本的独立着色。

> 交集边界通过沿网格边二分插值精确定位，曲线边缘光滑无锯齿。

### 全局视口设置

- **网格线**：开关网格显示。
- **字体大小**：调节轴标签与标记点标签字号（16–64px）。
- **坐标轴粗细**：调节坐标轴线宽（1–5px，步进 0.1px）。

### 导出

| 按钮         | 说明                          |
| ------------ | ----------------------------- |
| 导出高清 PNG | 输出约 3000px 宽的白底高清图  |
| 导出矢量 SVG | 输出矢量 SVG，可无损缩放      |
| 生成矢量 PDF | A4 横向打印样式，输出矢量 PDF |

## 🛠 技术说明

- 纯静态单文件，无任何第三方依赖，全部数据在浏览器本地处理。
- 曲线渲染基于 SVG；隐式方程与区域使用 marching squares 等值线提取，不等式区域按 `fnR <= 0` 判定着色，交集模式对多个区域做布尔交集。
- 交点检测：曲线离散为折线（隐式用 marching squares），线段两两求交（空间哈希加速），交点 3px 内去重（三线共点只标一个），带视口/曲线缓存。
- 表达式经 `new Function` + 白名单上下文编译，并拦截 `window/document/eval/Function/this` 等危险标识符与非法字符。

## 📄 文件说明

- `数学试卷函数图像绘制工具.html` —— 工具本体（单文件，可独立分发）

---

# Math Exam Function Plotter

A zero-dependency, single-file (pure HTML/CSS/JavaScript) math plotting tool designed for **math exam illustrations**: open it in a browser to draw function curves, implicit equations, inequality regions and marked points, then export high-resolution PNG / vector SVG / vector PDF with one click.



## ✨ Features

- **Zero-dependency single file**: no install, no network needed; just open it.
- **Curves**: explicit functions `y=f(x)`, implicit equations (circles, ellipses, ...), parametric equations.
- **Inequality regions**: shading for `<`, `<=`, `>`, `>=` inequalities.
- **Region intersection mode**: highlight the intersection of multiple inequality regions with one click (toggleable). Boundaries are located by binary-search interpolation, so curve edges stay smooth with no jagged pixels.
- **Click-to-mark**: click the canvas to auto-capture the nearest curve intersection and mark it; labels auto-number A, B, C… and get subscripts when taken (e.g. if A already exists, mark A₁).
- **Marked points**: arbitrary coordinates, super/subscript labels (e.g. `F_1` → F₁), custom colors, 360° draggable label placement.
- **Infinite viewport**: drag to pan, mouse-wheel zoom centered on the cursor, always locked to a true 1:1 scale.
- **Exam style**: math-italic fonts (Latin Modern / Times / STIX), ready for typesetting into papers; adjustable axis thickness and label font size.
- **Multiple exports**: high-res PNG, vector SVG, vector PDF (A4 landscape print).
- **Input safety**: expressions are validated with a character whitelist and dangerous-identifier blocking.

## 🚀 Quick Start

Open `数学试卷函数图像绘制工具.html` directly in any modern browser (Chrome / Edge / Firefox).

The canvas starts with only the coordinate axes; click **Load Example** (加载示例图) in the sidebar to see a sample ellipse, circle and line.

## 📖 Usage

### Canvas Interaction

| Action              | Effect                                                       |
| ------------------- | ------------------------------------------------------------ |
| Drag on empty space | Pan the canvas                                               |
| Mouse wheel         | Zoom centered on the cursor                                  |
| Click on canvas     | Auto-add a marked point at the nearest curve intersection or tangency point; clicking elsewhere adds nothing; label auto-numbered |
| Drag a point label  | Rotate/position the label 360°                               |

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

### Click-to-Mark & Intersection Snapping

- Click the canvas: the nearest **curve intersection or tangency point** within ~25px of the click is captured and marked; clicking anywhere else adds no point.
- Auto labels: assigned in A, B, C… order; if a letter is already used, a subscript is appended (A taken → A₁, A and A₁ taken → A₂). Works for any pair of explicit, parametric and implicit contour curves, including tangency cases.

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

### Global Viewport Settings

- **Grid**: toggle grid lines.
- **Font size**: adjust axis label and point label size (16–64px).
- **Axis thickness**: adjust coordinate axis stroke width (1–5px, step 0.1px).

### Export

| Button              | Description                          |
| ------------------- | ------------------------------------ |
| Export High-Res PNG | White-background PNG at ~3000px wide |
| Export Vector SVG   | Lossless vector SVG                  |
| Generate Vector PDF | A4 landscape print-style vector PDF  |

## 🛠 Technical Notes

- Pure static single file, zero third-party dependencies; everything runs locally in the browser.
- Rendering is SVG-based; implicit equations and regions are extracted with a marching-squares contour algorithm; inequality regions are shaded when `fnR <= 0`; intersection mode computes the boolean intersection of multiple regions.
- Intersection detection: curves are discretized into polylines (marching squares for implicit), segment pairs are tested with a spatial hash for speed, points within 3px are deduplicated (three lines sharing one point produce a single mark), cached per viewport/curve state.
- Expressions are compiled via `new Function` with a whitelisted context, and dangerous identifiers (`window`/`document`/`eval`/`Function`/`this`) and illegal characters are blocked.

## 📄 Files

- `数学试卷函数图像绘制工具.html` — the tool itself (single file, independently distributable)
