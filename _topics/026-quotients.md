---
layout: page
title: Quotient Spaces
---

One very useful way of creating new topological spaces out of old ones is by "gluing together" certain points.
Mathematically this is accomplished by equivalence relations, where points belonging to the same equivalence class are glued together to become a single point.

### Quotients

Let $$X$$ be a set with an equivalence relation $$\sim$$.  Recall that the **equivalence class** of $$a\in X$$ is the set

$$[a] = \{x\in X: a\sim x\}.$$

**Definition:** The set $$X/\sim$$ of all equivalence classes of $$X$$ with respect to the relation $$\sim$$ is called the **quotient** of $$X$$ by $$\sim$$.

The natural function

$$q: X\rightarrow X/\sim,\quad a\mapsto [a]$$

is called the **quotient map**.

In the case that $$X$$ is a topological space, the quotient can be endowed with a topology also, making it a topological space.
The topology we choose is specifically the one which makes the quotient map $$q$$ continuous.

**Definition:** Let $$\tau_X$$ be the topology of $$X$$.  The **quotient topology** is

$$\tau_{X/\sim} = \{U\subseteq X/\sim: q^{-1}(U)\in \tau_X\}.$$

The set $$X/\sim$$ endowed with the quotient topology is called a **quotient space**.


### Examples of quotient spaces

**Example 1:** Let $$X = [0,1]$$ and let $$\sigma$$ be the equivalence relation defined by

$$\sim = \{(t,t): t\in [0,1]\}\cup \{(0,1),(1,0)\}.$$

Then $$X/\sim$$ is homeomorphic to the unit circle

$$S^1 = \{(x,y)\in\mathbb R^2: x^2+y^2 = 1\}.$$

**Example 2:** To construct the **line with two origins**, we start with $$X=\mathbb R\times \{0,1\}$$ and define

$$\sim = \{((t,k),(t,k)): t\in \mathbb{R},\ k=0,1\}\cup\{((t,j),(t,k)): t\in \mathbb{R}\backslash\{0\},\ j,k=0,1\}.$$


**Example 3:** To construct real projective space $$\mathbb RP^n$$, we start out with $$\mathbb R^n$$ and consider the equivalence relation

$$(x_1,\dots, x_n)\sim (\lambda x_1,\dots, \lambda x_n),\ \forall x_1,\dots,x_n,\lambda\in\mathbb R,\ \lambda\neq 0.$$



