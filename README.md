【基础规则】
鼠标交互：可以在右侧画布上直接拖拽鼠标平移，或用滚轮缩放。
严格 1:1：系统强制保持横纵坐标 1:1，无论您输入什么范围，图像绝不变形。
代数语法：乘号必须显式写出（如 2*x，不能写 2x），次方用 ^（如 x^2）。
内置函数：sin, cos, tan, arcsin, arccos, arctan, sqrt(开根), exp, ln, lg, abs(绝对值)。常量：pi, e。
【方程与曲线输入示例】
显式函数：直接填 x^2 - 3*x，或者完整填 y = 2*sin(x)。
隐式曲线(圆/椭圆/双曲线)：选择“隐式/区域”，输入 x^2/9 + y^2/4 = 1，或 (x-2)^2 + (y-1)^2 = 4。
参数方程：逗号隔开，如 2*cos(t), sin(t)。右侧可定义 t 的区间。
【阴影区域(线性规划)】
选择“隐式/区域”，输入含有 <, <=, >, >= 的表达式。
示例：x^2 + y^2 <= 4 (圆的内部)；y >= 2*x + 1 (直线上方的半平面)。
【标记点与符号上下标】
在标签框中，下标用 _，上标用 ^。
示例：F_1 会显示为 F₁，x^2 显示为 x²。如果内容较多请加花括号如 A_{in}。
通过修改偏离距离和角度，可以将文字绕着点以任意方位摆放（0度在右，90度在上）。



# Basic Rules
Mouse Interaction: Drag the mouse directly on the canvas on the right to pan, or use the mouse wheel to zoom.
Strict 1:1 Aspect Ratio: The system enforces a 1:1 ratio for horizontal and vertical coordinates. The image will never be distorted no matter what range you input.
Algebra Syntax: Multiplication signs must be explicitly written (e.g. 2*x instead of 2x); caret symbol ^ denotes exponents (e.g. x^2).
Built-in Functions: sin, cos, tan, arcsin, arccos, arctan, sqrt (square root), exp, ln, lg, abs (absolute value). Constants: pi, e.

# Examples for Entering Equations and Curves
Explicit Functions: Simply input x^2 - 3*x, or the full form y = 2*sin(x).
Implicit Curves (Circles/Ellipses/Hyperbolas): Select "Implicit/Region", then input expressions such as x^2/9 + y^2/4 = 1 or (x-2)^2 + (y-1)^2 = 4.
Parametric Equations: Separate expressions with commas, e.g. 2*cos(t), sin(t). The interval of variable t can be defined on the right side.

# Shaded Regions (Linear Programming)
Select "Implicit/Region" and input expressions containing <, <=, >, >=.
Examples: x^2 + y^2 <= 4 (interior of a circle); y >= 2*x + 1 (half-plane above a straight line).

# Marked Points and Subscripts/Superscripts for Symbols
In the label input box, underscore _ stands for subscripts and caret ^ stands for superscripts.
Examples: F_1 renders as F₁, x^2 renders as x². Use curly braces for multi-character subscripts or superscripts, e.g. A_{in}.
Adjust offset distance and angle to place text around a point in any orientation (0 degrees points right, 90 degrees points upward).
