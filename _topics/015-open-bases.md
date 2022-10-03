---
layout: page
title: Open Bases and open subbases
---

**Additional reading:** Simmons 3.18

While dealing with open balls for metric spaces was oftentimes a little cumbersome, it did have the advantage of allowing us to thing of all the open sets without explicitly having to write down exactly what the open sets are.  The open sets in a metric space are whatever we can get by taking the union of a bunch of open balls.
This level of convenience isn't something we want to throw away!

Just like when we are thinking about vector spaces, we don't necessarily want to have to spell out the vector space by writing down every single vector in it.  Instead, we can write down a *basis* for the vector space and say that every vector in the vector space is a linear combination of the elements of this basis!
In the same way, a topological basis is a collection of elements of the topology which generate every other element of the topology.  (The analogy falls a bit flat, since there is no notion of linear independence).

### Open bases

**Definition:** An **open base** for a topological space $$(X,\tau)$$ is a subset $$\beta\subseteq\tau$$ with the property that every element in $$\tau$$ is a union of elements in $$\beta$$.  The elements of $$\beta$$ are called **basic open sets**.

**Example:**  The collection of open intervals $$\{(a,b): a, b\in\mathbb R,\ a < b\}$$ is an open base for the Euclidean topology on $$\mathbb R$$.

Intuitively an open base for a topology fills in the role of "nice" open sets, in the same way open balls work in metric spaces.  In fact, the open balls of a metric space form an open base for the topology!  Of course, this isn't the only example of an open base for the metric space, and we can actually find an open base $$\beta$$ which is countable when $$X$$ is separable.

**Definition:** A topological space is **separable** if it has a countable dense subset, ie. if there exists a countable subset $$A\subseteq X$$ with $$\overline{A} = X$$.

**Theorem:** Let $$X$$ be a separable metric space and let $$\{x_1,x_2,\dots\}$$ be a countable dense subset.  Then the collection $$\beta = \{B_{1/m}(x_n): 0< m,n\in \mathbb{Z}\}$$ is a countable open basis for $$X$$.

Having a *countable* basis for a topology is so useful sometimes that a topological space having this property deserves its own definition.

**Definition:** A topological space with the property that it has a countable open basis is called a **second countable space** or said to satisfy the **second axiom of countability**.

As a consequence, every open subset of a separable metric space can be made up of a union of at most *countably* many open sets.
In general, the question of how many open subsets we might have to union together to make an open set is an important property of a topological space.

**Definition:** A topological space $$X$$ is called **Lindelof** if for every collection $$\{U_i: i\in I\}$$ of open sets, there exists a countable subset $$J\subseteq I$$ with $$\bigcup_{i\in I} U_i = \bigcup_{j\in J} U_j.$$

In other words in a Lindelof space, if we build a complicated looking open subset out of an uncountable union of open sets, then we know we can actually throw out most of the ingredients until we have a countable collection which still builds the same open set.

The idea of writing an open set as a union of a bunch of other open sets is useful enough that it also comes with its own terminology.

**Definition:** Let $$U$$ be an open set.  A collection of open subsets $$\{U_i: i\in I\}$$ satisfying $$U=\bigcup_{i\in I}U_i$$ is called an **open cover** of $$U$$.
If $$J\subseteq I$$ is such that $$\bigcup_{j\in J} U_j = U$$, then the subcollection $$\{U_j: j\in J\}$$ is called an **open subcover** of the open cover $$\{U_i: i\in I\}$$.

With this terminology, we can say that being Lindelof is the same thing as saying that every open cover having a countable open subcover.

One of the main useful facts about second countable spaces is that they are automatically Lindelof.

**Lindelof's Theorem:**  Any second countable space is Lindelof.

Note that being Lindelof does not in general imply that the topological space is second-countable.

**Example:**

Let $$X=\mathbb R$$ and let $$\beta$$ be the collection of all left clopen intervals $$\beta = \{[a,b): a,b\in\mathbb R,\ a < b\}$$ and let $$\tau$$ be the collection of all unions of arbitrary collections of elements of $$\beta$$.  Then $$\tau$$ is a topology.  This topology is Lindelof but is not second countable.

The real line with this topology is called the **Sorgenfrey line**.
The fact that $$\mathbb R$$ with the usual Euclidean topology *is* second countable tells us that this topology is very different!

## Open subbases

Of course, in a topological space, we can take both arbitrary unions and finite intersections.
Thus a natural question is starting with a collection $$\gamma$$ of subsets of $$X$$, what sets can we get by taking arbitrary unions and finite intersections of elements of $$\beta$$?

**Lemma:**
Let $$\gamma$$ be a collection of subsets of $$X$$ and let $$\beta$$ be the collection of all finite intersections of elements of $$\gamma$$.  The the collection $$\tau$$ of all unions of arbitrary collections of elements of $$\beta$$ is a topology on $$X$$.

**Definition:**
Let $$X$$ be a topological space with topology $$\tau$$.  Let $$\gamma$$ be a collection of sets such that any arbitrary union of finite intersections of elements of $$\gamma$$ is an open set and such that every open subset of $$X$$ is of this form.  Then $$\gamma$$ is called an **open subbase** for $$X$$, or a **generating set** for the topology $$\tau$$.  The topology $$\tau$$ is said to be **generated by** $$\gamma$$.

**Example:**  The collection of semi-infinite open intervals $$\{(-\infty,a): a\in\mathbb R\}\bigcup\{(b,\infty): b\in \mathbb R\}$$ is an open subbase for the Euclidean topolgy on $$\mathbb R$$.


**Problem:**
We have shown that in a metric space, a singleton set $$\{x_0\}$$ is always closed.
Is the same true for any arbitrary topological space?

<details>
  <summary>Solution.</summary>
  No!  Consider for example the trivial topology.
</details>



