---
layout: page
title: Homework 2
permalink: /homework/hw2
---

### Directions
Solve the following problems and type up your solutions.  Your solutions should be provided in one of the following formats (in order of preference)
* typed up in $$\LaTeX$$ and submitted as a PDF on Canvas
* written legibly on blank paper, scanned into a PDF and then uploaded on Canvas
* written on ancient parchement with a quill and then flown to the instructor via owl post like in Harry Potter

If you go with the first strategy, you may wish to check out Overleaf which is a free and intuitive website for generating $$\LaTeX$$ documents online.
If you wish to use the second method and don't own a scanner at home, you can check out the numerous scanning apps available for smartphones.

**Problem 1:** 

Let $$X$$ be a set and let $$\mathcal P(X)$$ be the power set of $$X$$.
Complete the following argument to prove that the cardinality of $$X$$ is strictly smaller than the cardinality of $$\mathcal P(X)$$.

* (a) Give an example of an injective function $$f: X\rightarrow\mathcal P(X)$$, so that the cardinality of $$X$$ is less than or equal to the cardinality of $$\mathcal P(X)$$.
* (b) To prove that the cardinalities are not equal, we must prove that there cannot be a bijection.  We will use proof by contradiction.  Suppose that $$f: X\rightarrow \mathcal P(X)$$ is a bijection.  Define a subset $$A\subseteq X$$ by

$$A = \{x\in X: x\notin f(x)\}.$$

Prove that $$A$$ cannot be in the image of $$f$$ and therefore $$f$$ is not a bijection.  Note that this can be viewed as an abstract version of Cantor's diagonalization argument.
* (c) As an application of this result, prove that the set of functions from $$\mathbb N$$ to $$\{0,1\}$$ is uncountable.

**Problem 2:**  

Let $$X$$ be a non-empty set and suppose that $$d: X\times X\rightarrow \mathbb R$$ is a function satisfying the two conditions

* (non-degeneracy) $$d(x,y) = 0\Leftrightarrow x = y$$ for all $$x,y\in X$$
* (triangle inequality) $$d(x,y) \leq d(x,z) + d(y,z)$$ for all $$x,y,z\in X$$

Show that $$d$$ automatically satisfies *positivity* and *symmetry* and thus must be a metric on $$X$$.

**Problem 3:** Let $$(X,d)$$ be a metric space and suppose that $$x\in X$$.  Show that the complement of the singleton set $$\{x\}$$ must be an open set.

**Problem 4:** Give examples to show that the union of infinitely many closed sets may not be closed and that the intersection of infinitely many open sets may not be open.

**Problem 5:** Determine with proof the interior and the boundary of the Cantor set.

