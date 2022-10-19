---
layout: page
title: Compact Metric Spaces
---

**Additional reading:** Simmons 4.24

Earlier on, we proved that for a metric space $$X$$, a subset $$A\subseteq X$$ being compact implies that $$A$$ is closed and bounded
However, we know that the converse is not true, even if it happens to be true for $$\mathbb R^n$$ with the Euclidean topology by the Heine-Borel Theorem.
In this section, we explore several other conditions on a metric space which *do* turn out to be equivalent to compactness.

### Bolzano-Weierstrass

In our study of $$\mathbb R$$ in real analysis, one of the powerful theorems that we learn is the Bolzano-Weierstrass Theorem, a fundamental observation about the behavior of convergence of real sequences.

**Bolzano-Weierstrass Theorem (version 1):** Let $$\{x_n\}$$ be a bounded sequence of real numbers.  Then $$\{x_n\}$$ has a convergent subsequence $$\{x_{n_k}\}.$$

Equivalently, the Bolzano-Weierstrass Theorem is sometimes restated as

**Bolzano-Weierstrass Theorem (version 2):** If $$A\subseteq\mathbb R$$ is a bounded, infinite subset of $$\mathbb R$$, then $$A$$ has a limit point.

Both of these properties have natural analogs in more general metric spaces.

**Definition:** A metric space $$X$$ has the **Bolzano-Weierstrass property** if every infinite subset has a limit point.  It is called **sequentially compact** if every sequence of elements in $$X$$ has a convergent subsequence.

It is easy to prove that these two definitions are equivalent.

**Theorem:** A metric space $$X$$ has the Bolzano-Weierstrass property if and only if $$X$$ is sequentially compact.

Moreover, we can reinterpret the Bolzano-Weierstrass Theorem as saying that closed and bounded subsets of $$\mathbb R$$ have the Bolzano-Weierstrass property, or equivalently are sequentially compact.
We also know that closed and bounded subsets of $$\mathbb R$$ are compact.
It turns out that for **all** metric spaces, being compact, being sequentially compact, or having the Bolzano-Weierstrass property are all equivalent.

To prove this, we first consider an interesting property of open coverings called a **Lebesgue number**.

**Definition:** Let $$\{U_i\}$$ be an open cover of a metric space $$X$$.  A **Lebesgue number** of $$\{U_i\}$$ is a number $$a>0$$ satisfying the following property
* if $$A\subseteq X$$ is a subset with diameter less than $$a$$, then $$A\subseteq U_j$$ for some $$j$$

**Example:** Consider the open cover $$\{(n,n+2): n\in\mathbb Z\}$$ of $$\mathbb R$$.  Suppose that $$A\subseteq \mathbb R$$ has diameter less than $$1$$, and $$a\in A$$.  Then there exists an integer $$n>0$$ such that $$n < a < n+2$$.
From the diameter of $$A$$, we know that either $$A$$ is contained in $$(n,n+2)$$ or in $$(n-1,n+1)$$ or in $$(n+1,n+3)$$.
Thus a Lebesgue number for this open cover is $$1$$.

Not every open cover has to have a Lebesgue number.

**Example:** Consider the set of intervals $$\{(x/2,x): 0 < x < 1\}$$ of $$(0,1)$$.  This collection covers $$(0,1)$$, but for all $$\epsilon > 0$$ the set $$(0,\epsilon)$$ is not contained in any elements of the open cover.  Therefore the open cover has no Lebesgue number.

The following Lemma tells us that for sequentially compact spaces, every open cover must have a Lebesgue number.

**Lebesgue's Covering Lemma:**  Let $$X$$ be a sequentially compact space.  Then every open cover of $$X$$ has a Lebesgue number.

**Proof:** Suppose that $$\{U_i:i\in I\}$$ is an open cover with no Lebesgue number.  Then for all $$n>0$$ there must exist a set $$A_n$$ whose diameter is less than $$1/n$$ and which is not contained in $$U_j$$ for any $$j\in I$$.
For each $$n$$, choose $$x_n\in A_n$$.
Since $$X$$ is sequentially compact, we can choose a subsequence $$\{x_{n_k}\}$$ of $$\{x_n\}$$ converging to $$x\in X$$.
Furthermore, since $$\{U_i\}$$ cover $$X$$, there exists $$j\in I$$ such that $$x\in U_j$$ and therefore there is a radius $$r>0$$ with $$B_r(x)\subseteq U_j$$.
By definition , for all $$\epsilon > 0$$ there exists $$N>0$$ such that $$k\geq N$$ implies $$d(x_{n_k},x) < \epsilon$$.
Take $$\epsilon = r/2$$ and choose $$k$$ such that $$k\geq N$$ and $$n_k> 2/r$$.
Then for all $$y\in A_k$$, the triangle inequality tells us

$$d(x,y) \leq d(x,x_{n_k}) + d(x_{n_k},y) < r/2 + \text{diam}(A_{n_k}) < r.$$

Thus $$A_k\subseteq B_r(x)\subseteq U_j$$, which is a contradiction.  Hence our assumption that there is no Lebesgue number must be false.
This completes the proof.

One interesting corollary is that continiuous functions on sequentially compact metric spaces must be uniformly continuous.

**Theorem:** Let $$f: X\rightarrow Y$$ be a continuous function between metric spaces with $$X$$ sequentially compact.  Then $$X$$ is uniformly continuous.

**Proof:** We need to show that for all $$\epsilon > 0$$ there exists $$\delta>0$$ such that $$d_X(x_1,x_2) < \delta$$ implies $$d_Y(f(x_1),f(x_2))<\epsilon$$.
for all $$x_1,x_2\in X$$.
Let $$\epsilon > 0$$ and consider the open cover $$\{B_{\epsilon/2}(y): y\in Y\}$$ of $$Y$$.
Since $$f$$ is continuous, $$\{f^{-1}(B_{\epsilon/2}(y)): y\in Y\}$$ is an open cover of $$X$$ and by Lebegue's Covering Lemma, it has a Lebesgue number $$a$$.  Choose $$\delta = a/2$$.  Then if $$d(x_1,x_2)<\delta$$, we have $$x_1\in B_\delta(x_2)$$ and $$B_\delta(x_2)\in f^{-1}(B_{\epsilon/2}(y))$$ for some $$y\in Y$$.  Therefore $$x_1,x_2\in f^{-1}(B_{\epsilon/2}(y))$$, making $$f(x_1),f(x_2)\in B_{\epsilon/2}(y)$$.  By the triangle inequality,
$$d(f(x_1),f(x_2)) \leq d(f(x_1),y) + d(y,f(x_2)) < \epsilon.$$
This completes the proof.


Sequentially compact metric spaces also have the property that they are totally bounded.

**Definition:** A metric space $$X$$ is **totally bounded**, if for all $$\epsilon>0$$ there exists a *finite* subset $$A\subseteq X$$ with $$X = \bigcup_{a\in A} B_\epsilon(a).$$

**Theorem:** If $$X$$ is sequentially compact, then it is totally bounded.

**Proof:** Suppose that $$X$$ is sequentially compact.  Let $$\epsilon > 0$$.  Choose a sequence of values $$\{x_n\}$$ in $$X$$ recursively by first picking $$x_1$$ to be anything and then choosing $$x_{n+1}$$ to be in $$X\backslash \bigcup_{k=1}^n B_\epsilon(x_n)$$, assuming the latter set is non-empty.  If this sequence is infinite, then it must converge, but every point is $$\epsilon$$ away from every other.  This is a contradiction, so the sequence we defined must be finite.  Taking $$A = \{x_n\}$$, we have $$X = \bigcup_{a\in A} B_\epsilon(a)$$.  This completes the proof.

Using Lebesgue's Covering Lemma and the notion of being totally bounded, we can prove that sequentially compact, having the Bolzano-Weierstrass property, and compactness are all the same thing for metric spaces.

**Theorem:**  Let $$X$$ be a metric space.  Then the following are equivalent.
* (A) $$X$$ has the Bolzano-Weierstrass property;
* (B) $$X$$ is sequentially compact;
* (C) $$X$$ is compact.

**Proof:**
We will prove this round-robin style.
(A) implies (B) is obvious.
Now suppose (B) and let $$\{U_i: i\in I\}$$ be an open cover of $$X$$.  Then this cover has a Lebesgue number $$a$$.  Moreover $$X$$ is totally bounded, so for fixed $$0 < \epsilon < a/2$$, there exists a finite collection of points $$A=\{x_1,\dots,x_n\}$$ such that $$X= \bigcup_{i=1}^n B_{\epsilon}(x_i)$$.  The diameter of $$B_\epsilon(x_i)$$ is $$\leq 2\epsilon < a$$, so $$B_{\epsilon}(x_i)\in U_{m_i}$$ for some $$m_i\in I$$.  It follows that $$\{U_{m_i}: i=1,\dots n\}$$ is a finite subcover.  Thus $$X$$ is compact, proving (C).
Finally, assume (C) and let $$A$$ be an infinite subset of $$X$$.  Assume $$A$$ has no limit points.  Then $$A$$ is closed and is a subset of a compact set and thus $$A$$ is compact.
Furthermore, every point of $$A$$ is an isolated point, meaning for all $$x\in A$$ there exists $$\epsilon>0$$ such that $$B_{\epsilon}(x)\cap A = \{x\}$$ making $$\{x\}$$ open in the subspace topology.  It follows that $$\{\{x\}: x\in A\}$$ is an open cover of $$A$$ (in the subspace topology) which is infinite and has no subcovers.  This contradicts the fact that $$A$$ is compact.  Hence (A) must have the Bolzano-Weierstrass property.




