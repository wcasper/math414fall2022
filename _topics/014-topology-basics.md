---
layout: page
title: Topology Basics
---

**Additional reading:** Simmons 3.17

All the interesting properties that we discussed for sets in metric spaces, interiors, closures, limit points, and boundaries, can be extended to topological spaces.
In fact, in many ways these definitions tend to be *simpler* because we have shed the bulky machinery of distances and open balls.
Since these open balls are absent, the definitions of some of these things may change fundamentally in important ways. 
However, it is always in a way that generalizes the previous definition -- the interior, closure, etc. of a set in a topological space will be the same as for the associated metric space when the topological space is metrizable.
It is a great exercise to attempt to prove equivalence wherever possible.

### Open sets and interiors

In a topological space $$(X,\tau)$$ (or $$X$$ for brevity), the open sets are determined explicitly by the topology $$\tau$$.
Neighborhoods are defined explicitly in terms of these also.

**Definition:** An **open neighborhood of a point** $$x\in X$$ is simply an open subset of $$X$$ containing the point $$x$$.

Note that unlike open balls, neighborhoods do not need to be centered at the point.  Indeed, things are general enough at this point that being centered there has lost its meaning.

**Definition:** The **interior** of a subset $$A$$ of $$X$$ is the union of all open subsets of $$X$$ containing $$A$$.

$$\text{int}(A) = \bigcup_{U\subseteq A,\ \text{open}} U.$$

In particular, this means that the interior of $$A$$ is the largest open subset of $$X$$ contained in $$A$$.  As a consequence, we know that $$A$$ is open if and only if $$\text{int}(A) = A$$.

The next theorem proves that $$\text{int}(A)$$ can also be characterized in terms of open neighborhoods, like in the case of metric spaces.

**Theorem:** The interior $$\text{int}(A)$$ is the set of all points $$x\in A$$ for which there exists an open neighborhood of $$x$$ contained in $$A$$, ie.

$$\text{int}(A) = \{x\in A:\ \exists U\in\tau\ \text{s.t.}\ U\subseteq A\}.$$


### Closed sets and closures

Closed sets are defined exactly as they are defined for metric spaces.

**Definition:** Let $$X$$ be a topological space.  A subset $$A$$ of $$X$$ is **closed** if $$A'$$ is open.

Just like before, the compatibility of taking unions or intersections with remaining closed mirrors that of being open via De Morgan's laws.

**Theorem:** An intersection of any number of closed sets is closed.  A finite union of closed sets is closed.

**Definition:** Let $$A$$ be a subset of a topological space $$X$$.  The **closure** of $$A$$ is the intersection of all closed subsets of $$X$$ containing $$A$$:

$$\overline{A} = \bigcap_{A\subseteq C \text{ (closed) }\subseteq X} C.$$

If $$C\subseteq X$$ is the closure of $$A$$, then we say that $$A$$ is **dense in** $$C$$.  When $$C=X$$, we simply say that $$A$$ is **dense**.

It's obvious from the definition that the closure $$\overline{A}$$ of $A$ is closed.
In fact $$\overline{A}$$ is characterized as being the *smallest* closed subset containing $$A$$.

Many properties that used to be awkward to prove in the case of metric spaces suddenly become trivial to prove under our upgraded definition.

**Theorem:**  Let $$A$$ be a subset of a topological space $$X$$.  Then $$A\subseteq \overline{A}$$ with equality if and only if $$A$$ is closed.

As a consequence, we can immediately see several properties of closures

**Corollary:**  Let $$A$$ and $$B$$ be subsets of a topological space $$X$$. Then
* (A) $$\overline{\varnothing} = \varnothing$$ and $$\overline{X} = X$$
* (B) $$\overline{A} = \overline{\overline{A}}$$
* (C) $$\overline{A\cup B} = \overline{A\cup B}$$

**Problem:**
We have shown that in a metric space, a singleton set $$\{x_0\}$$ is always closed.
Is the same true for any arbitrary topological space?

<details>
  <summary>Solution.</summary>
  No!  Consider for example the trivial topology.
</details>


### Limit points, isolated points, boundaries

As in the case of metric spaces, we can characterize being closed in terms of the *limit points*, which we must now define for general topological spaces.

**Definition:** Let $$A$$ be a subset of a topological space $$X$$.  An element $$x\in X$$ is a **limit point** of $$A$$ if every open neighborhood of $$x$$ contains a point of $$A$$ different from $$x$$.  The **derived set** $$D(A)$$ is the set of all limit points of $$A$$.

This is exactly the definition as in the case of metric spaces, except we are replacing open balls with arbitrary open sets!

As before, we characterize closed sets as those which contain all of their limit points and closures as the set along with its limit points.

**Theorem:** The closure $$\overline{A}$$ is the union of $$A$$ and all of its limit points:  $$\overline{A} = A\cup D(A)$$.

**Corollary:** A subset $$A\subseteq X$$ is closed if and only if every limit point of $$A$$ is contained in $$A$$; ie. if and only if $$D(A)\subseteq A$$.

In contrast to limit points, we have isolated points.  These two flavors of points make up *all* the points of a set.

**Definition:** A point $$x\in A$$ is an **isolated point** if there exists an open neighborhood of $$x$$ which contains no other point of $$A$$.

**Theorem:** A closed set $$A$$ is the disjoint union of its set of isolated points and limit points.

Just like for metric spaces, we can define the *boundary* of a set.  Intuitively, these are the points which lie on the "edge" of both $$A$$ and $$A'$$.

**Definition:** The **boundary** of a set $$A$$ is $$\partial A = \overline A\cap \overline{A'}$$.  A point $$x\in \partial A$$ is called a **boundary point** of $$A$$.

Any closed set is comprised of its interior points and its boundary points.

**Theorem:** Let $$A$$ be a closed subset of $$X$$.  Then $$A$$ contains $$\partial A$$ and is in fact equal to the disjoint union of $$\text{int}(A)$$ and $$\partial A$$.


