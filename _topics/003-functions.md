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

### Properties of functions

Three basic properties of functions are useful starting out.

* A function $$f: A\rightarrow B$$ is **one-to-one** or **injective** if $$f(x) = f(x')$$ implies $$x=x'$$ for all $$x,x'\in A$$.
* A function $$f: A\rightarrow B$$ is **onto** or **surjective** if for all $$y\in B$$ there exists $$x\in A$$ with $$f(x) = y$$.  Equivalently, if the codomain of $$f$$ is the same as the range of $$f$$.
* A function $$f: A\rightarrow B$$ is **bijective** if it is both injective and surjective.

### Special kinds of functions

A function $$f: X\rightarrow\mathbb R$$ from a set $$X$$ to the real numbers is called a **real function** on $$X$$.
Likewise, a function $$f: X\rightarrow\mathbb C$$ is called a **complex function**.
A function whose range consists of a single value is called a **constant function**.
The function $$f:X\rightarrow X$$ with the rule $$f(x) = x$$ is called the **identity function** on $$X$$.

Suppose that $$A$$, $$B$$, and $$U$$ are sets with $$U\subseteq A$$.  Then given a function $$f: A\rightarrow B$$, we can define the **restriction** of $$f$$ to $$U$$ by

$$f\vert_U: U\rightarrow B,\ \ f\vert_U(x) = f(x)\ \forall x\in U.$$

In other words, $$f\vert_U$$ is the function which borrows the rule of $$f$$ but only applies it on the smaller set $$U$$.  In this setting, we also refer to $$f$$ as an **extension** of $$f\vert_U$$.

Given another function $$g: B\rightarrow C$$ we can form the **composition** $$g\circ f: A\rightarrow C$$ which is defined by the rule $$(g\circ f)(x) = g(f(x))$$.

In the case that $$f$$ is bijective, we can define it's **inverse function** $$f^{-1}: B\rightarrow A$$ which is defined by the rule $$f^{-1}(y) = x$$ for $$y = f(x)$$.  In particular, we have the identities

$$f(f^{-1}(y)) = y\quad\text{and}\quad f^{-1}(f(x)) = x.$$

In terms of compositions, this says $$f\circ f^{-1}$$ is the identity function on $$B$$ and $$f^{-1}\circ f$$ is the identity function on $$A$$.

Note that the **only** functions which have inverses are bijections.  Even so, sometimes for convenience we call certain functions inverses, even when inverses don't exist!  What is meant is an inverse function on a restricted domain and range.  For example, $$\arcsin(x)$$ is an inverse function of $$\sin(x)$$ on the restricted domain $$[-\pi/2,\pi/2]$$ and codomain $$[-1,1]$$.  Changing the domain and codomain will change the inverse function, or cause it to cease to exist.

### Image and preimage

Consider a function $$f: A\rightarrow B$$.  The **image** of a subset $$U\subseteq A$$ under $$f$$ is

$$f(U) = \{y\in B: y=f(x)\ \text{for some}\ x\in U\}.$$

Images satisfy the following properties

* $$U_1\subseteq U_2\ \Rightarrow\ f(U_1)\subseteq f(U_2)$$
* $$f(\bigcup_I U_i) = \bigcup_I f(U_i)$$
* $$f(\bigcap_I U_i) \subseteq \bigcap_{I} f(U_i)$$

Likewise, the **preimage** of a subset $$V\subseteq B$$ under $$f$$ is

$$f^{-1}(V) = \{x\in A: y=f(x)\ \text{for some}\ y\in V\}.$$

**Note:** It is not necessary for $$f^{-1}$$ to be invertible for this to make sense!

Preimages satisfy the following properties

* $$V_1\subseteq V_2\ \Rightarrow\ f^{-1}(V_1)\subseteq f^{-1}(V_2)$$
* $$f^{-1}(\bigcup_I V_i) = \bigcup_I f^{-1}(V_i)$$
* $$f^{-1}(\bigcap_I V_i) = \bigcap_{I} f^{-1}(V_i)$$
* $$f^{-1}(V') = (f^{-1}(V))'$$

In particular, preimages are more well-behaved than images.  This will be seen repeatedly throughout the course.

**Question:** Let $$f: A\rightarrow B$$ be a function.  Prove that $$f(U_1\cap U_2) = f(U_1)\cap f(U_2)$$ for all subsets $$U_1,U_2\subseteq A$$ if and only if $$f$$ is injective.
<body>
<center>
<button class="collapsible">reveal solution</button>
<div class="content">
  <p>
  First suppose that our function is injective and define a new function
  $$g: f(A)\rightarrow A,\quad g(y) = x\ \text{for}\ f(x)=y.$$
  This new function is bijective and therefore has an inverse.  In fact
  $$f(U_1)\cap f(U_2) = g^{-1}(U_1)\cap g^{-1}(U_2) = g^{-1}(U_1\cap U_2) = f(U_1\cap U_2).$$
  Now to prove the other direction, suppose that 
  $$f(U_1\cap U_2) = f(U_1)\cap f(U_2),\ \forall U_1,U_2\subseteq A.$$
  Then
  $$f(\{x\}\cap \{x'\}) = f(\{x\})\cap f(\{x'\}),\ \forall x,x'\in A$$
  and thus
  $$\begin{align*}
  f(x') = f(x) & \Leftrightarrow f(\{x\})\cap f(\{x'\})\neq\varnothing\\
               & \Leftrightarrow f(\{x\}\cap \{x'\})\neq\varnothing\\
               & \Leftrightarrow x=x'.
  \end{align*}
  $$
  This proves that the function is injective.
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






