---
layout: page
title: Metric spaces
---

**Additional reading:** Simmons 2.9

### Basic definition

The thing that distinguishes a topological space $$X$$ from a set is that a topological space has an explicit definition of what it means to be "in the neighborhood of" a point.
The most intuitive way to accomplish this is by defining a notion of the distance between points.
We do this by defining a distance function or **metric**, a function $$d: X\times X\rightarrow \mathbb R$$ whose value $$d(x,y)$$ is the distance between $$x$$ and $$y$$.

The distance function $$d(x,y)$$ cannot be completely crazy.  Instead, it should satisfy a few properties which agree with our intuition about how our notion of how distances should behave.  For example, we don't expect the distance between any two points to be negative so it makes sense to require $$d(x,y)\geq 0$$.  Moreover, the distance between different points should be nonzero, meaning $$d(x,y) = 0 \Leftrightarrow x=y$$.  Likewise, we expect that the distance from $$x$$ to $$y$$ should be the same as the distance from $$y$$ to $$x$$, so we impose $$d(x,y) = d(y,x)$$.  Finally, if we are moving from a point $$x$$ to a point $$y$$ then forcing ourselves to pass through a particular intermediate point $$z$$ can only make the distance larger.  This imposes a constraint called the **triangle inequality**

$$d(x,y)\leq d(x,z) + d(z,y).$$

Putting these three properties together, we arrive at the definition of a metric.

**Definition:** Let $$X$$ be a set.  A **metric** is a function $$d: X\times X\rightarrow\mathbb R$$ satisfying the following three properties:
* (i)   $$d(x,y)\geq 0$$ and $$d(x,y) = 0$$ if and only if $$x=y$$;
* (ii)  $$d(x,y) = d(y,x)$$ (*symmetry*);
* (iii) $$d(x,y)\leq d(x,z) + d(z,y)$$ (*triangle inequality*).

A set $$X$$ endowed with a metric is called a **metric space**.

### Examples of metric spaces

**Example 1:** Our first example is the real line $$\mathbb R$$ with the metric $$d(x,y) = \vert x-y\vert$$.  It is easy to see that all three properties a metric are satisfied, making $$\mathbb R$$ into a metric space.  More generally the usual notice of distance in $$\mathbb R^n$$ 

$$d(x,y) = \sqrt{(x_1-y_1)^2 + (x_2-y_2)^2 + \dots + (x_n-y_n)^2}$$

for $$x = (x_1,x_2,\dots,x_n)$$ and $$y = (y_1,y_2,\dots,y_n)$$ defines a metric on $$\mathbb R^n$$.  This is called the **Euclidean metric** on $$\mathbb R^n$$.

**Example 2:** The set $$\mathbb C$$ of complex numbers with the metric

$$d(z_1,z_2) = \sqrt{(x_1-x_2)^2 + (y_1-y_2)^2},\quad z_i = x_i + iy_i$$

makes the complex numbers into a metric space.  In terms of the absolute value of complex numbers, we can rewrite this as $$d(z_1,z_2) = \vert z_1-z_2\vert$$, paralleling the usual metric on $$\mathbb R$$.

**Example 3:** Let $$X$$ be a set.  The **discrete metric** on $$X$$ is defined to be

$$
d(x,y) = \left\lbrace\begin{array}{cc}
0 & x=y,\\
1 & x\neq y.
\end{array}\right.
$$

**Example 4:** Let $$X$$ be the set of continuous, real-valued functions on the closed interval $$[0,1]$$.  The **uniform metric** on $$X$$ is

$$d(f,g) = \sup_{t\in [0,1]} |f(t)-g(t)|.$$

**Example 5:** Let $$p$$ be a prime number.  The **p-adic metric** on $$\mathbb Q$$ is defined by

$$
d(x,y) = \left\lbrace\begin{array}{cc}
0 & x=y,\\
p^{-\max_k\{k:\ \ p^k\ \text{divides}\ (x-y)\}}  & x\neq y.
\end{array}\right.
$$

This unusual metric is particularly interesting and plays a central role in analytic number theory.

**Question:** Which of the following functions are metrics on $$\mathbb R$$.
* (A) $$d(x,y) = \frac{\vert x-y\vert }{1 + \vert x-y\vert }$$
* (B) $$d(x,y) = (x-y)^2$$
* (C) $$d(x,y) = 0$$


<details>
  <summary>Answer for (A).</summary>
  This is a metric.  Try proving that it satisfies the triangle inequality.
</details>
<details>
  <summary>Answer for (B).</summary>
  This is a not a metric.  It fails to satisfy the triangle inequality.  Can you show this?
</details>
<details>
  <summary>Answer for (C).</summary>
  This is a not a metric because it fails to satisfy the property $$d(x,y)=0\Leftrightarrow x=y$$
</details>







