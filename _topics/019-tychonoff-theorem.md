---
layout: page
title: Tychonoff's Theorem
---

**Additional reading:** Simmons 4.23

Tychonoff's Theorem states that the product of any collection of compact spaces is also compact, and is one of the most applicable basic results in general topology.
To prove Tychonoff's Theorem, we will first go through a brief digression on Zorn's Lemma and the Axiom of Choice.

### Zorn's Lemma

Zorn's Lemma is a statement about *posets*, partially ordered sets, which provides the existence of a maximal element of a poset.

**Definition:** Let $$P$$ be a poset.  An element $$a\in P$$ is **maximal** if $$a\leq b$$ implies $$a = b$$ for all $$b\in P$$.

Obviously, posets need not have maximal elements.

**Example:** The set $$\mathbb R$$ of all real numbers with the usual ordering does not have a maximal element.

Furthermore, even if $$P$$ has a maximal element, it need not be unique!

**Example:** Let $$P$$ be the set of all *proper* subsets of $$\{1,2,3\}$$, with partial ordering given by inclusion.  Then $$A=\{1,2\}$$ and $$B = \{2,3\}$$ are both maximal elements of $$P$$.

In general, Zorn's Lemma provides a useful condition under which a partially ordered set is guaranteed to have a maximal element.
The characterization is based on *chains*.

**Definition:** A **chain** in a poset $$P$$ is a subset $$C\subseteq P$$ where every pair of elements in $$C$$ are comparable.

**Zorn's Lemma:** Let $$P$$ be a nonempty poset and suppose that every chain in $$P$$ has an upper bound in $$P$$.  Then $$P$$ contains at least one maximal element $$m$$.

**Proof:**
Suppose that $$P$$ is a poset where every chain in $$P$$ has an upper bound in $$P$$, but that $$P$$ does not have a maximal element.
Let $$\mathcal C$$ be the collection of all chains in $$P$$.
Then given any chain $$C\in P$$, we know that $$C$$ has an upper bound $$\vee C$$.  Since $$\vee C$$ is not a maximal element, we can choose an element $$b_C\in P$$ with $$b_C\neq \vee C$$ and $$\vee C\leq b_C$$.
Choosing such an element for each chain $$C$$, we define a function $$b: \mathcal C\rightarrow P$$ with $$b(C) = b_C$$ for all $$C\in\mathcal C$$.

Now using $$b$$, we can recursively build a sequence by starting with an element $$a_1\in P$$ and then choosing $$a_2 = b(\{a_1\})$$, $$a_3 = b(\{a_1,a_2\})$$, and so on.
In fact, by transfinite recursion, we can build a collection $$\{a_i: i\in I\}$$ where $$I$$ is a totally ordered set, $$a_i < a_j$$ for $$i < j$$, and where the cardinality of $$I$$ is as large as we want.  In fact, we can take $$|I| > |P|$$, but this contradicts the fact that $$\{a_i: i\in I\}\subseteq P$$.
This completes the proof.

Our proof of Zorn's Lemma above relies on the constuction of the function $$b: \mathcal C\rightarrow P$$, which in turn relied on choosing an infinite collection of elements $$b_C$$, one for each $$C\in\mathcal C$$.
Mathematically, it is not at all obvious that this is a legitimate thing to do.
Can we choose an element from infinitely many collections of sets?
The assumption that we can do so is often taken as an axiom, called the **Axiom of Choice**.
The Axiom of Choice turns out to be equivalent to many other conditions, such as Zorn's Lemma, or the assumption that the product of infinitely many non-empty sets must be non-empty, or the assumption that every vector space has a basis.  In fact, Tychonoff's theorem turns out to be equivalent to the Axiom of Choice!

As a simple application of Zorn's Lemma, we will prove that every vector space $$V$$ has a basis.

**Theorem:** Let $$V$$ be a vector space.  Then $$V$$ has a basis.

**Proof:** Let $$P$$ be the collection of all linearly independent subsets of $$V$$, partially ordered by inclusion.  If $$C\subseteq P$$ is a chain in $$P$$, then $$C = \{A_i: i\in I\}$$ is a collection of linearly independent subsets of $$V$$ with $$A_i\subseteq A_j$$ or $$A_j\subseteq A_i$$ for all $$i,j\in I$$ with $$i\neq j$$.
This implies that $$\bigcup_{i\in I} A_i$$ is also a linearly independent collection of vectors in $$V$$ and it's easy to see that $$\bigcup_{i\in I} A_i = \vee C$$ is the upper bound of $$C$$.
Thus every chain in $$P$$ has an upper bound.  From Zorn's lemma, $$P$$ has a maximal element $$B$$.  Since $$B\in P$$, we know that $$B$$ is a collection of linearly independent vectors.  Moreover, if $$v\in V$$ is not in the span of $$B$$ then $$B\cup \{v\}$$ is larger than $$B$$, which contradicts maximality.  Thus $$B$$ must span $$V$$, making $$B$$ a basis for $$V$$.

### Tychonoff's Theorem 

**Tychonoff's Theorem:**  Let $$\{X_i: i\in I\}$$ be any collection of compact topological spaces. Then $$\prod_{i\in I} X_i$$ is compact.

To prove this, we first establish a lemma where we use Zorn's Lemma.

**Lemma:** Let $$X$$ be a set and let $$\mathcal C$$ be a collection of subsets of $$X$$ with the finite intersection property.  Then there exists a collection $$\mathcal B$$ of subsets of $$X$$ with the finite intersection property, with $$\mathcal C\subseteq \mathcal B$$, such that if $$\mathcal A$$ properly contains $$\mathcal B$$ then $$\mathcal A$$ does not have the finite intersection property.

**Proof:** Let $$P$$ be the poset consisting of all collections of subsets of $$X$$ with the finite intersection property which contain $$\mathcal C$$.  Every chain $$C = \{\mathcal A_i: i\in I\}$$ has an upper bound $$\bigcup_{i\in I} A_i$$, and so by Zorn's Lemma $$P$$ has a maximal element $$\mathcal B$$, which clearly satisfies the conditions above.


**Proof of Tychonoff's Theorem:**  Suppose that $$X = \prod_{i\in I} X_i$$.  We must show that every collection  $$\mathcal C$$ of closed subsets of $$X$$ with the finite intersection property has non-empty intersection, ie. $$\bigcap_{C\in\mathcal C} C \neq \varnothing$$.  Let $$\mathcal B$$ be the maximal collection of subsets of $$X$$ containing $$C$$ with the finite intersection property.
Obviously $$\bigcap_{B\in\mathcal B}\overline{B}\subseteq\bigcap_{C\in\mathcal C}C$$, so it suffices to prove that $$\bigcap_{B\in\mathcal B}\overline{B}\neq\varnothing.$$

The set $$\{\pi_i(B): B\in B\}$$ is a collection of subsets of $$X_i$$ with the finite intersection property.
Since $$X_i$$ is compact, it follows that $$\bigcap_{i\in I}\overline{\pi_i(B)}\neq \varnothing.$$
Choose $$x_i\in \bigcap_{i\in I}\overline{\pi_i(B)}$$ for all $$i\in I$$ and consider $$(x_i: i\in I)\in X$$.
If $$U_i$$ is a neighborhood of $$x_i\in X_i$$, then since $$x_i\in\overline{\pi_i(B)}$$ for all $$B\in \mathcal B$$, we know that $$U_i\cap \pi_i(B)\neq\varnothing$$ and therefore $$\pi_i^{-1}(U_i)\cap B\neq\varnothing$$.
By the maximality of $$\mathcal B$$, it follows that $$\pi_i^{-1}(U_i)\in \mathcal B$$.
Now if $$U$$ is an open set of $$X$$ containing $$(x_i)$$, then from the usual basis for the topology of $$X$$, there exists an open set of the form $$\prod_{i\in I}U_i$$ containing $$x_i$$ contained in $$U$$ with $$U_i=X_i$$ for all $$i\notin J$$ for some finite subset $$J\subseteq I$$. By definition, $$x_i\in U_i$$ for all $$i\in I$$.
Consequently, $$\prod_{i\in I}U_i = \bigcap_{j\in J}\pi_j^{-1}(U_j)$$ and thus

$$U\cap B\superseteq \bigcap_{j\in J}\pi_j^{-1}(U_j)\cap B \neq\varnothing$$

for all $$B\in \mathcal B$$.  Since $$U$$ was arbitrary, it follows that $$(x_i)\in\overline{B}$$ for all $$B\in\mathcal B$$.  Hence $$(x_i)$$ belongs to the intersection $$\bigcap_{B\in\mathcal{B}}\overline{B}$$, making the latter nonempty.


Using Tychonoff's Theorem, we can prove the following $$n$$-dimensional version of Heine-Borel:

**Heine-Borel Theorem (General version):**
A subset of $$\mathbb R^n$$ (with the Euclidean topology) is compact if and only if it is closed and bounded.

**Proof:**  Since $$\mathbb R^n$$ is a metric space, compact automatically implies closed and bounded.  Thus we are left with proving the other direction.  Let $$C$$ be a closed and bounded subset of $$\mathbb R^n$$.  Then since $$C$$ is bounded, there exists $$r>0$$ such that $$C\subseteq [-r,r]^n$$.
Furthermore, $$[-r,r]$$ is compact by the $$1$$-dimensional version of Heine Borel, so $$[-r,r]$$ is a product of $$n$$ compact spaces and hence is compact.
It follows that $$C$$ is a closed subspace of a compact space, and thus is compact.



