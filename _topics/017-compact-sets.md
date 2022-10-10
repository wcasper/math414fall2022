---
layout: page
title: Compact sets
---

**Additional reading:** Simmons 3.19

From our previous experience in calculus, a subset of $$\mathbb R^n$$ is called *compact* if it is both closed and bounded.
Compact sets play an important role, particularly in light of the **Extreme Value Theorem**, which says that a continuous function on a compact set has a global maximum and a global minimum.
Much of calculus is spent with how to find these extrema, using methods like finding critical points or using Lagrange multipliers.
In this section, we discuss compactness in the generality of topological spaces.

### Compact set
In a more general topological space, we don't have any notion of distance so this definition of compact needs to be replaced with a more general version.
Furthermore, even in the case of metric spaces, calling a set compact if it is closed and bounded is not the right definition anyway -- that would mess a lot of things up, such as making the real line with the discrete metric compact.
The following definition gives the right notion of compactness in a way that applies to all topological spaces simultaneously.

**Definition:**  A topological space $$X$$ is called **compact** if every open cover of $$X$$ has a finite subcover.  More generally a subset $$A\subseteq X$$ is compact if itis compact as a subspace.

Here it is important to remember what open sets in a subspace look like!

**Problem:** True or False.  Let $$X=\mathbb R$$ with the Euclidean topology and let $$Y=[0,1]$$ be a subspace of $$X$$.  The set $$[0,1)$$ is an open subset of $$Y$$.
<details>
  <summary>Solution.</summary>
  True!  The open subsets of $$Y$$ are intersections of open subsets of $$X$$ with $$Y$$.  So for example $$[0,1) = (-3,1)\cap Y$$ is open.
</details>

**Example:** Let $$X$$ be any set with the trivial topology.  Then $$X$$ is compact.

**Example:** Let $$X$$ be any set with the discrete topology.  Then $$X$$ is compact if and only if $$X$$ is finite.

**Example:** Let $$X = \mathbb R$$ with the Euclidean topology.  Then $$X$$ is not compact.

**Example:** Let $$X = [0,1]$$ be a subspace of $$\mathbb R$$ with the Euclidean topology.  Then $$X$$ is compact.

**Example:** Let $$X = (0,1)$$ be a subspace of $$\mathbb R$$ with the Euclidean topology.  Then $$X$$ is not compact.

**Example:** Let $$X$$ be a finite set with any topology.  Then $$X$$ is compact.

Starting out with a compact space, we can make a great many more just by taking closed subsets.

**Theorem:** Suppose that $$X$$ is a compact topological space.  Then any closed subset of $$X$$ is also compact.
**Proof:**  Suppose that $$X$$ is compact and that $$A\subseteq X$$ is closed.  Let $$\{U_i: i\in I\}$$ be an open cover of the topological space $$A$$.  Then by definition of the relative topology, each $$U_i$$ is of the form $$U_i = V_i\cap A$$ for some open subset $$V_i$$ of $$X$$.  This means that $$\{V_i: i\in I\}\cup\{A'\}$$ is an open cover of $$X$$, and therefore has a finite subcover $$\{V_j: j\in J\}\cup\{A'\}$$ for some subset $$J\subseteq I$$ with $$|J|$$ finite.  It follows that $$\{U_j:j\in J\}$$ is a finite subcover of $$A$$.

One of the principal applications of compact sets is the Extreme Value Theorem that says that a continuous function on a compact set has an absolute max and an absolute min.
This is beautifully captured in the property that the continuous image of a compact set is compact.

**Theorem:** Let $$X$$ and $$Y$$ be topological spaces and suppose that $$X$$ is compact.  If $$f: X\rightarrow Y$$ is a continuous function, then the image $$f(X)$$ is compact.
**Proof:**
Suppose that $$\{V_i:i\in I\}$$ is an open cover of $$f(X)$$.
Then $$\{f^{-1}(V_i): i\in I\}$$ is an open cover of $$X$$ and has a finite subcover $$\{f^{-1}(V_j): j\in J\}$$.
It follows that $$\{V_j: j\in J\}$$ is a finite subcover of $$f(X)$$.

### Compact vs closed and bounded

The original definition of compact we learn in calculus is *closed and bounded*.  However, such a definition does not really make sense for arbitrary metric spaces, let alone arbitrary topological spaces where "bounded" has lost all meaning.

**Example:** Let $$X = \{1,2\}$$ with the trivial topology.  Then every subset of $$X$$ is finite and therefore compact.  However, $$\{1\}$$ is not closed.

The fact that compact = closed and bounded in Euclidean space is an important result in real analysis called the **Heine-Borel Theorem**.  We will prove the Heine-Borel theorem below for $$\mathbb R$$, but for starters, we can prove a partial result in this direction by showing that compact subsets of a metric space are necessarily closed.

**Theorem:** Let $$C$$ be a compact subset of a metric space $$X$$.  Then $$C$$ is closed.
**Proof:** Suppose that $$x_0\in C$$ is an accumulation point of $$C$$ which is not in $$C$$.  Consider the open cover of $$X$$ consisting of $$U_n = \{x_0\in C: d(x_0,x) > 1/n\}.$$
Then since $$C$$ is compact, there is a finite subcover $$\{U_{n_k}: k = 1,2,\dots m\}$$ with $$n_1 < n_2 < \dots < n_m$$.  It follows that $$C = U_{n_m}$$ and therefore every element of $$C$$ is distance at least $$1/n_m$$ away from $$x_0$$.  Therefore $$B_{1/n_m}(x_0)\cap C = \varnothing$$, which is a contradiction.


### Finite intersection property

An alternative characterization of compactness can be given using collections of closed sets with the finite intersection property.

**Definition:** A collection of $$\mathcal C$$ of sets has the **finite intersection property** if every finite subcollection of $$\mathcal C$$ has nonempty intersection.

**Example:** Let $$\mathcal C = \{C_n: n\in\mathbb N\}$$ with $$C_n = \{k\in\mathbb Z: k\geq n\}$$.  The collection $$\mathcal C$$ has the finite intersection property, thought the infinite intersection $$\bigcap_{n\in\mathbb N} C_n = \varnothing.$$

**Theorem:** Let $$X$$ be a topological space.  The following are equivalent

* $$X$$ is compact;
* Every collection $$\mathcal C$$ of closed sets with empty intersection has a finite subcollection with empty intersection;
* Every collection $$\mathcal C$$ of closed sets with the finite intersection property actually has nonempty intersection.


**Example:** Consider $$\mathbb{R}$$ with the Euclidean topology.  The collection of closed sets $$\mathcal C = \{(-\infty,-n]: n\geq 0\}$$ has the finite intersection property, but the intersection of all the sets in $$\mathcal C$$ is empty.  This shows $$\mathbb{R}$$ is not compact.


### Checking with bases and subbases

To check compactness, it suffices to restrict our attention to the sets of a base or subbase.

**Definition:** Let $$\beta$$ and $$\gamma$$ be a base and subbase for a topology $$\tau$$ on $$X$$, respectively.  An element $$U\in\beta$$ is called a **basic open set**.  Likewise, an element $$U\in\gamma$$ is called a **subbasic** open set.  An open cover consisting of basic or subbasic open sets is referred to as a **basic open cover** or a **subbasic open cover**.

**Alexander's Subbase Theorem:** Let $$\gamma$$ be a subbase for a topology $$\tau$$ on $$X$$.  Then $$X$$ is compact if and only if every subbasic open cover has a finite subcover.

Note that since every base is also a subbase, this also implies the same theorem, but with base replaced with subbase.

**Proof:**  One direction is clear, but the other is fairly complicated and requires the *Axiom of Choice* (ie. Zorn's lemma), which annoys some math folks.


As a consequence, we have an easy and low-tech proof the Heine-Borel theorem.

**Heine-Borel Theorem:** A subset of $$\mathbb R$$ is compact if and only if it is both closed and bounded.
**Proof:** Suppose that $$C\subseteq \mathbb R$$ is compact.  For each $$x\in C$$, let $$U_x = (x-1,x+1)\cap C$$.  Then $$\{U_x\}$$ is an open cover of $$C$$ and contains a finite subcover $$\{U_{x_i}: i=1,\dots, n\}$$, which is obviously bounded.  Since compact subsets of a metric space are closed, $$C$$ is also closed.

Conversely, suppose that $$C$$ is a closed and bounded subset of a compact metric space.  Then $$C$$ is a closed subspace of a closed interval $$[a,b]$$.  Since closed subspaces of compact spaces are compact, it suffices to show that $$[a,b]$$ is compact for all real numbers $$a,b$$ with $$a < b$$.
Consider the open subbase of $$[a,b]$$ consisting of sets of the form $$\{[a,x): a < x < b\}\cup \{(x,b]: a < x < b\}.$$
By Alexander's Subbase Theorem, it suffices to prove that any open subbase cover of $$[a,b]$$ has a finite subcover.

Assume that $$\mathcal U$$ is an open subbase cover of $$[a,b]$$.  Then $$(x,b]\in \mathcal U$$ for some $$a < x < b$$.  Let $$x_0 = \inf \{x: (x,b]\in \mathcal U\}.$$
Then $$x_0\in [a,b]$$ and therefore there exists $$a< x_0 < x_1 < b$$ with $$[a,x_1)\in \mathcal U$$.  It follows that $$\{[a,x_1), (x_0,b]\}$$ is a subcover of $$\mathcal U$$.



