---
layout: page
title: Path Homotopy
---

Two paths which can be continuously deformed into one-another are called homotopic.

### Paths and Loops

**Definition:** A **path** in a topological space $$X$$ is a continuous function

$$\gamma: [0,1]\rightarrow X.$$

When $$\gamma(0) = a$$ and $$\gamma(1) = b$$, we call this a **path from a to b**.
If $$a=b$$, we call this a **loop**, or more specifically a **loop based at a**.

In particular, loops are paths but not every path is a loop.

**Example:** The **constant loop** based at $$a$$ is the constant function $$\gamma: [0,1]\rightarrow X$$ defined by $$\gamma(t) = a$$ for all $$t$$.

There are a variety of ways we can make new paths in $$X$$ out of old ones.

* If $$\gamma$$ is a path in $$X$$ from $$a$$ to $$b$$, then the **reverse path** is $$\overline\gamma(t) = \gamma(1-t)$$ is a reverse path from $$b$$ to $$a$$.
* If $$\gamma$$ and $$\eta$$ are two paths in $$X$$, then the **concatenation** $$\eta * \gamma$$ is the path

$$(\eta * \gamma)(t) = \left\lbrace
\begin{array}{cc}
\gamma(2t), & 0\leq t\leq 1/2\\
\eta(2t-1), & 1/2\leq t\leq 1
\end{array}
\right\rbrace.$$

In particular if $$\gamma$$ is a path from $$a$$ to $$b$$ and $$\eta$$ is a path from $$b$$ to $$c$$, then $$\eta * \gamma$$ is a path from $$a$$ to $$c$$.

### Homotopy

We say that there is a homotopy from a path $$\gamma$$ to a path $$\eta$$ if there is a way of continuously morphing $$\gamma$$ into $$\eta$$.
More rigorously, we define this as follows.

**Definition:** Let $$\gamma$$ and $$\eta$$ be two paths from $$a$$ to $$b$$ in $$X$$.  A **homotopy from** $$\gamma$$ **to** $$\eta$$ is a continuous function

$$h: [0,1]\times [0,1]\rightarrow X$$

satisfying $$h(s,0) = a$$, and $$h(s,1)=b$$ for all $$s$$ and $$h(0,t) = \gamma(t)$$ and $$h(1,t) = \eta(t)$$ for all $$t$$.  If there is a homotopy from $$\gamma$$ to $$\eta$$, then we say $$\gamma$$ is homotopic to $$\eta$$.


**Example:** Let $$X = \{(x,y)\in\mathbb R^2: x^2+y^2\leq 1\}$$ be the closed unit disk in $$\mathbb{R}$$.  Then the path from $$(1,0) to (-1,0)$$ given by

$$\gamma(t) = (\cos(\pi t),0),\quad t\in [0,1]$$

is homotopic to the path

$$\eta(t) = (\cos(\pi t), \sin(\pi t)),\quad t\in [0,1]$$

with the homotopy

$$h: [0,1]\times [0,1]\rightarrow X,\quad h(s,t) = (s\cos (\pi t), s\sin(\pi t)).$$

**Example:** Let $$X = \{(x,y)\in\mathbb R^2: x^2 + y^2 \leq 1,\ (x,y)\neq (0,0)\}.$$  Then there is no homotopy from 

$$\eta(t) = (\cos(\pi t), -\sin(\pi t)),\quad t\in [0,1]$$

to 

$$\eta(t) = (\cos(\pi t), \sin(\pi t)),\quad t\in [0,1]$$

**Theorem:** Let $$X$$ be a topological space and $$a,b\in X$$.  The property of being homotopic defines an equivalence relation on the set of all paths from $$a$$ to $$b$$ on $$X$$.

**Definition:** The **homotopy class** of a path $$\gamma$$ is the set

$$[\gamma] = \{eta:\ \text{$\eta$ is homotopic to $\gamma$}\}.$$


**Theorem:**
Let $$[\eta]$$ and $$[\gamma]$$ be two paths based at $$a$$.  Then the operation

$$[\eta] * [\gamma] := [\eta * \gamma]$$ is well-defined.


