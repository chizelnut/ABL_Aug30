# 神经网络连线实验 · Neural Network Wires Lab

**▶ 打开实验 / Open the lab: <https://chizelnut.github.io/ABL_lab2/>**

AI Builders Lab — Lesson 2 · 2026年8月30日

---

## 这是什么 · What this is

一个可以**用手拨动神经网络权重**的实验。左边 4×4 的画布是 16 个输入神经元，
中间 4 个隐藏神经元，右边 3 个输出（0、1、7）。**点任意一条连线，拖动滑块改它的权重，
右边的分数立刻就变。** 全部在浏览器里跑，不用装任何东西，手机和 iPad 也能用。

A hands-on lab where you **turn the weights of a neural network by hand**. The 4×4 canvas on
the left is 16 input neurons; 4 hidden neurons in the middle; 3 outputs (0, 1, 7) on the right.
**Click any wire, drag the slider, and the scores on the right change instantly.** Runs entirely
in the browser — nothing to install, works on phones and iPads.

界面有中英文切换（右上角按钮）。 · Use the button in the top-right to switch languages.

## 怎么玩 · How to use it

1. 点 **0 / 1 / 7** 按钮画一个数字，或者自己点格子画。
2. 点 **随机所有权重**，看看一个没训练过的网络会猜成什么。
3. 点中一条 **隐藏 → 输出** 的线，把滑块拉到 +1 或 −1，看那个输出的分数条怎么变。
4. 点 **全部清零** —— 所有权重是 0 时，三个输出打平，网络什么也判断不出来。
   训练要做的，就是把这些 0 一点一点推到正确的数值上。

## 为什么有这个实验 · Why it exists

Lesson 1 里我们跑了 `model.fit()`，看到准确率从 10% 涨到 97%，
但 `fit` 到底在改什么，是看不见的。

这就是知识点 **M2-16（前向 → 代价 → 反向 → 更新）** 的那一层。
这个实验把网络缩小到能用手玩的尺寸：**76 条线，每条都能亲手拨**。
学生先用手感受"改一条线，输出就跟着变"，再去理解训练算法几百万次地做同一件事。

Lesson 1 ran `model.fit()` and watched accuracy climb from 10% to 97% — but *what* `fit`
changes stays invisible. This lab shrinks the network to 76 wires you can move by hand, so
students feel "change one wire, the output moves" before hearing that backpropagation does
exactly that, millions of times over.

## 教学时的两点提醒 · Two notes for teaching

- **重点在第二层。** 隐藏 → 输出的 12 条线又粗又好点，因果关系一眼可见。
  输入 → 隐藏那 64 条线扇形密集，其中约 7 条被别的线压住、点不到 —— 演示时用第二层。
- **"全部清零"是最好的一张牌。** 权重全 0 → 平局 → 网络毫无用处。
  这就是训练开始前的样子。

- **The second layer is where the demo lives.** The 12 hidden→output wires are thick, easy to
  hit, and their effect is immediate. The 64 input→hidden wires fan out densely and about 7 of
  them sit underneath others and cannot be clicked. Demo on the second layer.
- **"Set all to zero" is the strongest single move.** All weights 0 → a three-way tie → the
  network is useless. That is exactly what a network looks like before training.

## 简化之处 · Simplifications

真实的手写识别网络是 784 个输入、十万条以上的连线、权重是自动学出来的任意小数，
输出还要经过 softmax 换算成概率。这里为了能用手玩，缩到 16 个输入、4 个隐藏神经元、
权重范围 −1 到 +1，输出直接比分数大小。

A real handwriting network has 784 inputs, 100k+ wires, learned decimal weights, and a softmax
on the output. This one is deliberately small enough to touch.

---

单个 HTML 文件，无外部依赖。 · Single self-contained HTML file, no external dependencies.
