# Drawing Tool Instructions
## 1. Basic Rules
1. **Mouse Interaction**: Drag the mouse directly on the right canvas to pan; scroll the mouse wheel to zoom in/out.
2. **Strict 1:1 Aspect Ratio**: The system enforces a 1:1 ratio for horizontal and vertical axes. Graphs will never distort no matter what coordinate range you input.
3. **Algebra Syntax Rules**
    - Multiplication sign must be explicitly written: e.g. `2*x` (do NOT write `2x`)
    - Exponent operator: `^`, e.g. `x^2`
4. **Built-in Functions & Constants**
    - Trigonometric & inverse trigonometric: `sin`, `cos`, `tan`, `arcsin`, `arccos`, `arctan`
    - Other functions: `sqrt` (square root), `exp`, `ln`, `lg`, `abs` (absolute value)
    - Math constants: `pi`, `e`

## 2. Equation & Curve Input Examples
### Explicit Functions
Enter the expression directly like `x^2 - 3*x`, or the full equation `y = 2*sin(x)`.

### Implicit Curves (Circles, Ellipses, Hyperbolas)
Select **Implicit / Region** mode, then input equations:
- Ellipse: `x^2/9 + y^2/4 = 1`
- Circle: `(x-2)^2 + (y-1)^2 = 4`

### Parametric Equations
Separate x and y expressions with a comma. Set the range of parameter `t` on the right panel.
```
2*cos(t), sin(t)
```

## 3. Shaded Regions (Linear Programming)
Select **Implicit / Region** mode, input inequalities containing `<`, `<=`, `>`, `>=`:
- Interior of a circle: `x^2 + y^2 <= 4`
- Half-plane above a straight line: `y >= 2*x + 1`

## 4. Marked Points & Superscript / Subscript Notation
### Format Rules for Superscripts & Subscripts
- Subscript with `_`: `F_1` → $F_1$
- Superscript with `^`: `x^2` → $x^2$
- Wrap multi-character scripts in curly braces `{}`: `A_{in}` → $A_{in}$

### Text Position Adjustment
Adjust offset distance and angle to place labels around points:
- 0°: Text to the right of the point
- 90°: Text above the point



# 绘图工具使用说明
## 一、基础规则
1. **鼠标交互**：右侧画布可直接拖拽鼠标平移画面，鼠标滚轮缩放画布。
2. **严格1:1坐标轴**：系统强制横、纵坐标比例1:1，输入任意坐标范围，图形不会拉伸变形。
3. **代数书写语法**
    - 乘法必须显式书写：例 `2*x`，禁止简写 `2x`
    - 次方运算符使用 `^`：例 `x^2`
4. **内置函数与常量**
    - 三角函数/反三角函数：`sin`、`cos`、`tan`、`arcsin`、`arccos`、`arctan`
    - 其他函数：`sqrt`(开根号)、`exp`、`ln`、`lg`、`abs`(绝对值)
    - 数学常量：`pi`、`e`

## 二、方程与曲线输入示例
### 1. 显式函数
直接填写表达式 `x^2 - 3*x`，或完整等式 `y = 2*sin(x)`。

### 2. 隐式曲线（圆、椭圆、双曲线）
绘图类型选择「隐式/区域」，输入等式：
- 椭圆：`x^2/9 + y^2/4 = 1`
- 圆：`(x-2)^2 + (y-1)^2 = 4`

### 3. 参数方程
x、y表达式用逗号分隔，右侧设置参数`t`取值区间：
```
2*cos(t), sin(t)
```

## 三、阴影区域（线性规划绘图）
绘图类型选择「隐式/区域」，输入包含 `<`、`<=`、`>`、`>=` 的不等式表达式：
1. 圆形内部：`x^2 + y^2 <= 4`
2. 直线上半平面：`y >= 2*x + 1`

## 四、标记点与符号上下标
### 1. 上下标书写规则
- 下标使用 `_`：`F_1` → $F_1$
- 上标使用 `^`：`x^2` → $x^2$
- 多字符上下标加大括号 `{}`：`A_{in}` → $A_{in}$

### 2. 文字位置调整
修改偏离距离、角度可调整文字相对标记点方位：
- 0°：文字在点右侧
- 90°：文字在点上方
