---
layout: page
title: Functions
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

**Additional reading:** Simmons 1.3

Loosely speaking, a **function** $$f: A\rightarrow B$$ from a set $$A$$ to a set $$B$$ is a rule which associates to each element of $$A$$ a unique element $$f(a)$$ of $$B$$, which we call the **image** of $$a$$ under $$f$$.  Functions are so common in mathematics that they end up going by many names, such as **map**, **transformation**, or **operator**.  The language that is favored often depents on the flavor of mathematics we are studying.

* **Example:** $$f: (0,\infty)\rightarrow \mathbb R$$ with the rule $$f(x) = 1/x^2$$ is a function
* **Example:** $$f: \mathbb R\rightarrow \mathbb R$$ with the rule $$f(x) = 1/x$$ is not defined at $$x=0$$, so it doesn't satisfy our definition of a function
* **Example:** $$f: (0,\infty)\rightarrow \mathbb R$$ with the rule $$f(x)^2 = x$$ is not a function because it associates every point $$x$$ with two points $$\pm\sqrt{x}$$.

The set $$A$$ is called the **domain** of the function and $$B$$ is called the **codomain**.  The set of all values that the function attains over its domain is called the **range**.

### Special kinds of functions

A function $$f: X\rightarrow\mathbb R$$ from a set $$X$$ to the real numbers is called a **real function** on $$X$$.
Likewise, a function $$f: X\rightarrow\mathbb C$$ is called a **complex function**.
A function whose range consists of a single value is called a **constant function**.

Suppose that $$A$$, $$B$$, and $$C$$ are sets with $$C\subseteq A$$.  Then given a function $$f: A\rightarrow B$$, we can define the **restriction** of $$f$$ to $$C$$ by

$$f\vert_C: C\rightarrow B,\ \ f\vert_C(x) = f(x)\ \forall x\in C.$$

In other words, $$f\vert_C$$ is the function which borrows the rule of $$f$$ but only applies it on the smaller set $$C$$.  In this setting, we also refer to $$f$$ as an extension of $$f\vert_C$$.

## Properties of functions



## Formal definition of a function

**Question:** Which of the following statements about algebra with sets is FALSE?
* (A) the complement of $$A'$$ is $$A$$
* (B) $$A\cup B=B$$ if and only if $$B\subseteq A$$
* (C) $$A\cap B=B$$ if and only if $$B\subseteq A$$
<body>
<center>
<button class="collapsible">obviously the answer is (A) </button>
<div class="content">
  <p>Careful!  Carefully working through the definition, you should be able to see that taking the complement of a complement gets you back to where you started.</p>
</div>
<button class="collapsible">no way, the answer is (B) </button>
<div class="content">
  <p>Right!  Actually the first statement is equivalent to A being a subset of B</p>
</div>
<button class="collapsible">can't trick me, it's (C) </button>
<div class="content">
  <p>Careful!  Try drawing a Venn diagram to see that these two conditions are the same.</p>
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
## Bigger unions and intersections





