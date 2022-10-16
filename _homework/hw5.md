---
layout: page
title: Homework 5
permalink: /homework/hw5
---

### Directions
Solve the following problems and type up your solutions.  Your solutions should be provided in one of the following formats (in order of preference)
* typed up in $$\LaTeX$$ and submitted as a PDF on Canvas
* written legibly on blank paper, scanned into a PDF and then uploaded on Canvas
* written on ancient parchement with a quill and then flown to the instructor via owl post like in Harry Potter

If you go with the first strategy, you may wish to check out Overleaf which is a free and intuitive website for generating $$\LaTeX$$ documents online.
If you wish to use the second method and don't own a scanner at home, you can check out the numerous scanning apps available for smartphones.

**Problem 1:**  

Let $$X= [0,1]$$ be the subspace of $$\mathbb R$$ with the Euclidean topology.
A **dyadic rational** is a rational number of the form $$a/2^k$$ for some integers $$a$$ and $$k$$.

* (A) Prove that for any dyadic rational $$r\in (0,1)$$, the sets $$[0,r)$$ and $$(r,1]$$ are open subsets of $$X$$ for all $$k\geq 0$$.
* (B) Prove that the collection

$$\{[0,r): r\in (0,1)\ \text{dyadic rational}\}\cup \{(r,1]: r\in (0,1)\ \text{dyadic rational}\}$$

is a subbasis for the topology of $$X$$.

**Problem 2:**

Let $$X$$ and $$Y$$ be topological spaces and let $$\gamma$$ be a subbasis for the topology on $$Y$$.
Prove that a function $$f: X\rightarrow Y$$ is continuous if and only if $$f^{-1}(V)$$ is open for all $$V\in\gamma$$.


**Problem 3:**

You are walking in the forest at midnight.  While passing a magical pond, a frog jumps out at you and croaks that if $$f: [0,1]\rightarrow \mathbb R$$ is a real-valued function whose range is $$(0,1)$$, then $$f$$ must be continuous.  In such an important situation, you only have three options:
* use the theorems we learned in class to carefully prove the frog is right;
* come up with a counter-example;
* or carefully back away from the frog and get this problem wrong.

Assume the frog is a friend of Euclid, so they only care about the Euclidean topology.

**Problem 4:**

Let $$\{X_i: i\in I\}$$ be a collection of topological spaces and suppose $$f$$ is a function from a topological space $$W$$ to the product space $$\prod_{i\in i} X_i$$ (with the product topology).  Prove that $$f$$ is continuous if and only if the compositions $$\pi_i\circ f: W\rightarrow X_i$$ are continuous for all $$i\in I$$.

**Problem 5:**

Given a real number $$x\in [0,1]$$ the **binary expansion** of $$x$$ is a sequence of zeros and ones $$(x_1,x_2,x_3,\dots)$$ with $$x_i\in\{0,1\}$$ with

$$x = \frac{x_1}{2} + \frac{x_2}{2^2} + \frac{x_3}{2^3} + \dots.$$

From one perspective, this is like a decimal expansion of $$x$$ but in base $$2$$.
This is also how the value of a real number can be stored on a computer.

* (A) Show that every real number in $$[0,1]$$ has a unique binary expansion.
* (B) Let $$X_i = \{0,1\}$$ for all $$i\in\mathbb N$$.  Use $$A$$ to prove that the function

$$f:\prod_{i=1}^\infty X_i\rightarrow [0,1],\quad (x_1,x_2,x_3,\dots)\mapsto \sum_{i=1}^\infty x_i2^{-i}$$

is bijective.

* (C) Suppose that $$X_i$$ has the discrete topology for all $$i$$ and that $$\prod_{i=1}^\infty X_i$$ has the product topology.  Show that the preimages of the sets $$[0,r)$$ and $$(r,1]$$ are open for all dyadic rationals $$r\in (0,1)$$.

* (D) Use (C) and Problem 2 to conclude that the function $$f$$ is continuous.

* (E) Finally, use the function $$f$$ to prove that $$[0,1]$$ is compact.

