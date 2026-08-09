这里为您设计了一份排版整洁、内容详尽的 `README.md` 文件，包含中英文双语版本。您可以直接复制保存。

---

# Math Paper Graphing Tool (数学试卷函数图像绘制工具)

📄 [中文版 (Chinese)](#中文说明) | 📄 [English Version](#english-description)

---

## 中文说明

**数学试卷函数图像绘制工具**是一个完全基于纯 HTML + CSS + JavaScript 开发的**单文件**离线应用。专为数学教师、教辅编辑和数学爱好者设计，旨在快速生成符合“中国中学试卷规范”的完美数学坐标系与函数图像。

无需安装庞大的软件，无需学习复杂的 TikZ 语法，只需双击打开即可使用。

### ✨ 核心特性

*   📦 **单文件 & 零依赖：** 没有任何外部库（无 CDN、无 React/Vue、无 ECharts），断网环境完美运行，双击 `.html` 即用。
*   📐 **试卷级排版标准：**
    *   严格锁定 **1:1 横纵轴比例**，无论如何缩放平移，圆永远是圆，绝对变形。
    *   无多余刻度线，采用标准的 V 形坐标轴箭头。
    *   原点 $O$ 及坐标轴标签 $x, y$ 采用规范的数学斜体衬线字体。
*   🧮 **强大的数学引擎：**
    *   **显式函数：** 支持 `y = x^2 - 3*x` 等常规函数。
    *   **隐式方程：** 采用 Marching Squares 算法，完美绘制圆、椭圆 `x^2/9 + y^2/4 = 1`、双曲线等。
    *   **不等式区域（线性规划）：** 自动识别 `<, <=, >, >=` 并进行无缝平滑的半透明阴影着色。
    *   **参数方程：** 支持 `x(t), y(t)` 形式。
*   🖱️ **神级交互体验：**
    *   **无限画布：** 直接在右侧画布上**拖拽平移**，鼠标**滚轮无限缩放**。
    *   **标签排版：** 鼠标悬停在标记点的字母上，可**直接按住拖拽**，360° 绕点移动避开连线，告别繁琐的数值微调。
*   📤 **出版级导出：** 
    *   一键导出 **矢量 SVG**（无损插入 Word/PPT）
    *   一键导出 **约 3000px 宽的高清 PNG**
    *   一键生成 **矢量 PDF**（支持 A4 横向打印排版）

### 🚀 快速开始

1. 下载 `MathGraph.html` 文件。
2. 使用任何现代浏览器（Chrome, Edge, Firefox, Safari）双击打开。
3. 点击左侧面板上的 **“加载示例图”**，或者点击 **“+ 添加”** 开始绘制您的第一个方程。

### 📝 表达式书写指南

*   **基本运算：** 乘号必须写出（如 `2*x`），指数用 `^`（如 `x^2`）。
*   **支持的函数：** `sin, cos, tan, arcsin, arccos, arctan, sqrt(开根), exp, ln, lg, abs(绝对值)`。
*   **支持的常量：** `pi` ($\pi$), `e`。
*   **标记点上下标：** 在标记点的“标签”栏中，下标用 `_`，上标用 `^`。例如：输入 `F_1` 将渲染为 $F_1$，输入 `A^2` 将渲染为 $A^2$。

---

## English Description

**Math Paper Graphing Tool** is a pure HTML, CSS, and JavaScript **single-file** offline web application. It is specifically designed for math teachers, textbook editors, and math enthusiasts to quickly generate perfect, exam-standard mathematical coordinate systems and function graphs.

No need to install heavy software, no need to learn complex TikZ syntaxes. Just double-click and draw.

### ✨ Key Features

*   📦 **Single File & Zero Dependencies:** No external libraries (No CDN, no React/Vue, no third-party charting libraries). Works perfectly offline. Just double-click the `.html` file.
*   📐 **Exam-Standard Aesthetics:**
    *   Strictly locked **1:1 aspect ratio**. No matter how you pan or zoom, circles remain perfect circles.
    *   Clean layout with no distracting grid tick marks; uses standard sharp V-shaped arrows for axes.
    *   Origin $O$ and axis labels $x, y$ are rendered in standard italic serif math fonts.
*   🧮 **Powerful Math Engine:**
    *   **Explicit Functions:** e.g., `y = x^2 - 3*x`.
    *   **Implicit Equations:** Powered by the Marching Squares algorithm to perfectly render conics like `x^2/9 + y^2/4 = 1`.
    *   **Inequalities (Linear Programming):** Automatically parses `<, <=, >, >=` and renders smooth, seamless semi-transparent shaded regions.
    *   **Parametric Equations:** Supported via `x(t), y(t)` format.
*   🖱️ **Seamless Interactivity:**
    *   **Infinite Canvas:** **Click & drag** directly on the canvas to pan, and use the **mouse wheel to zoom** infinitely.
    *   **Draggable Labels:** Hover over point labels and **drag them freely** 360° around the coordinate point to avoid overlapping lines effortlessly.
*   📤 **Publication-Ready Export:** 
    *   Export as **Vector SVG** (Insert directly into Word/PPT without losing quality).
    *   Export as **High-Res PNG** (~3000px width).
    *   Generate **Vector PDF** (A4 Landscape print layout).

### 🚀 Quick Start

1. Download the `MathGraph.html` file.
2. Double-click it to open in any modern web browser (Chrome, Edge, Firefox, Safari).
3. Click **"加载示例图" (Load Example)** on the left panel, or click **"+ 添加" (+ Add)** to start graphing.

### 📝 Syntax Guide

*   **Basic Math:** Multiplication must be explicit (e.g., `2*x`), use `^` for exponents (e.g., `x^2`).
*   **Functions:** `sin, cos, tan, arcsin, arccos, arctan, sqrt, exp, ln, lg, abs`.
*   **Constants:** `pi` ($\pi$), `e`.
*   **Subscripts & Superscripts:** In the point label input, use `_` for subscript and `^` for superscript. (e.g., `F_1` renders as $F_1$, `A^2` renders as $A^2$).

---
**Tech Stack:** Pure Vanilla JavaScript, DOM API, SVG Rendering, Marching Squares Algorithm. 
**License:** MIT
