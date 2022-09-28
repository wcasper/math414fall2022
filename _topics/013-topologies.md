---
layout: page
title: Topologies 
---

**Additional reading:** Simmons 3.16

### Topological spaces

When we studied metric spaces, the definition of a metric gave us a way to understand distances between points and thereby what "open sets" are.
However, the open sets themselves are what allow us to define continuity and convergence!
Topological spaces cut out the middle man: we decide what we want our open sets to be, without relying on a metric.

**Definition:** A **topological space** $$(X,\tau)$$ is a set $$X$$ with a collection $$\tau$$ of subsets of $$X$$ satisfying the following properties:
* $$\varnothing$$ and $$X$$ are elements of $$\tau$$
* any arbitrary union of elements of $$\tau$$ will also be in $$\tau$$
* any finite intersection of elements of $$\tau$$ will also be in $$\tau$$

In this case $$\tau$$ is called a **topology** on $$X$$ and the elements of $$\tau$$ are called **open sets**.
We will often omit $$\tau$$ and refer to $$X$$ as a topological space with collection $$\tau$$ of open sets floating around implicitly in the background.

**Example:** Let $$X = \{1\}$$ with $$\tau = \{\varnothing,\{1\}\}.$$ Then $$X$$ is a topological space.

**Example:** The **trivial** or **indiscrete** topology on a set $$X$$ is $$\tau = \{X,\varnothing\}$$

**Example:** The **discrete** topology on a set $$X$$ is $$\tau = \mathcal{P}(X)$$ (the power set of $$X$$).  Note that this is the same collection of open sets when we consider $$X$$ with the discrete metric.

**Example:** The **cofinite topology** on a set $$X$$ is the set $$\tau$$ consisting of the empty set along with all subsets whose complements are finite.

**Example:** Let $$X$$ be a metric space.  The collection $$\tau$$ of open sets as defined by the metric defines a topology on $$X$$ making $$X$$ into a topological space.

The last example says that all metric spaces are examples of topological spaces.  However, the opposite is not true in general!

**Definition:** A topological space $$(X,\tau)$$ is called **metrizable** if there exists a metric $$d$$ on $$X$$ so that the sets in $$\tau$$ are precisely the open sets with respect to the metric.

**Example:** Let $$X = \mathbb R$$ with the discrete topology.  Then $$X$$ is metrizable since if we take the discrete metric on $$\mathbb R$$, then all the sets are open sets.

**Example:** Let $$X = \mathbb R$$ with the trivial topology.  Then $$X$$ is not metrizable.  Can you explain why?

#### Subspaces

If $$X$$ is a metric space and $$Y\subseteq X$$ is a subset, then we can automatically make $$Y$$ into a metric space as well just by defining distance on $$Y$$ the same way as we define it on $$X$$.  In this case, we called Y a **subspace** of the metric space $$X$$.  In a similar sense, given a topological space $$X$$ we can automatically make any subset $$Y\subseteq X$$ into a topological space too.

**Definition:** Let $$(X,\tau)$$ be a topological space and let $$Y\subseteq X$$ be a subset.  Then

$$\tau' = \{U\cap Y: U\in \tau\}$$

defines a topology on $$Y$$ called the **relative topology**.  A subset of $$X$$ endowed with the relative topology is called a **subspace** of $$X$$.


### Continuous mappings and homeomorphisms

In the case of metric spaces, we had a beautifully simple characterization of continuous mappings completely in terms of open sets.
Since we have lost our metric, this characterization becomes the *defintion* of a continuous mapping.

**Definition:** Let $$(X,\tau)$$ and $$(Y,\eta)$$ be topological spaces and suppose that $$f:X\rightarrow X$$ is a function.
* We say that $$f$$ is **continuous** if and only if the preimage of every open subset of $$Y$$ is an open subset of $$X$$.  Equivalently, $$f^{-1}(V)\in \tau$$ for all $$V\in\eta$$.
* We say that $$f$$ is an **open mapping** if and only if the image of every open set is open.  Equivalently $$f(U)\in \eta$$ for all $$U\in \tau$$.

**Example:** Let $$X$$ and $$Y$$ be metric spaces.  Then a function $$f: X\rightarrow Y$$ is continuous as a map of topological spaces if and only if it is continuous as a map of metric spaces.

**Example:** Let $$X$$ be a set with the discrete topology and let $$Y$$ be any topological space.  Then any function $$f: X\rightarrow Y$$ will be continuous.

**Example:**  Let $$X$$ be $$\mathbb R$$ with the discrete topology and $$Y$$ be $$R$$ with the topology obtained from the Euclidean metric.  Then the map $$f: X\rightarrow Y$$ defined by $$f(x) = x$$ is bijective and continuous, but is not an open mapping.

Now suppose we are presented with the task of trying to figure out *all* of the topological spaces.
One thing that immediately becomes apparent is that some spaces that aren't technically the same really are actually the same!
For example, suppose that we let $$X = \{1\}$$ with the topology $$\{\varnothing, \{1\}\}$$ and $$Y = \{2\}$$ with the topology $$\{\varnothing, \{2\}\}$$.
These aren't the same topological space, but only because $$X$$ and $$Y$$ aren't the same set.  Otherwise, one is pretty much the same as the other, up to relabeling!
Topological spaces which are similar in this sense are called *homeomorphic*.

**Definition:**  Let $$X$$ and $$Y$$ be topological spaces.  A **homeomorphism** from $$X$$ to $$Y$$ is a function $$f: X\rightarrow Y$$ which is bijective, continuous, and an open map.  If there is a homeomorphism from $$X$$ to $$Y$$, then $$X$$ and $$Y$$ are called **homeomorphic**.

**Theorem:** Given a fixed collection of topological spaces, the relation $$\sim$$ defined by $$X\sim Y$$ if there is a homeomorphism from $$X$$ to $$Y$$ is an equivalence relation.  

The equivalence classes of the above equivalence relation are called **homeomorphism classes**.


**Problem:**
How many topologies are there possible to put on the set $$X = \{1,2,3\}$$?
How many homeomorphism classes are there?

<details
  <summary>Solution.</summary>
  There are $$29$$ different topologies, but only $$9$$ homeomorphism classes.  Can you find them all?
</details>


### The Zariski topology

One of the most interesting and useful topologies which is great departure from metric spaces is the **Zariski topology** on $$n$$-dimensional real space $$\mathbb R^n$$ or complex space $$\mathbb C^n$$.
Here the open sets are specifically defined as complements of the zeros of collections of multivariate polynomials.

**Example:** The subset $$U = \{(x,y,z)\in \mathbb R^3: x^2 + y^2 + z^2 \neq 1\}$$ is open in the Zariski topology, because it is the complement of the zero set of the polynomial $$x^2+y^2+z^2-1$$.

**Example:** The complement of the singleton set $$\{(1,2,5)\}$$ is open in th Zariski topology, since this singleton set is the zero set of the collection of polynomials $$\{x-1,y-2,z-5\}$$.

The Zariski topology plays a central role in the geometric point of view of abstract algebra, what mathematicians call *algebraic geometry*.  Using the Zariski topology, commutative rings coming from abstract algebra can be transformed into topological spaces.  Through this transformation, questions about algebraic properties of the ring are translated into questions about the geometry of the topological space!

