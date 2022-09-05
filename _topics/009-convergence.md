---
layout: page
title: Convergence and Completeness
---

**Additional reading:** Simmons 2.12

### Convergence
Convergence of sequences in a metric space is simply a direct generalization of convergence studied in calculus.

**Definition:** A sequence $$\{x_n\}$$ in a metric space $$X$$ is said to **converge** if there exists a point $$x\in X$$ such that 

$$\forall\ \epsilon > 0,\ \ \exists\ N>0,\ \text{such that}\ \ n\geq N\Rightarrow d(x_n,x) < \epsilon.$$

Equivalently, we could say

$$\forall\ \epsilon > 0,\ \ \exists\ N>0,\ \text{such that}\ \ x_n\in B_\epsilon(x)\ \forall n\geq N.$$

In this case, we call $$x$$ the **limit** of $$\{x_n\}$$ and that the sequence **converges to** $$x$$ or **approaches** $$x$$ and write $$x_n\rightarrow x$$.
The notion of a limit can also be captured in terms of limit points.

**Theorem:** A sequence $$\{x_n\}$$ taking infinitely many values converges if and only if as a set it has one, and only one, limit point.

**Example:** Let $$X = [0,1]$$ with the Euclidean metric.  The sequence $$\{x_n\}$$ defined by $$x_n = 1/n$$ converges to $$0$$.

**Example:** Let $$X = (0,1)$$ with the Euclidean metric.  The sequence $$\{x_n\}$$ defined by $$x_n = 1/n$$ does not converge.

### Cauchy Sequences

As we see in the previous example, a sequence can "try to converge", but still fail if the underlying metric space $$X$$ is missing points in a certain sense.  We can characterize the sequences which are trying to converge as *Cauchy sequences*.  We can thereby characterize the metric spaces which are not missing any points, giving us the notion of *complete metric spaces*.

**Definition:** A **Cauchy sequence** is a sequence $$\{x_n\}$$ satisfying the property that 

$$\forall\ \epsilon > 0,\ \ \exists\ N>0,\ \text{such that}\ \ m,n\geq N\Rightarrow d(x_m,x_n) < \epsilon.$$

In other words, a Cauchy sequence is a sequence whose terms get closer and closer to one-another as the indices increase.

**Theorem:** If $$\{x_n\}$$ is a convergent sequence, then $$\{x_n\}$$ is Cauchy.
**Proof:** Suppose that $$x_n\rightarrow x$$.  Then for all $$\epsilon>0$$ there exists $$N$$ such that $$n\geq N$$ implies $$d(x_n,x) < \epsilon/2$$.  Thus by the triangle inequality, for $$m,n\geq N$$ we have

$$d(x_m,x_n)\leq d(x_m,x) + d(x_n,x)\leq \epsilon/2 + \epsilon/2 = \epsilon.$$

This completes the proof.

**Definition:** A metric space $$X$$ is called **complete** if every Cauchy sequence in $$X$$ converges.

**Example:** By the Bolzano-Weierstrass Theorem, the real numbers $$\mathbb{R}$$ converges.

**Example:** The open interval $$(0,1)$$ with the Euclidean metric is not complete.

**Theorem:** Let $$X$$ be a complete metric space and $$Y$$ a subspace.  Then $$Y$$ is complete if and only if it is closed.

**Example:** The closed interval $$[0,1]$$ with the Euclidean metric is complete.

If we have a metric space $$X$$ which is not complete, we can always find a space filling in the missing points, called a *completion*.  However, in order to define the completion in a rigorous way, we will need the notion of functions between metric spaces.


**Question:** Let $$X$$ be a set with the discrete metric.  Is $$X$$ complete?

<details>
  <summary>Yes, totes.</summary>
  That's right!  In particular, a Cauchy sequence $$\{x_n\}$$ for the discrete metric will necessarily be constant for large $$n$$.
</details>
<details>
  <summary>No way.</summary>
  Careful!  Try to see what Cauchy sequences look like for the discrete metric.
</details>






