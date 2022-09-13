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

In the special case that $$d_X(x_1,x_2) = d_Y(f(x_1),f(x_2))$$, the function $$f$$ is called an **isometric embedding**.  If $$f$$ is bijective, it's called an **isometry**.  Clearly, isometries are continuous and they can be thought of as maps which preserve distances.
In fact, two spaces which have isometries are in a strong sense "the same" as metric spaces.

We can characterize continuity in two important ways.

**Theorem:** A function $$f: X\rightarrow Y$$ is continuous at $$x_0\in X$$ if and only if for all sequences $$\{x_n\}$$ in $$X$$, $$x_n\rightarrow x$$ implies $$f(x_n)\rightarrow f(x)$$.

**Theorem:** A function $$f: X\rightarrow Y$$ is continuous if and only if $$f^{-1}(V)$$ is open for all open subsets $$V\subseteq Y$$.

**Question:** Let $$X$$ and $$Y$$ be metric spaces.  Is the following TRUE or FALSE?  If $$f:X\rightarrow Y$$ is a continuous function, then the image $$f(U)$$ of any open set $$U$$ is also open.

<details>
  <summary>True.</summary>
  Careful, consider for example a constant function.
</details>
<details>
  <summary>False.</summary>
  That's right!  Can you think of an explicit counter-example?
</details>


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

### Completions

Given our notion of "good" maps between metric spaces, as shown above we can define a **completion** of a metric space, which adds in all the "missing" points which are limits of Cauchy sequences.

**Definition:** Let $$X$$ be a metric space.  A **completion** of $$X$$ is a complete metric space $$\overline X$$ which contains $$X$$ as a dense subspace, satisfying the following property:
* for every complete metric space $$Y$$ and uniformly continuous function $$f: X\rightarrow Y$$, there exists a unique function $$\overline f: \overline X\rightarrow Y$$ extending $$f$$.

This definition is a bit confusing at first, but the next two lemmas show that (1) completions are essentially unique, and (2) if $$X$$ is complete, then it is its own completion.

**Lemma:** If $$\overline X_1$$ and $$\overline X_2$$ are two different completions of $$X$$, then there exists an isometry $$f: \overline X_1\rightarrow\overline X_2$$.

**Lemma:** If $$X$$ is complete, then $$X$$ is a completion of $$X$$.

Lastly, we have a construction showing that completions always exist!  Our construction is remniscent of Cantor's construction of $$\mathbb R$$ as the completion of $$\mathbb Q$$.
Start by considering the set $$X'$$ of all Cauchy sequences of elements of $$X$$.
Define an equivalence relation $$\sim$$ on $$X''$$ by saying $$\{x_n\}\sim\{y_n\}$$ if and only if $$\lim_n d(x_n,y_n) = 0$$.
The set $$X'$$ of all equivalence classes of elements of $$X'$$ has a metric defined by

$$d([(x_n)],[(y_n)]) = \lim_n d(x_n,y_n),$$

making $$X'$$ into a complete metric space.  Moreover, $$X$$ may be identified as the subset of $$X'$$ consisting of constant sequences.  With this identification, $$X'$$ is a completion of $$X$$.

As a consequence, we can build some interesting new spaces which are constructed like the real numbers but which are very different.
We simply start with a metric on the rational numbers other than the usual one and then take the completion.

**Definition:** The **p-adic** numbers $$\mathbb Q_p$$ are a completion of the rational numbers with respect to the $$p$$-adic metric.


