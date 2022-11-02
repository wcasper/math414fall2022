---
layout: page
title: Separation Axioms
---

**Additional reading:** Simmons 5.26 and 5.27

As part of our goal in studying topological spaces, we are faced with a very natural question: which topological spaces are essentially the same and which are fundamentally different?  As we have seen above, this essentially amounts to the question of which topological spaces are homeomorphic.
This is far from a unique experience in any field of mathematics, as a fundamental question in any discipline is how to tell whether one thing is the same as another.

In topology, one way we can tell whether certain things are different is to study *topological properties*, properties which are preserved under homeomorphism.
We will a certain collection of such properties here, called **separation properties** or **separation axioms**, which give a qualitative description of the fineness of a topology.  While these are called axioms, the are not fundamental axioms like in set theory.  Rather, they are additional properties that topological spaces can possess, which mathematicians will sometimes restrict their attention to.

### Separation axioms

Separation axioms talk about how distinct two points in a topological space are from the point of view of open sets.
Suppose $$x_1$$ and $$x_2$$ are distinct elements of $$X$$.
Then we have the following possible separation axioms.

**Definition:**  A topological space is called
* **Kolmogorov** or $$T_0$$ if every pair of points has an open set including one point but exluding another;
* **Frechet** or $$T_1$$ if every pair of points has a corresponding pair of open sets including each point but excluding the other;
* **Hausdorff** or $$T_2$$ if every two points have disjoint open neighborhoods.

To summarize, we have the following table.

|  Axiom  | Space | Condition |
| ------- | ----- | --------- |
| $$T_0$$ | Kolmogorov space | there is an open set containing exactly one of $$x_1$$ or $$x_2$$ |
| $$T_1$$ | Frechet space | there are two open sets $$U_1$$ and $$U_2$$ such that $$x_i\in U_i$$ and $$x_j\notin U_i$$ for $$i=1,2$$ and $$j\neq i$$ |
| $$T_2$$ | Hausdorff space | there are two poen sets $$U_1$$ and $$U_2$$ such that $$x_i\in U_i$$ for $$i=1,2$$ and $$U_1\cap U_2 = \varnothing$$ |

We can impose an even stronger condition by replacing our points with sets.

|  Axiom  | Space | Condition |
| ------- | ----- | --------- |
| $$T_3$$ | regular Hausdorff space | $$T_1$$ and any point and any closed set have disjoint open neighborhoods |
| $$T_4$$ | normal Hausdorff space | $$T_1$$ and any disjoint closed sets have disjoint open neighborhoods |
| $$T_5$$ | completely normal Hausdorff space | any subspace is $$T_4$$ |

At some point the naming scheme gets absurd.  For example, $$T_6$$ spaces are called perfectly normal Hausdorff spaces.  There is probably a lesson here about using *descriptive naming schemes* so that future generations aren't stuck with trying to remember the difference between normal, regular, perfect, and other unqualified qualitative descriptors.

These axioms are in order of increasing strength, so that for example a $$T_3$$ space is necessarily a $$T_1$$ space.

**Question:** How many topologies on $$X = \{1,2,3\}$$ are $$T_1$$?
<details>
  <summary>reveal solution</summary>
  There is only one, the discrete topology!  In fact, we can prove that any finite set which is $$T_1$$ must have the discrete topology.
</details>
<br/>

### Examples

Given all of the new defintions, it is important to also inundate ourselves with examples.  Simultaneously, this will help to innoculate us against common pitfalls or misconceptions about properties that all topological spaces must satisfy.

**Example:** Let $$X = \{1,2\}$$ with the topology $$\tau = \{\varnothing, \{1\}, \{1,2\}\}$$.  Then $$X$$ is $$T_0$$ but not $$T_1$$.  This space is called **Serpinski space**.

**Example:** Let $$X = \{1,2,3\}$$ with the topology $$\tau = \{\varnothing, \{3\}, \{2,3\}, \{1,2,3\}\}$$ is $$T_0$$ but not $$T_1$$.

**Example:** Let $$X = \mathbb{R}$$ with the cofinite topology.  Then $$X$$ is $$T_1$$ but not $$T_2$$.

**Example:** Let $$X = \mathbb{R}$$ with the Euclidean topology.  Then $$X$$ is Hausdorff.

**Example:** Any metrizable space is $$T_5$$.

**Example:** Let $$X = \mathbb{R}$$ and $$K = \{1/n: n\in \mathbb{N}\}$$ and consider the topology on $$X$$ defined by

$$\tau = \{U\subseteq X: U\in\tau_{eucl}\}\cup \{U\backslash K: U\in \tau{eucl}\}.$$

Then $$X$$ is Hausdorff but is not regular or normal.


