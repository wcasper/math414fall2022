---
layout: page
title: Urysohn's Lemma
---

**Additional reading:** Simmons 5.27, 5.28 and 5.29

As we already know, every metric space is in fact a topological space.
In fact, this was a big part of our motivation of the definition of a topological space!
* metric spaces were designed to generalize $$\mathbb R^n$$, replacing the usual distance formula with a distance function
* topological spaces were designed to generalize metric spaces, replacing open balls with arbitrary open neighborhoods

Furthermore, we saw that some but not all topological spaces are homeomorphic to metric spaces, and these spaces we called **metrizable**.
This leads to a natural and fundamental question.

**Question:** Which topological spaces are metrizable?

This question is pretty intimidating, given how weird topological spaces can be!
Consequently, our goal is instead to provide a set of general conditions describing when a topological space is metrizable.
Urysohn provides such a set below in **Urysohn's Embedding Theorem**.

### Urysohn's Lemma

As a starting point, we want to explore the relationship between the fineness of the topological space and the existence of a rich collection of continuous, real valued functions.  If $$X$$ is a set with the discrete topology, every real-valued function on $$X$$ is continuous.  However, if $$X$$ has the trivial topology then the only continuous functions on $$X$$ are constant functions, so we are definitely lacking a rich variety!

So how many functions might we want?
One thought is that we should at least desire enough functions to separate points.

**Definition:** The collection of continuous, real-valued functions on a topological space $$X$$ **separates points** if given any two different points $$x,y\in X$$, there exists a continuous function $$f: X\rightarrow\mathbb{R}$$ with $$f(x)\neq f(y)$$.

For some results, we desire even stronger conditions, like the continuous functions separating points and arbitrary closed sets!

**Definition:** A topological space is **completely regular** if it is $$T_1$$ and for any closed subset $$C\subseteq X$$ and point $$x\in X$$ not in $$C$$, there exists a continuous function $$f: X\rightarrow\mathbb R$$ satisfying $$f(x) = 0$$ and $$f(y) = 1$$ for all $$y\in C$$.
Completely regular spaces are sometimes called **Tychonoff spaces** or $$T_{3\frac{1}{2}}$$.

In particular the condition that a space is $$T_{3\frac{1}{2}}$$ is slightly stronger than being $$T_3$$ but weaker than being $$T_4$$.
Of course, this isn't at all immediately apparent!
One way to see this is the following fundamental result, which shows that functions not only separate points and closed sets, but they even separate pairs of closed sets!

**Urysohn's Lemma:** Let $$X$$ be $$T_4$$ and let $$A$$ and $$B$$ be disjoint, closed subsets of $$X$$.  Then there exists a continuous, real valued function $$f: X\rightarrow\mathbb R$$ whose range is $$[0,1]$$ with $$f(x) = 0$$ for $$x\in A$$ and $$f(x) = 1$$ for $$x\in B$$.

**Proof:** Since $$X$$ is $$T_4$$ (ie. normal) there exists disjoint open neighborhoods $$U_{1/2}$$ of $$A$$ and $$V_{1/2}$$ of $$B$$.  It follows that $$\overline {U_{1/2}}$$ is contained in $$B'$$.  To summarize:

$$A\subseteq\subseteq U_{1/2}\subseteq\overline{U_{1/2}}\subseteq B'.$$

Now we can repeat this process with the closed sets $$A, U_{1/2}'$$ and $$\overline{U_{1/2}},B'$$ to get two new open sets $$U_{1/4}$$ and $$U_{3/4}$$ satisfying

$$A\subseteq U_{1/4}\subseteq\overline{U_{1/4}}\subseteq U_{1/2}\subseteq\overline{U_{1/2}}\subseteq U_{3/4}\subseteq \overline{U_{3/4}}\subseteq B'.$$

Continuing recursively, we obtain a collection of open sets $$\{U_r: r\in D\}$$, indexed by the set $$D$$ of dyadic rationals in $$(0,1)$$, satisfying

$$U_r\subseteq \overline{U_r}\subseteq U_s,\quad \forall\ r < s,\ r,s\in D.$$

Now define $$f: X\rightarrow\mathbb R$$ by

$$f(x) = \sup\{r\in D: x\notin U_r\}.$$

For any $$a\in (0,1)$$,

$$f^{-1}([0,a)) = \bigcup_{r\in D,\ r < a} U_r,\quad f^{-1}((a,1]) = \bigcup_{r\in D,\ r > a} (\overline{U_{r}})',$$

which are open sets.  Thus the preimages of all the elements of a particular open subbasis of $$[0,1]$$ are open, so $$f$$ is continuous.

**Remark:** There's nothing special about $$0$$ and $$1$$ here.  By rescaling and shifting, we can make $$f$$ equal to $$a$$ on $$A$$ and $$b$$ on $$B$$ for any real numbers $$a$$ and $$b$$.

One consequence of Urysohn's Lemma has to do with trying to extend continuous functions defined on closed sets to continuous functions on the entire space.

**Tietze Extension Theorem:** Let $$X$$ be a normal space and suppose that $$C\subseteq X$$ is closed.  Given a continuous function $$f_0: C\rightarrow \mathbb R$$ whose range lies in a bounded interval $$[a,b]$$, there exists a continuous function $$f: X\rightarrow\mathbb R$$ whose range also lies in $$[a,b]$$ with $$f(x) = f_0(x)$$ for all $$x\in C$$.  In other words, $$f$$ extends the function $$f_0$$ defined on $$C$$ to the whole space $$X$$.

**Remark:** This is definitely false, if $$C$$ is not closed!  For example, $$f(x) = \sin(1/x)$$ is continuous on $$(0,1]$$, but cannot be extended continuously to $$[0,1]$$.

**Proof of Theorem:**
By shifting and rescaling, without loss of generality we may assume $$[a,b] = [-1,1]$$.
Then $$A_0 = f^{-1}([-1,-1/3])$$ and $$B_0 = f^{-1}([1/3,1])$$ are disjoint closed sets, so we can make a continuous function $$g_0: X\rightarrow \mathbb R$$ taking values in $$[-1/3,1/3]$$ which is equal to $$1/3$$ on $$B_0$$ and $$-1/3$$ on $$A_0$$.

Now consider the continuous fucntion $$f_1(x) = \frac{3}{2}(f(x) - g_0(x))$$.  Then $$|f_1(x)|\leq 1$$ and $$|g_0(x)|\leq 1/3$$.
Define $$A_1 = f_1^{-1}([-1,-1/3])$$ and $$B_1 = f_1^{-1}(1/3,1)$$.
Again, we can find a continuous function $$g_1$$ on $$X$$ taking values in $$[-1/3,1/3]$$ which is equal to $$1/3$$ on $$B_1$$ and $$-1/3$$ on $$A_1$$.

Recursively, define $$f_n(x) = \frac{3}{2}(f_{n-1}(x) - g_{n-1}(x))$$, $$A_n = f_n^{-1}([-1,-1/3])$$, $$B_n = f_n^{-1}([1/3,1])$$, and let $$g_n$$ be a continuous, real-valued function on $$X$$ which is equal to $$-1/3$$ on $$A_n$$ and equal to $$1/3$$ on $$B_n$$.
Then $$|f_n(x)|\leq 1$$ for all $$x\in C$$, and $$|g_n(x)|leq 1/3$$ for all $$x\in X$$.

Now define a function

$$g(x) = \sum_{k=0}^\infty g_k(x)(\frac{2}{3})^k.$$

The comparison test proves that the series on the right hand side converges, and it is easy to see $$g(x) = f(x)$$ for all $$x\in C$$.
Moreover, the series of partial sums

$$s_n(x) = \sum_{k=0}^n g_k(x)(\frac{2}{3})^k$$

are all continuous and in the uniform norm

$$\lVert s_n - g \rVert = \sup_{x\in X} \left|\sum_{k=n+1}^\infty g_k(x)(\frac{2}{3})^k\right| \leq \sum_{k=n+1}^\infty \frac{1}{3}\frac{2}{3}^k = \frac{2}{3}^{n+1}.$$

Thus $$s_n$$ converges to $$g$$ in the uniform norm, forcing $$g$$ to be continuous.

### Urysohn's Embedding Theorem

It is easy to check that metric spaces are automatically $$T_4$$, so one immediately sees that one of the necessary conditions for a topological space to be metrizable is for it to be $$T_4$$ also.
Interestingly, not much more is needed for a wide collection of topological spaces to be shown to be metrizable!

Urysohn's idea is that every subspace of a metric space is also a metric space, with the subspace metric.
Therefore, to show that a topological space is metrizable, what he should try to do is find some sort of way to relate it to a subspace of a metric space.
Of course, the metric space we consider may have to be very large in order to contain so many other topological spaces as subspaces!
The metric space Urysohn ended up considering was the set $$\ell^2(\mathbb{N})$$ of all square-summable real sequences.

$$\ell^2(\mathbb N) = \{(a_0,a_1,a_2,\dots): a_j\in \mathbb R\ \forall j,\ \sum_{k=0}^\infty a_j^2 < \infty\}.$$

Since we can add two sequences together to produce another, the above set is actually a vector space.
In particular it is a **normed vector space** with norm

$$\lVert (a_n) \rVert = \sqrt{\sum_{k=0}^\infty a_k^2}.$$

As we know, normed vector spaces are automatically metric spaces.
This space is a particularly nice example, since it is complete as a metric space, making it a **Banach space**.
Even better, this vector space has a dot product or **inner product**, so it is an example of a complete inner product space, also called a **Hilbert space**.


**Urysohn's Embedding Theorem:** Let $$X$$ be a $$T_4$$ space which is second-countable.  Then there exists a homeomorphism from $$X$$ to the metric space $$\ell^2(\mathbb N)$$.  In particular $$X$$ is homeomorphic to a metric space and thus metrizable.

**Proof:** see text.


