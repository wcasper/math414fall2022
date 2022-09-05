---
layout: page
title: Continuity
---

**Additional reading:** Simmons 2.13

### Continuous maps
In many branches of mathematics, one deals with certain fundamental objects which are essentially sets with additional structure.
We create relationships between these fundamental objects by looking at functions between them which play nice with respect to this underlying structure.
In linear algebra for example, we deal with maps between vector spaces that preserve linearity, ie. *linear transformations*.
Likewise, In abstract algebra we use maps which preserve the underlying algebraic structure (eg. group, ring, field), called *homomorphisms*.
In complex analysis, we use *holomorphic* functions which preserve underlying complex structure.
Here in topology, the additional structure we have put on sets is a notion of what it means to be "near" points.
Thus the functions that we are interested in will be those which preserve nearness, ie. points which are near $$x$$ must be mapped to points which are near $$f(x)$$.
These are precisely *continuous functions*.
For metric spaces, we express this relationship using metrics.  Later, we will see how to generalize this to more abstract topological spaces.

**Definition:** Let $$X$$ and $$Y$$ be metric spaces with metrics $$d_X$$ and $$d_Y$$, respectively.  A function $$f: X\rightarrow Y$$ is called **continuous** at $$x_0\in X$$ if

$$\forall\ \epsilon>0\ \ \exists\ \delta>0\ \ \text{such that for all $x\in X$}\ \ d_X(x,x_0) < \delta\Rightarrow d_Y(f(x),f(x_0)) < \epsilon.$$

Equivalently, we can state this as

$$\forall\ \epsilon>0\ \ \exists\ \delta>0\ \ \text{such that}\ \ f(B_\delta(x_0))\subseteq B_\epsilon(f(x_0)).$$

We call $$f$$ **continuous** if it is continuous at every point in its domain.  This can be seen to be an obvious generalization of the notion of continuity from Calculus.

In the special case that $$d_X(x_1,x_2) = d_Y(f(x_1),f(x_2))$$, the function $$f$$ is called an **isometry**.  Clearly, isometries are continuous and they can be thought of as maps which preserve distances.

We can characterize continuity in two important ways.

**Theorem:** A function $$f: X\rightarrow Y$$ is continuous at $$x_0\in X$$ if and only if for all sequences $$\{x_n\}$$ in $$X$$, $$x_n\rightarrow x$$ implies $$f(x_n)\rightarrow f(x)$$.

**Theorem:** A function $$f: X\rightarrow Y$$ is continuous if and only if $$f^{-1}(V)$$ is open for all open subsets $$V\subseteq Y$$.


### Uniform continuity

**Definition:** A function $$f: X\rightarrow Y$$ is said to be **uniformly continuous** if

$$\forall\ \epsilon>0\ \ \exists\ \delta>0\ \ \text{such that for all $x_1,x_2\in X$}\ \ d_X(x_1,x_2) < \delta\Rightarrow d_Y(f(x_1),f(x_2)) < \epsilon.$$

**Example:** The function $$f: (0,1)\rightarrow\mathbb R$$ defined by $$f(x) = 1/x$$ is continuous but not uniformly continuous.

**Theorem:** Let $$X$$ and $$Y$$ be metric spaces and suppose that $$Y$$ is complete.  Suppose $$A\subseteq X$$ is a subspace of $$X$$ whose closure is $$X$$ and that $$f: A\rightarrow Y$$ is uniformly continuous.  Then $$f$$ extends uniquely to a uniformly continuous mapping from $$X\rightarrow Y$$.


**Question:** Let $$X$$ and $$Y$$ be metric spaces.  Show that $$f:X\rightarrow Y$$ is continuous if and only if $$f^{-1}(B)$$ is closed for all closed subsets $$B\subseteq Y$$.

<details>
  <summary>Solution.</summary>
  Use the fact the a set is closed if and only if it's complement is open.
</details>






