---
layout: page
title: Euclidean space
---

**Additional reading:** Simmons 2.15

### Euclidean space

We have said previously that $$\mathbb R^n$$ is a metric space when endowed with the metric obtained from the distance formula.
However, we never verified that this metric satisifes the required axioms, in particular the triangle inequality.
In this section, we will do so.  In fact, we will show that $$\mathbb R^n$$ is a Banach space!


Our first step is to more thoroughly explore the **Euclidean norm**

$$\lVert x \rVert = \sqrt{x_1^2 + x_2^2 + \dots + x_n^2},\quad x = (x_1,x_2,\dots, x_n).$$

**Lemma (Cauchy-Schwartz Inequality):** If $$x,y\in \mathbb R^n$$ then

$$\sum_{i=1}^n |x_iy_i|\leq \left(\sum_{i=1}^n x_i^2\right)^{1/2}\left(\sum_{i=1}^n y_i^2\right)^{1/2}.$$

**Proof:**  Suppose that $$a,b$$ are positive real numbers.  Obviously $$(a-b)^2\geq 0$$, and therefore $$a^2 + b^2 \geq 2ab$$.  Equivalently, we have the following simple case of the well-known **AM-GM inequality**: $$ab\leq \frac{1}{2}(a^2+b^2).$$  Therefore for all $$1\leq i\leq n$$

$$\frac{|x_i|}{\lVert x\rVert}\frac{|y_i|}{\lVert y\rVert} \leq \frac{1}{2}\left(\frac{|x_i|^2}{\lVert x\rVert^2} + \frac{|y_i|^2}{\lVert y\rVert^2}\right).$$


Summing both sides with respect to $$i$$, we get

$$\frac{1}{\lVert x\rVert\ \lVert y\rVert}\sum_{i=1}^n|x_iy_i| \leq \frac{1}{2}\left(\sum_{i=1}^n\frac{|x_i|^2}{\lVert x\rVert^2} + \sum_{i=1}^n\frac{|y_i|^2}{\lVert y\rVert^2}\right) = 1.$$

This completes the proof.

As a consequence of this, we can prove the triangle inequality for the Euclidean norm.

**Lemma (Minkowski Inequality):**  Let $$x,y\in\mathbb R^n$$.  Then

$$\left(\sum_{i=1}^n (x_i+y_i)^2\right)^{1/2}\leq \left(\sum_{i=1}^n x_i^2\right)^{1/2} + \left(\sum_{i=1}^n y_i^2\right)^{1/2}.$$

**Proof:**

$$\begin{align}
\sum_{i=1}^n (x_i+y_i)^2
&\leq \sum_{i=1}^n |x_i+y_i|(|x_i|+|y_i|)\\
&= \sum_{i=1}^n |x_i+y_i|\ |x_i| + \sum_{i=1}^n|x_i+y_i|\ |y_i|\\
&\leq \lVert x+y\rVert\ \lVert x\rVert + \lVert x+y\rVert\ \lVert y\rVert.
\end{align}$$

The result follows immediately.

As a consequence we see that $$\mathbb R^n$$ with the Euclidean norm is a normed vector space!  In fact it is a Banach space.  We call $$\mathbb R^n$$ endowed with this norm **Euclidean space**.

**Theorem:** Euclidean space $$\mathbb R^n$$ is a complete Banach space.


### Other metrics on real space

In lecture, we introduced several other norms $$\mathbb R^n$$:

* the **taxi cab norm**or **$$\ell^1$$ norm**

$$\lVert x\rVert_1 = \sum_{k=1}^n |x_k|.$$

* the **uniform norm** or **$$\ell^\infty$$ norm**

$$\lVert x\rVert_\infty = \max_k |x_k-y_k|.$$

* the **$$\ell^p$$ norm** (for $$1 < p < \infty$$)

$$\lVert x\rVert_p = (\sum_{k=1}^n |x_k|^p)^{1/p}.$$

All of these make the vector space $$\mathbb R^n$$ into a Banach space.  For example, if we let $$X = \{1,2,\dots, n\}$$ with the discrete topology, then we can identify $$\mathbb R^n$$ with $$\mathcal B(X,\mathbb R)$$, by letting $$x$$ correspond to the function $$f(k) = x_k$$ under this identification, the uniform norms of each space are the same.

In general, we must establish that each of the above are norms on $$\mathbb R^n$$ by showing that they satisfy the relevant properties.  The only property that is not obvious is the **triangle inequality** which takes a bit of proving.

The starting point is the following observation for **conjugate exponents**, ie. real numbers $$1 < p,q < \infty$$ satisfying $$\frac{1}{p} + \frac{1}{q} = 1$$.

**Theorem (Young's Inequality):**  Let $$p$$ and $$q$$ be conjugate exponents.  Then

$$ab\leq \frac{a^p}{p} + \frac{a^q}{q}$$

with equality if and only if $$a^p = b^q.$$

Note that when $$p=q=2$$, this is just a restatment of AM-GM, so this can be seen as a beautiful generalization of the inequality we used to prove Cauchy-Schwartz!

**Proof:**

First note that
$$ab = \exp(\ln(ab)) = \exp(\ln(a) + \ln(b)) = \exp(\frac{1}{p}\ln(a^p) + \frac{1}{q}\ln(b^q))$$
The function $$\exp(x)$$ is convex, so $$\exp(ux + (1-u)y)\leq u\exp(x) + (1-u)\exp(y)$$ for all $$x,y\in \mathbb R$$ and $$0 < u < 1$$.
Taking $$u = \frac{1}{p}$$, $$x = \ln(a^p)$$ and $$y= \ln(b^q)$$, we get

$$ab\leq \frac{1}{p}\exp(\ln(a^p)) + \frac{1}{q}\exp(\ln(b^q)) = \frac{1}{p}a^p + \frac{1}{q}b^q.$$

Leveraging Young's Inequality, we can prove Holder's inequality.

**Theorem (Holder's Inequality):**

Let $$p$$ and $$q$$ be conjugate exponents.  Then for all $$x,y\in \mathbb R^n$$, we have

$$|x\cdot y| \leq \lVert x\rVert_p\lVert x\rVert_q

To prove this, follow the same idea as the proof of Cauchy-Schwartz.

Finally, we can leverage Holder's inequality to prove the triangle inequality for $$\lVert\cdot\rVert_p$$.

**Theorem (Minkowski Inequality):**

Let $$1 < p < \infty$$.  Then for all $$x,y\in \mathbb R^n$$, we have

$$\left(\sum_{i=1}^n (x_i+y_i)^p\right)^{1/p}\leq \left(\sum_{i=1}^n x_i^p\right)^{1/p} + \left(\sum_{i=1}^n y_i^p\right)^{1/p}.$$

**Proof:**

$$\lVert x+y\rVert_p^p = \sum_k |x_k+y_k|^{p-1}|x_k+y_k| \leq \sum_k (|x_k|+|y_k|)|x_k+y_k|^{p-1}.$$

Now applying Holder's inequality, for $q$ the exponential conjugate of $$p$$

$$\lVert x+y\rVert_p^p \leq \left[\left(\sum_k |x_k|^p\right)^{1/p} + \left(\sum_k |y_k|^p\right)^{1/p}\right]\left(\sum_k |x_k+y_k|^{(p-1)q}\right)^{1/q} .$$

Now $$p = pq-q$$ so this says

$$\lVert x + y\rVert_p^p = (\lVert x\rVert_p + \lVert y\rVert_p)\lVert x + y\rVert_p^{p/q}$$

Dividing both sides by $$\lVert x + y\rVert_p^{p/q}$$, we see

$$\lVert x + y\rVert_p^{p-p/q} = (\lVert x\rVert_p + \lVert y\rVert_p)\lVert x + y\rVert_p^{p/q}.$$

Since $$p-p/q=1$$ this completes the proof.

**Theorem:** The linear space $$\mathbb R^n$$ with the norm $$\lVert \cdot\rVert_p$$ is a Banach space for all $$1\leq p\leq \infty$$.

