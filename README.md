# Neural Network Wires Lab

**▶ Open the lab: <https://chizelnut.github.io/ABL_lab2/>**

AI Builders Lab — Lesson 2 · August 30, 2026

---

## What this is

A hands-on lab where you **turn the weights of a neural network by hand**.

The 4×4 canvas on the left is 16 input neurons. Four hidden neurons sit in the middle, and
three outputs on the right stand for the digits 0, 1 and 7. **Click any wire, drag the slider,
and the scores on the right change instantly.**

Runs entirely in the browser — nothing to install. Works on phones and iPads.

## How to use it

1. Click **0 / 1 / 7** to draw a digit, or click the squares to draw your own.
2. Click **Randomize all weights** and see what an untrained network guesses.
3. Click one of the **hidden → output** wires and drag the slider to +1 or −1. Watch that
   output's score bar move.
4. Click **Set all to zero**. With every weight at 0 the three outputs tie and the network
   can't tell anything apart. Training is the process of pushing those zeros, a little at a
   time, toward values that work.

## Why it exists

In Lesson 1 we ran `model.fit()` and watched accuracy climb from 10% to 97% — but *what*
`fit` was changing stayed invisible.

This lab is that missing layer, knowledge point **M2-16** (forward → cost → backward →
update). It shrinks the network down to **76 wires you can move with your own hands**.
Students feel "change one wire, the output moves" first; then backpropagation is just that
same fact, exploited a few million times over.

## Two notes for teaching

- **The second layer is where the demo lives.** The 12 hidden→output wires are thick, easy to
  click, and their effect is immediate. The 64 input→hidden wires fan out densely, and about
  7 of them sit underneath other wires and can't be clicked at all. Demo on the second layer.
- **"Set all to zero" is the strongest single move in the lab.** All weights zero → a
  three-way tie → the network is useless. That is exactly what a network looks like before
  training starts.

## Simplifications

A real handwriting network has 784 inputs, over a hundred thousand wires, learned decimal
weights, and a softmax that converts scores into probabilities. This one is deliberately
small enough to touch: 16 inputs, 4 hidden neurons, weights from −1 to +1, and raw scores
compared directly.

---

Single self-contained HTML file. No external dependencies.
