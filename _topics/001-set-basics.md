---
layout: page
title: Set basics
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

Sets play a fundamental role in all mathematics because under the hood almost everything is a set.  Numbers are sets.  Functions are sets.  Even topological spaces are sets.
Intuitively, a **set** is a collection of objects called **elements** and we write $$x\in A$$ means $$x$$ *is an element of* $$A$$.

We say that a set $$A$$ is a **subset** of a set $$B$$ if every element in $$A$$ is also an element in $$B$$.  Mathematically, we express this as either $$A\subset B$$ or $$A\subseteq B$$ (we use these interchangeably).
If $$A\subseteq B$$ and $$B\subseteq A$$, then we say $$A$$ and $$B$$ are **equal** and write $$A=B$$.  If $$A\subseteq B$$ and $$A\neq B$$, we say that $$A$$ is a **proper subset** of $$B$$ and write $$A\subsetneq B$$.

**Question:** Which of the following statements about sets is FALSE?
<body>
<center>
<button class="collapsible">(A) there is a set $$A$$ with $$A\subseteq B$$ for all sets $$B$$.</button>
<div class="content">
  <p>Careful!  The empty set is a subset of every set.  In fact it is the only set which is a subset of every other set.</p>
</div>
<button class="collapsible">(B) there is a set $$A$$ which </button>
<div class="content">
  <p>Careful!  Corners can be smoothed away, just like when we make a cube into a sphere.</p>
</div>
<button class="collapsible">(C) there exists a set $$A$$ with an element $$x\in A$$ satisfying $$x\subseteq A$$</button>
<div class="content">
  <p>Careful!  Sets can also be elements of other sets.  For example, if we take $$A = \{1,2,\{1\}\}$$ then $$\{1\}$$ is an element of $$A$$ but also a subset of $$A$$.</p>
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
## Examples of sets

Examples of sets include

$$
\begin{align*}
A &= \{1,2,3,a,b,c\}\\
B &= \{x: \text{$x$ is a real number and}\ 0\leq x \leq 2\}
\end{align*}
$$

The first set is in list **notation**, where the elements of the set are simply listed out.  The second set is in **set builder notation**, where the elements are determined by a specified condition.  A very important special example of a set is the **empty set** $$\varnothing$$ , which is the set not containing any elements.

Some special sets that we will rely on are
* the set $$\mathbb N$$ of natural numbers $$1,2,3,\dots$$
* the set $$\mathbb Z$$ of integers
* the set $$\mathbb Q$$ of rational numbers
* the set $$\mathbb R$$ of real numbers
* the set $$\mathbb C$$ of complex numbers
As an important special case for us, we adopt the typical notation for subintervals of the real numbers.



