---
layout: page
title: Topology Basics
---

**Additional reading:** Simmons 2.17

### Closed sets

Closed sets are defined exactly as they are defined for metric spaces.

**Definition:** Let $$X$$ be a topological space.  A subset $$A$$ of $$X$$ is **closed** if $$A'$$ is open.

Just like before, the compatibility of taking unions or intersections with remaining closed mirrors that of being open via De Morgan's laws.

**Theorem:** An intersection of any number of closed sets is closed.  A finite union of closed sets is closed.

All the interesting properties that we discussed for sets in metric spaces, interiors, closures, and boundaries, can be extended to topological spaces.
In fact, in many ways these definitions tend to be *simpler* because we have shed the bulky machinery of distances and open balls.

**Definition:** Let $$A$$ be a subset of a topological space $$X$$.  The **closure** of $$A$$ is the intersection of all closed subsets of $$X$$ containing $$A$$:

$$\overline{A} = \bigcap_{A\subseteq C \text{\ (closed) }\subseteq X} C.$$


**Problem:**
How many topologies are there possible to put on the set $$X = \{1,2,3\}$$?
How many homeomorphism classes are there?

<details
  <summary>Solution.</summary>
  There are $$29$$ different topologies, but only $$9$$ homeomorphism classes.  Can you find them all?
</details>



