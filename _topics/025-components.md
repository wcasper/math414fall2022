---
layout: page
title: Connected Components
---

**Additional reading:** Simmons 6.32

In this section, we show that a topological space $$X$$ can be partitioned into a collection of connected topological spaces called its components.


### Components

**Definition:** A **connected component**, or just **component**, $$U$$ of $$X$$ is a connected subspace of $$X$$ which is not contained in any other connected subset of $$X$$.

In other words, a connected component is a maximally connected subset of $$X$$.
Whenever we run into a definition like this, where we are finding a maximal element of a poset, we should justify its existence.  Typically, this means applying Zorn's Lemma, though in this case we can get away without it.  To aid us in our cause, we first observe the following lemma.

**Lemma:** Let $$X$$ be a topological space and suppose $$\{A_i: i\in I\}$$ is a collection of connected subsets of $$X$$.  If $$\bigcap_{i\in I}A_i$$ is non-empty, then $$\bigcup_{i\in I} A_i$$ is also connected.

With this in mind, we have the following theorem about the existence of connected components.

**Theorem:** Let $$A$$ be a connected subset of $$X$$.  Then there exists a unique connected component of $$X$$ containing $$A$$.  

**Proof:** Let $$P$$ be the poset of all connected subsets of $$X$$ containing $$A$$.
Then by the previous lemma $$C = \bigcup_{B\in P} B$$ is a connected subset of $$X$$.
Since $$C$$ contains $$A$$, we have $$C\subseteq P$$ and clearly $$C$$ is a maximal element of $$A$$.  In fact, it's clear that $$C$$ is the supremum of $$P$$ so $$C$$ is unique.

In particular, topological spaces always have connected components.
Topologically, components of a topological space are always closed.

**Theorem:** If $$C\subseteq X$$ is a component, then it is closed.

**Proof:** Suppose that $$C$$ is a connected component.  Then $$\overline C$$ is connected so by maximality $$C = \overline C$$.

**Theorem:** Let $$\{U_i: i\in I\}$$ be the collection of all components of $$X$$.  Then this collection is a partition of $$X$$.

**Proof:** For each $$x\in X$$, let $$C_x$$ be the connected component of $$X$$ containing $$X$$.  Then if $$C_x\cap C_y\neq\varnothing$$, the previous lemma implies that $$C_x\cup C_y$$ is connected.  By maximality, it follows that $$C_x = C_x\cup C_y= C_y$$.  Hence the collection of distinct components form a partition of $$X$$.

Sometimes connected components are characterized by the idea that they are both open and closed.

**Theorem:** Suppose that $$X$$ is a topological spacee with finitely many connected components.  Then a subset $$A\subseteq X$$ is a union of finitely many connected components of $$X$$ if and only if it is both open and closed.
In particular, the only connected subsets which are both open and closed are the connected components.

**Proof:** Suppose that $$C_1,\dots,C_r$$ are the connected components of $$X$$.
Then $$C_j$$ is closed for all $$j$$, and so the complement $$C_j' = \bigcup_{i\neq j} C_i$$ is a finite union of closed sets, and is therefore closed.  Hence $$C_j$$ is also open.

Conversely, suppose that $$A\subseteq X$$ is both open and closed.  Then $$A\cap C_j$$ and $$A'\cap C_j$$ are both open subsets of $$C_j$$ in the relative topology whose union is $$C_j$$.  Since $$C_j$$ is connected, we realize that either $$C_j\subseteq A$$ or $$A\cap C_j=\varnothing$$ for all $$j$$.  It follows that $$A$$ is the union of some collection of connected components of $$X$$.

**Remark:** A topological space with finitely many connected components is sometimes called a **Noetherian topological space**.

**Example:** Let $$\mathbb Q$$ be the rational numbers with the subspace topology of $$\mathbb R$$.  A subspace of $$\mathbb R$$ is connected if and only if it is an interval, so the only connected subsets of $$\mathbb Q$$ are singletons.  Thus the connected components of $$\mathbb Q$$ are singletons.  However, these singletons are not open.



