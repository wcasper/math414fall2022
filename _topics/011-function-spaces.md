---
layout: page
title: Function Spaces
---

**Additional reading:** Simmons 2.14

### Function spaces

Given two metric spaces $$X$$ and $$Y$$, it is natural to consider the set of all continuous functions from $$X$$ to $$Y$$.
So far, we have begun a study of *metric spaces*, so to better understand the set of continuous functions, we are motivated to endow it too with the structure of a metric space.
Given continuous functions $$f,g: X\rightarrow Y$$, we can intuitively define the distance between them by

$$d(f,g) = \sup_{x\in X} d(f(x),g(x)).$$

However, there is a problem with this.  This function may not be well-defined!  The "distance" between two functions could potentially be infinite.
To fix this, we consider the set of *bounded* continuous functions.

**Definition:** Let $$X$$ be a metric space.  A subset $$A\subseteq X$$ is called **bounded** if there exists a constant $$k>0$$ such that

$$d(x,y)\leq k\ \forall x,y\in A.$$

**Definition:** Let $$X$$ and $$Y$$ be metric spaces.  A function $$f: X\rightarrow Y$$ is called **bounded** if $$f(X)$$ is a bounded subset of $$Y$$.

Armed with this definition, we consider the sets

$$\mathcal B(X,Y) = \{f: X\rightarrow Y |\ \text{$f$ is a bounded function}\}.$$

$$\mathcal C(X,Y) = \{f: X\rightarrow Y |\ \text{$f$ is a bounded continuous function}\}.$$

**Theorem:** The function $$d: V\times V\rightarrow\mathbb R$$ defined by

$$d(f,g) = \sup_{x\in X} d(f(x),g(x))$$

is a metric on $$V$$ for $$V = \mathcal B(X,\mathbb R)$$, $$V=\mathcal B(X,\mathbb C)$$, $$V = \mathcal C(X,\mathbb R)$$, and $$V=\mathcal C(X,\mathbb C)$$.

The above metric is called the **uniform metric**.

Two very important special cases are
* the space $$C(X,\mathbb R)$$ of bounded, continuous real-valued functions on $$X$$;
* the space $$C(X,\mathbb C)$$ of bounded, continuous complex-valued functions on $$X$$.

Note: here the metric defined on $$\mathbb R$$ or $$\mathbb C$$ is defined by $$d(z,w) = \lvert z-w\rvert $$.
Here, we can characterize bounded more simply, in a very intuitive fashion.

**Lemma:** A function $$f: X\rightarrow\mathbb R$$ is bounded if and only if there exists $$k>0$$ such that $$\lvert f(x)\rvert \leq k$$ for all $$x\in X$$.

Both the spaces $$C(X,\mathbb R)$$ and $$C(X,\mathbb C)$$ are *vector spaces*.
Furthermore, the vector spaces have a notion of the *length* of a vector in a way which defines the metric.
Vector spaces with way to define lengths of vectors are called *normed linear spaces*.

**Definition:** A (real or complex) **normed linear space** is a (real or complex) vector space $$V$$ endowed with a real-valued function $$\lVert\cdot\rVert: X\rightarrow\mathbb R$$ satisfying the following properties
* $$\lVert x\rVert \geq 0$$ and $$\lVert x\rVert = 0\Leftrightarrow x = 0$$
* $$\lVert x + y rVert \leq \lVert x\rVert + \lVert y\rVert$$
* $$\lVert \alpha x rVert\leq |\alpha|\ \lVert x rVert$$

**Theorem:** The sets $$\mathcal C(X,\mathbb R)$$ and $$\mathcal C(X,\mathbb C)$$ are both normed vector spaces with norm defined by

$$\lVert f\rVert = \sup_{x\in X} |f(x)|.$$

As we see, the metric on $$\mathcal C(X,\mathbb R)$$ is defined in terms of the norm by $$d(f,g) = \lVert f-g\rVert$$.
In general, a normed vector space always inherets the structure of a metric space in this way.

**Theorem:** Let $$V$$ be a normed vector space.  Then $$d(x,y) = \lVert x-y\rVert$$ defines a metric on $$V$$.

### Convergence

As in any metric space, we can talk about convergence of sequences.  However, for function spaces, we are really talking about convergence of sequences of functions!
Whenever we see a statement about convergence of functions like $$f_n\rightarrow f$$, we should ask *in what sense*?
Such a question gets to the heart of many questions in analysis and there are many important possible answers, such as: pointwise convergence, uniform convergence, $$L^p$$-norm convergence, weak convergence, and convergence in measure.  Many of these concepts however, can be encoded in terms of a choice of normed vector space.

The simplest form of convergence of functions is pointwise convergence.

**Definition:** We say that a sequence of real-valued functions $$\{f_n\}$$ on a metric space $$X$$ converges **poinwise** to a function $$f: X\rightarrow R$$ if $$f_n(x)\rightarrow f(x)$$.  Equivalently, this says that for all $$\epsilon>0$$ and for all $$x\in X$$ there exists $$N\geq 0$$ such that $$n\geq N$$ implies $$\lvert f_n(x)-f(x)\rvert <\epsilon$$.

However, pointwise convergence tends to not be strong enough to guarantee to preserve any nice properties the original sequence of functions might have had.
Instead, it is often necessary to consider stronger versions, such as uniform convergence.

**Definition:** We say that a sequence of bounded, real-valued functions $$\{f_n\}$$ on a metric space $$X$$ converges **uniformly** to a function $$f: X\rightarrow R$$ if for all $$\epsilon>0$$ there exists $$N>0$$ such that $$n\geq N$$ implies $$\lvert f_n(x)-f(x)\rvert <\epsilon$$ for all $$x\in X$$.

This second form says a lot more about the sequence, since it says we can choose an integer $$N$$ which works for all $$x\in X$$ simultaneously.
For pointwise convergence, the value of $$N$$ can depend on both $$\epsilon$$ and the point $$x$$.
In particular, we have the following obvious result.

**Proposition:** If $$\{f_n\}$$ converges uniformly to $$f$$ then it also converges pointwise to $$f$$.

Naturally, one may ask whether a particular normed vector space is complete.

**Definition:** A normed linear space which is complete as a metric space is called a **Banach space**.

**Theorem:** Both $$\mathcal B(X,\mathbb R)$$ and $$\mathcal B(X,\mathbb C)$$ are Banach spaces.

**Theorem:** Both $$\mathcal C(X,\mathbb R)$$ and $$\mathcal C(X,\mathbb C)$$ are closed subspaces of $$\mathcal B(X,\mathbb R)$$ and $$\mathcall B(X,\mathbb C)$$, and are therefore Banach spaces.

In particular, this implies the following corollary.

**Corollary:** The uniform limit of bounded, continuous functions is also a bounded, continuous function.

**Question:** Is the following sequence of functions in $$\mathcal C(X,\mathbb R)$$ a Cauchy sequence?

$$f_n(x) = \left\lbrace\begin{array}{cc}1-n|x|, & |x|\leq 1/n\\0,& |x|> 1/n\end{array}\right.$$

<details>
  <summary>Solution.</summary>
  No.  If it was, it would converge to a continuous function.  However it converges pointwise to a discontinuous one.
</details>






