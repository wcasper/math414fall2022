---
layout: page
title: Open sets
---

**Additional reading:** Simmons 2.10

### Open balls

Let $$(X,d)$$ be a metric space.  Given a point $$x_0\in X$$ and a real number $$r>0$$, we define the **open ball** centered at $$x_0$$ of radius $$r$$ to be the set

$$B_r(x_0) = \{x\in X: d(x_0,x) < r\}.$$

The motivation for this name comes from the special case when $$X = \mathbb R^n$$ with the Euclidean metric.
* when $$n=1$$, $$B_r(x_0)$$ is the open interval $$(x_0-r,x_0+r)$$;
* when $$n=2$$, $$B_r(x_0)$$ is the open disk in the plane centered at $$x_0$$ of radius $$r$$;
* when $$n=3$$, $$B_r(x_0)$$ is the open ball of radius $$r$$ centered at $$x_0$$.

Of course in this generality, open balls don't have to take the shape of balls anymore.

**Example:**  The function

$$d(x,y) = \max \{|x_k-y_k|: 1\leq k\leq n\}.$$

for $$x = (x_1,\dots,x_n)$$ and $$y = (y_1,\dots,y_n)$$ defines a metric on $$\mathbb R^n$$.  Open balls with this metric take the shape of diamonds.

### Open sets

Open balls allow us to define "neighborhoods" of points.  We can express how close one point is to another by specifying an open ball to which both points belong.  The radius of the open ball controls the actual closeness.
However, there's nothing particularly important about requiring neighborhoods to be ball-shaped.  In many applications it's actually kind of unnatural.  For example, if we want to consider all points in $$\mathbb R^2$$ which are close to a particular curve $$y = f(x)$$, the neighborhoods that we are interested are going to be more naturally tube-shaped.  This leads us to try to find a more general definition of neighborhoods, which we call **open sets**.

**Definition:** Let $$(X,d)$$ be a metric space.  A subset $$U\subseteq X$$ is called **open** if for every point $$x_0\in X$$ there is a radius $$r>0$$ (which can depend on $$x_0$$ such that $$B_r(x)\subseteq U$$.

In other words, a subset $$U\subseteq X$$ is open if every point in $$X$$ is also contained in an open ball contained in $$X$$.

**Example 1:** Every open ball $$B_r(x)$$ for $$r>0$$ and $$x\in X$$ is an open set.  This is not immediately obvious, since we need to prove that given $$y\in B_r(x)$$ we can choose $$\epsilon>0$$ with $$B_\epsilon(y)\subseteq B_r(x)$$.  To do so, we need to rely on the fact that our metric satisfies the triangle inequality, so that

$$d(x,z)\leq d(x,y) + d(y,z).$$

Therefore if we choose $$\epsilon = r-d(x,y)$$ then $$z\in B_\epsilon(y)$$ implies $$d(y,z)\lt r-d(x,y)$$ so that $$d(x,z)\lt r$$ and $$z\in B_r(x)$$.  Hence $$B_\epsilon(y)\subseteq B_r(x)$$.  In fact this is one good reason why having the triangle inequality is important!

**Example 2:** Both the empty set and the whole space $$X$$ are open.  Both are easy consequences of the definition.

**Example 3:** Let $$\mathbb R$$ be the real line with the Euclidean metric.  Then the open subsets of $$\mathbb R$$ consist of disjoint unions of a countable collection of open intervals.

**Example 4:** Let $$X$$ be any set and let $$d$$ be the discrete metric

$$d(x,y) = \left\lbrace\begin{array}{cc}0,&x=y\\1,&x\neq y\end{array}\right.$$

Then $$X$$ is a metric space and every subset of $$X$$ is open.


### Properties of open sets

Open sets satisfy the following fundamental property which will later be used to characterize *any* topological space.

**Theorem:** The intersection of a finite collection of open sets is open.  The union of a arbitrary collection of open sets is open.

In the special case of a metric space, we can characterize open sets even more specifically.  In particular, open sets are exactly the same things as unions of open balls.

**Theorem:** In a metric space $$X$$ a set $$U$$ is open if and only if it is the union of a collection of open balls.


### More general sets

Of course, not all sets in a metric space need to be open.  Sometimes it is useful to consider the "open part" of a subset $$A\subseteq X$$, which we call the interior.

**Definition:** The **interior** $$\text{int}(A)$$ of a subset $$A\subseteq X$$ is the set of all points $$x\in A$$ for which there is a ball centered at $$x$$ contained in $$A$$, ie.

$$\text{int}(A) = \{x\in A:\ \ \exists r>0\ \text{s.t.}\ B_r(x)\subseteq A\}.$$

**Example:** If $$U$$ is open, then $$\text{int}(U)=U$$.

**Example:** The interior of the unit square $$A = [0,1]\times [0,1]$$ in $$\mathbb R^2$$ (with the Euclidean metric) is the open square $$(0,1)\times (0,1)$$.

**Example:** The interior of the singleton set $$\{3\}$$ in $$\mathbb R$$ (with the Euclidean metric) is $$\varnothing$$.


**Question:** Which of the following facts about subsets $$A$$ and $$B$$ of a metric space $$X$$ are TRUE and which are FALSE?
* (A) The interior $$\text{int}(A)$$ is an open set
* (B) $$\text{int}(A\cup B) = \text{int}(A)\cup \text{int}(B)$$
* (C) $$\text{int}(A\cap B) = \text{int}(A)\cap \text{int}(B)$$

<details>
  <summary>Answer for (A).</summary>
  This is TRUE!  Try checking the definition of an open set.
</details>
<details>
  <summary>Answer for (B).</summary>
  This is FALSE!  The only thing we can say for sure is $$\text{int}(A\cup B) \supseteq \text{int}(A)\cup \text{int}(B)$$
</details>
<details>
  <summary>Answer for (C).</summary>
  This is TRUE!  Try proving it yourself.
</details>






