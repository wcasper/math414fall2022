---
layout: page
title: Closed sets
---

**Additional reading:** Simmons 2.11

### Closed sets

Closed sets are in a very literal way the opposite of open sets.

**Definition:** A subset $$A\subseteq X$$ of a metric space $$X$$ is called **closed** if its complement $$A'$$ is an open set.

Consequently, the complement $$U'$$ of any open set $$U$$ will automatically be closed.  From our knowledge of open sets, this gives us a lot of examples of closed sets right away.

**Example 1:** The empty set $$\varnothing$$ and the whole space $$X$$ are both closed.

**Example 2:** If $$U$$ is any open subset of $$X$$, then $$U'$$ is closed.

The analog of an open ball for closed sets is the **closed ball**

$$\overline B_r(x_0) = \{x\in X: d(x,x_0)\leq r\}.$$

Note the use of $$\leq$$ in place of $$\lt$$ for closed balls.

**Example 3:** The closed ball $$\overline B_r(x_0)$$ is a closed set.

This is not immediately apparent at all.  To show it, we must prove that the complement $$\overline B_r(x_0)'$$ is an open set.  To do so, it suffices to show that if $$x\notin $$\overline B_r(x_0)$$ then there exists $$\epsilon > 0$$ such that $$B_r(x_0)\cap B_\epsilon(x) = \varnothing$$.  Take $$\epsilon = d(x_0,x)-r$$.  Then for any $$y\in B_\epsilon(x)$$, the triangle inequality says

$$d(x_0,x) \leq d(x_0,y) + d(x,y) < d(x_0,y) + \epsilon$$

and therefore $$d(x_0,y) \gt d(x_0,x)-\epsilon = r$$ so that $$y\notin \overline B_r(x_0)$$.  This proves $$B_r(x_0)\cap B_\epsilon(x)=\varnothing$$ so that the complement of the closed ball is open.

As a special case, we see that closed intervals $$[a,b]$$ are closed subsets of $$\mathbb R$$ with the Euclidean topology.

Applying De Morgan's laws, the fact that a finite intersection of open sets is open and an arbitrary union of open sets is open translates immediately to some related facts about closed sets

**Theorem:** The intersection of an arbitrary collection of closed sets is closed.  The union of finitely many closed sets is closed.

This gives us the ability to construct very strange closed sets.

**Example 4:**  Define a sequence of closed intervals

$$\begin{align}
F_1 &= [0,1]\\
F_2 &= [0,1/3]\cup [2/3,1]\\
F_3 &= ([0,1/9]\cup[2/9,3/9])\cup ([6/9,7/9]\cup [8/9,9/9])\\
\vdots & \vdots\\
F_n &= \bigcup_{k=0}^{3^{n-1}-1}([3k/3^n,(3k+1)/3^n]\cup[(3k+2)/3^n]\cup[(3k+3)/3^n])
\end{align}$$

so that $$F_{n+1}$$ is obtained from $$F_n$$ be removing the middle third of each of the intervals.  Each of the $$F_n$$'s is a closed set, so the intersection $$C = \bigcap_n F_n$$ is also closed.  This set is called the **Cantor set** and is very interesting from the point of view of analysis (specifically measure theory).  It has a lot of very interesting properties, such as the fact that $$\int(C)=\varnothing$$.  At each stage in the construction, we remove a collection of intervals whose lengths sum to $$2^n/3^{n+1}$$.  This says the length left over is the original length $$1$$ minus $$\sum_{n}2^n/3^{n+1} = 1$$, so in a very specific way the "length" of $$C$$ is $$0$$.  However, you can prove that $$C$$ consists of all the points in $$[0,1]$$ that do not have a $$1$$ in their ternary expansions and therefore that $$C$$ has the same cardinality as $$[0,1]$$.

### Limit points

The definition of a closed set is a bit lackluster, since it is completely characterized by open sets.  However, there is another interesting and useful characterization of closed sets in terms of special points called *limit points*.

**Definition:** Let $$A$$ be a subset of a metric space $$X$$.  A point $$x\in X$$ is called a **limit point** of $$A$$ if for all $$r>0$$ the ball $$B_r(x)$$ contains at least one point of $$A$$ different from $$x$$.

Note that a limit point of a set $$A$$ does not necessarily belong to $$A$$.

**Example 1:** Consider the half-open interval $$A = [-1,3)$$ in $$\mathbb R$$ (with the Euclidean metric).  The point $$3$$ is not an element of $$A$$ but every open interval centered at $$3$$ will contain lots of points in $$A$$.  Therefore $$3$$ is a limit point of $$A$$.  In fact we can show that the set of limit points of $$A$$ is the closed interval $$[-1,3]$$.

The next theorem shows that limit points may be used to characterize closed sets.

**Theorem:** A subset $$A\subseteq X$$ is closed if and only if every limit point of $$A$$ is contained in $$A$$.


### Closures

This characterization allows us to define the closure of a set, which is the smallest closed subset of $$X$$ containing $$A$$.

**Definition:** The **closure** $$\overline A$$ of a subset $$A\subseteq X$$ is the union of $$A$$ and the set of limit points of $$A$$

$$\overline A = \{x\in X: x\in A\ \text{or $x$ is a limit point of $A$}\}.$$

Closures satisfy several nice properties, such as

* $$A$$ is closed if and only if $$\overline{A} = A$$
* if $$B\subseteq X$$ is closed and contains $$A$$ then $$\overline A\subseteq B$$
* $$\overline A$$ is the intersection of all closed subsets containing $$A$$

### Boundary points

**Definition:** A point $$x\in X$$ is a **boundary point** of $$A$$ if every open ball centered at $$x$$ intersects both $$A$$ and $$A'$$.  The **boundary** $$\partial A$$ of $$A$$ is the set of all boundary points of $$A$$.

The closure of $$A$$ gives a nice characterization of the boundary points of $$A$$.

**Theorem:** $$\partial A = \overline A\cap \overline{A'}$$



**Question:** Which of the following statement about a metric space $$X$$ and a subset $$A\subseteq X$$ are TRUE and which are FALSE?
* (A) Every subset of $$X$$ is either open or closed.
* (B) The boundary $$\partial A$$ is a closed set.
* (C) $$(\overline A)' = \text{int}(A')$$

<details>
  <summary>Answer for (A).</summary>
  This is FALSE!  Consider for example a half-open interval.
</details>
<details>
  <summary>Answer for (B).</summary>
  This is TRUE!  As we see from the previous theorem, it is the intersection of two closed sets.
</details>
<details>
  <summary>Answer for (C).</summary>
  This is TRUE!  Try proving it yourself!
</details>






