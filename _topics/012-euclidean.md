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

**Lemma (Cauchy's Inequality):** If $$x,y\in \mathbb R^n$$ then

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






