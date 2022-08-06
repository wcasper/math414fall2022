---
layout: page
title: Cardinality
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

**Additional reading:** Simmons 1.5 (numerical equivalence) and 1.6

### Cardinality
The **cardinality** $$\lvert A\rvert$$ of a set $$A$$ measures the number of elements of a set.

Here are some examples.
* The cardinality of $$\{1,2,\Delta\}$$ is $$3$$.
* The cardinality of $$\{\heartsuit,\diamondsuit,\clubsuit,\spadesuit\}$$ is $$4$$.

Cardinality is also generalized to infinite sets, starting with the observation of Cantor that for finite sets, two sets have the same cardinality if and only if there is a bijection between them.

**Definition 1:** We say sets $$A$$ and $$B$$ have the **same cardinality** ($$\lvert A\rvert = \lvert B\rvert$$) if there exists a bijective function from $$A$$ to $$B$$.

Likewise, by observing generalizations about the existence of injections or surjections in the finite case, we can obtain inequalities between cardinalities.

**Definition 2:** We say $$A$$ has **cardinality less than or equal to** $$B$$ ($$\lvert A\rvert \leq \lvert B\rvert$$) if there exists an injective function (one-to-one function) from $$A$$ to $$B$$.

**Definition 3:** We say $$A$$ has **cardinality greater than or equal to** $$B$$ ($$\lvert A\rvert \geq \lvert B\rvert$$) if there exists a surjective function (onto function) from $$A$$ to $$B$$.

Now one of the most beautiful things about this is that these three definitions are mutually compatible, even in the infinite situation!  For example one can show $$\lvert A\rvert \leq \lvert B\rvert$$ if and only if $$\lvert B\rvert\geq \lvert A\rvert$$.  This is captured by the next theorem.

**Theorem:** Let $$A$$ and $$B$$ be sets.  There exists an injective function $$f: A\rightarrow B$$ if and only if there exists a surjective function $$g: B\rightarrow A$$.  Consequently $$\lvert A\rvert \leq \lvert B\rvert$$ if and only if $$\lvert B\rvert\geq \lvert A\rvert$$.

This theorem which shows consistency between the intuitively motivated definitions above tells mathematicians that they are on the right track and that their definitions are "right" or "natural".  Adding to this sense of compatibility, we can prove $$\lvert A\rvert\leq \lvert B\rvert$$ and $$\lvert A\rvert \geq \lvert B\rvert$$ implies $$\lvert A\rvert = \lvert B\rvert$$.

**Schroeder-Bernstein Theorem:** Let $$A$$ and $$B$$ be sets.  There exists both an injective function $$f: A\rightarrow B$$ and a surjective function $$g: A\rightarrow B$$ if and only if there exists a bijective function $$h: A\rightarrow B$$.  Consequently $$\lvert A\rvert\leq \lvert B\rvert$$ and $$\lvert A\rvert \geq \lvert B\rvert$$ if and only if $$\lvert A\rvert = \lvert B\rvert$$.


### Countability

A set $$A$$ is **finite** or has **finite cardinality** if the number of elements in $$A$$ is finite.
Sets which are not finite are called **infinite**.
It turns out that cardinality can also distinguish between different sizes of infinity.
The "smallest" infinite cardinality is called **countably infinite**.
Loosely speaking, we call a set $$A$$ countably infinite if we can "count it", ie. enumerate the elements so that there is a first element, a second element, and so on.
Formally, this is the same as having a bijection from the natural numbers $$\mathbb N$$ to the set $$A$$.

**Definition 4:** We say a set is **countably infinite** if it has the same cardinality as $$\mathbb N$$.  We call a set **countable** if it is either finite or countably infinite.  Sets which are not countable are called **uncountable**.

At first glance, it can be pretty startling that we can't count some sets.
Intuitively, it makes sense that you should be able to by just grabbing one element, then another, and then another.
Since we are doing this mathematically, we don't have to be limited by finite time either, we can just keep deciding which element is the billionth, which is the billionth-and-first, and so on.  However, some sets are so big that this simply is mathematically impossible, no matter how long you are counting for.

**Example:** The open interval $$(0,1)$$ is uncountable.  To show this, we use the famous **Cantor diagonalization** argument.  We will assume that we have counted it and arrive at a contradiction.  Since we are assuming we have counted it, we can enumerate $$(0,1) = \{x_1,x_2,x_3,\dots\}$$ for some sequence of real numbers $$x_1,x_2,x_3,\dots$$.  Now let's write these all out in their decimal expansions

$$\begin{align*}
x_1 &= 0.d_{11}d_{12}d_{13}d_{14}d_{15}\dots\\
x_2 &= 0.d_{21}d_{22}d_{23}d_{24}d_{25}\dots\\
x_3 &= 0.d_{31}d_{32}d_{33}d_{34}d_{35}\dots\\
x_4 &= 0.d_{41}d_{42}d_{43}d_{44}d_{45}\dots\\
x_5 &= 0.d_{51}d_{52}d_{53}d_{54}d_{55}\dots\\
\vdots & \quad\quad\quad\vdots
\end{align*}$$

so that $$d_{jk}$$ is the $$k$$'th decimal place in the decimal expansion of $$x_k$$.
The right hand side of this looks like a big matrix, and we want to play with the main diagonal.  We consider the real number $$y$$ with decimal expansion

$$y = 0.d_1d_2d_3d_4d_5\dots,\quad \text{with}\ d_k = d_{kk} + 2\mod 10$$

Clearly $$y\in (0,1)$$ and since $$(0,1) = \{x_1,x_2,x_3,\dots\}$$ we must have $$y=x_k$$ for some $$k$$.
However, by definition we see that $$y\neq x_k$$ for all $$k$$ because both numbers have different values in the $$k$$'th decimal place!

So far, this proves that $$(0,1)$$ has a bigger cardinality than $$\mathbb N$$, making it uncountable.
In fact, we can adapt Cantor's argument to prove that there are even bigger cardinalities.

**Theorem:** For any set $$X$$ the power set $$\mathcal P(X)$$ has larger cardinality than $$X$$.

Here the **power set** of $$X$$ is the set of subsets of $$X$$:

$$\mathcal P(X) = \{U: U\subseteq X\}.$$

**Question:** Which of the following sets have the same cardinalities?  Which of the following sets are countable?

$$\mathbb Z$$, $$\{n\in \mathbb Z: n\ \text{is even}\}$$, $$\mathbb R$$, $$\mathbb Q$$, $$\mathbb C$$

<body>
<center>
<button class="collapsible">see answer</button>
<div class="content">
  <p>
  The set of integers, set of even integers, and set of rational numbers are all countably infinite (and therefore have the same cardinality.
  The real and complex numbers both have the same cardinality as the interval (0,1) and are uncountable.
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







