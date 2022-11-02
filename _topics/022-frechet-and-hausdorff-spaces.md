---
layout: page
title: Frechet and Hausdorff Spaces
---

**Additional reading:** Simmons 5.26 and 5.27

The most important separation axioms starting out $$T_1$$ or **Frechet** and $$T_2$$ or **Hausdorff**.

## Frechet space

**Theorem:** Let $$X$$ be $$T_1$$.  Then any singleton set in $$X$$ is closed.  Conversely, if $$X$$ is a topological space where every singleton set is closed, then $$X$$ is $$T_1$$.

**Proof:**  Let $$x\in X$$.  For any $$y\in X$$, let $$U_y$$ be an open set containing $$y$$ but not containing $$x$$.  Then $$\{x\} = \bigcap_{y\neq x} U_y'$$ is the intersection of a collection of closed sets and is therefore closed.

We might hope to find all kinds of examples satisfying certain separation axioms but not others using finite topological spaces, but the following corollary shows that this is to be only a dream.

**Corollary:**  Suppose that $$X$$ is a finite set which is $$T_1$$.  Then $$X$$ has the discrete topology.

**Proof:**  Each singleton is closed.  Since finite unions of closed sets are closed, this means that every finite subset of $$X$$ is closed.  Hence every subset of $$X$$ is closed.  This forces every subset of $$X$$ to be open, so $$X$$ has the discrete topology.

## Hausdorff space

**Theorem:** The product of any collection of Hausdorff spaces is Hausdorff.

**Proof:**  Let $$\{X_i: i\in I\}$$ be a collection of Hausdorff spaces and consider $$\prod_{i\in I} X_i$$.  Suppose that $$(x_i: i\in I)$$ and $$(y_i: i\in I)$$ are two *different* points in $$\prod_{i\in I} X_i$$.  Then there exists $$j\in I$$ with $$x_j\neq y_j$$.  Since $$X_j$$ is Hausdorff, there exists $$U,V\subseteq X_j$$ with $$U\cap V= \varnothing$$ and $$x_j\in U$$ and $$y_j\in V$$.  It follows that $$\pi_j^{-1}(U)$$ and $$\pi_j^{-1}(V)$$ are disjoint open neighborhoods of $$(x_i)$$ and $$(y_i)$$, respectively.

The property of being $$T_2$$ is almost as strong as $$T_3$$ in the sense that any point and any *compact* subset $$C$$ of $$X$$ not containing our point have disjoint open neighborhoods.

**Theorem:** Let $$X$$ be a Hausdorff space, $$x\in X$$ and let $$C$$ be a compact subset of $$X$$ not containing $$X$$.  Then $$x$$ and $$C$$ have disjoint open neighborhoods.

**Proof:**
For each $$y\in C$$, let $$U_y$$ and $$V_y$$ be a disjoint open neighborhoods of $$x$$ and $$y$$, respectively.  Then $$\{V_y\cap C: y\in C\}$$ is an open cover of $$C$$ and has a finite subcover $$\{V_{y_i}\cap C: i=1,\dots, n\}.$$
Let $$U = \bigcap_{i=1}^n U_{y_i}$$ and $$V = \bigcup_{i=1}^n V_{y_i}$$.  Then $$U$$ and $$V$$ are open neighborhoods of $$x$$ and $$C$$, respectively, and $$U\cap V = \varnothing$$ by definition.


One consequence of this theorem is that every compact subset of a Hausdorff space is closed.

**Theorem:** Let $$C\subseteq X$$ be compact.  Then $$C$$ is closed.

**Proof:** Suppose that $$C\subseteq X$$ is compact.  Then for every $$x\in X$$ not in $$C$$, there exists an open neighborhood $$U_x$$ of $$x$$.  It follows that $$C = \bigcap_{x\notin C} U_x'$$ is the intersection of a collection of closed sets, and is therefore closed.

A further consequence of this theorem is that bijective, continuous mappings from compact spaces to Hausdorff spaces are Homeomorphisms.

**Theorem:** Let $$X$$ be compact and $$Y$$ be Hausdorff, and suppose that $$f: X\rightarrow Y$$ is a continuous bijection.  Then $$f$$ is a homeomorphism.

**Proof:**To prove that $$f$$ is a homeomorphism, we must show that $$f(U)$$ is open for all open subsets $$U\subseteq X$$.  If $$C\subseteq X$$ is closed, then it is compact.  The continuous image of a compact set is compact, so $$f(C)$$ is also compact.  By the previous theorem, it is closed.  Hence $$f(U')$$ is closed for all open $$U$$, and it follows that $$f(U) = f(U')'$$ is open for all open sets $$U\subseteq X$$.
