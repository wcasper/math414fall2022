---
layout: page
title: Relations
---

<style>
.collapsible {
  background-color: #777;
  color: white;
  cursor: pointer;
  padding: 18px;
  width: 40%;
  border: none;
  text-align: left;
  outline: none;
  font-size: 15px;
}

.active, .collapsible:hover {
  background-color: #555;
}

.collapsible:after {
  content: '\002B';
  color: white;
  font-weight: bold;
  float: right;
  margin-left: 5px;
}

.active:after {
  content: "\2212";
}

.content {
  padding: 0 18px;
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.2s ease-out;
  background-color: #ffffff;
}
</style>

**Additional reading:** Simmons 1.5

### Relations

In mathematics, we are constantly trying to identify patterns and relationships, for example the relationship between $$x$$ and $$y$$-coordinates in a parabola $$y=x^2$$.  As such, it is imperative to have a formal way of describing various relationships.  One very slick way of accomplishing this is via the notion of a relation.

**Definition:** A **relation from a set $$A$$ to a set $$B$$** is a subset $$\mathscr R$$ of the cartesian product $$A\times B$$.  If $$A=B$$, then we say $$\mathscr R$$ is a **relation on $$A$$.$$$$**  Notation-wise, we write $$a\mathscr Rb$$ to mean that $$(a,b)\in\mathscr R$$.

Note that we don't have to use a fancy R to denote a relation.  You can often see relations denoted by $$\sim$$ or $$\equiv$$, or even a letter like $$f$$.  The choice of notation typically depends on the context or on the *kind* of relation we are dealing with.  The tremendous flexibility of the concept of a relation allows is immediately apparent via the very diverse roles they play.  Let's see some examples:

**Example:**  Let $$P$$ be the set of all living people in the world.  We define a relation $$\mathscr R$$ on $$P$$ by saying $$x\mathscr Ry$$ if $$x$$ and $$y$$ have a biological parent in common.  Thus for example (Venus Williams)$$\mathscr R$$(Serena Williams).

**Example:**  Let $$A=\{a,b,c,d\}$$ and $$B = \{1,2,3,4\}$$ and $$\mathscr R = \{(a,3),(b,2),(b,3)\}$$.  Then $$\mathscr R$$ is an equivalence relation from $$A$$ to $$B$$.  For example $$a\mathscr R3$$ and $$b\mathscr R2$$.

**Example:**  Let $$B$$ be the set of all published books.  Define a relation $$\mathscr R$$ from $$B$$ to $$\mathbb N$$ by saying $$x\mathscr R n$$ if and only if $$n$$ is the number of pages in book $$x$$.  

In the special case that $$\mathscr R$$ is an equivalence relation on $$A$$, we are typically interested in three specific properties.  

**Definition:**   We call $$\mathscr R$$ 

- **reflexive** if $$x\mathscr Rx$$ for all $$x\in A$$
- **symmetric** if $$x\mathscr R y$$ implies $$y\mathscr R x$$ for all $$x,y\in A$$
- **transitive** if $$x\mathscr R y$$ and $$y\mathscr R z$$ implies $$x\mathscr R z$$ for all $$x,y,z\in A$$

A relation $$\mathscr R$$ on $$A$$ which is reflexive, symmetric, and transitive is called an **equivalence relation**.  In this case, we define the **equivalence class** of an element $$a\in A$$ to be

$$
[a] = \{x\in A: a\mathscr Rx\}
$$

### Partitions

We can think of partitions as a mathematical formulation of "slicing up a pie".
A **partition** of a set $$A$$ is a collection of subsets $$\{A_i: i\in I\}$$ of $$A$$ satisfying two properties
* the collection is **pairwise disjoint**, meaning $$A_j\cap A_k =\varnothing$$ for $j\neq k$$,
* the union of the collection is all of $$A$$, ie. $$\bigcup_{i\in I} A_i=A$$.

It turns out that there is an intimate relationship between partitions and equivalence relations.  Starting with an equivalence relation $$\sim$$ on a set $$A$$, the set of equivalence classes of $$\sim$$ defines a partition of $$A$$.
Conversely, if we start with a partition $$\{A_i: i\in I\}$$ of $$A$$, then we can define a relation by saying $$x\sim y$$ if and only if $$x$$ and $$y$$ both belong to the same set $$A_i$$ for some $$i$$.  This relation is an equivalence relation and the equivalence classes are exactly the sets in the partition we started out with!  To summarize:

**Theorem:** There is a bijective correspondence between the set of all equivalence relations on a set $$A$$ and the set of all partitions of $$A$$ which identifies sets in the partition with equivalence classes.


**Question:** For each of the following relations on $$\mathbb Z$$, decide if the relation is reflexive, symmetric, or transitive.
* (A) $$x\mathscr y$$ iff $$x$$ divides $$y$$
* (B) $$x\mathscr y$$ iff $$x-y$$ is even
* (C) $$x\mathscr y$$ iff $$x-y$$ is odd
<body>
<center>
<button class="collapsible">answer for (A)</button>
<div class="content">
  <p>
  reflexive and transitive, but not symmetric
  </p>
</div>
<button class="collapsible">answer for (B)</button>
<div class="content">
  <p>
  reflexive, symmetric, and transitive
  </p>
</div>
<button class="collapsible">answer for (C)</button>
<div class="content">
  <p>
  symmetric but not reflexive or transitive
  </p>
</div>
</center>
<script>
var coll = document.getElementsByClassName("collapsible");
var i;

for (i = 0; i < coll.length; i++) {
  coll[i].addEventListener("click", function() {
    this.classList.toggle("active");
    var content = this.nextElementSibling;
    if (content.style.maxHeight){
      content.style.maxHeight = null;
    } else {
      content.style.maxHeight = content.scrollHeight + "px";
    } 
  });
}
</script>
</body>

<br/>

## Formal definition of a function
The way that we have defined functions is how we tend to use them in practice.
However, it is a bit lackluster from a mathematical point of view, since we are introducing some kind of new undefined term we are calling a "rule".
The right way to define a function is in terms of sets.
In fact, as you probably already know a function is really a special kind of set!

Formally, a **function** $$f: A\rightarrow B$$ is a subset $$\Gamma_f$$ of the Cartesian product $$A\times B$$ satisfying two properties
* for all $$x\in A$$ there exists $$y\in B$$ with $$(x,y)\in \Gamma_f$$
* if $$(x,y)\in \Gamma_f$$ and $$(x,y')\in \Gamma_f$$ then $$y=y'$$

Then notationally, the statement $$f(x) = y$$ is just a new way of writing $$(x,y)\in\Gamma_f$$.
Thus the first property guarantees that $$f$$ assigns every value of $$x$$ to a value of $$y$$.
The second property says that each $$x$$ is assigned to at most one value of $$y$$.
The subset $$\Gamma_f$$ is sometimes called the **graph of** $$f$$.  

Subsets of the Cartesian product $$A\times B$$ are called **relations**.  We will talk more about relations later on.






