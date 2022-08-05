---
layout: page
title: The algebra of sets
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

**Additional reading:** Simmons 1.2 and 1.4

There are several natural operations for creating new sets out of old ones.

* the **union** of two sets $$A$$ and $$B$$ is the set of all the elements in $$A$$ and $$B$$ combined

$$A\cup B = \{x: x\in A\ \text{or}\ x\in B\}.$$

* the **intersection** of two sets $$A$$ and $$B$$ is the set of all the elements $$A$$ and $$B$$ have in common

$$A\cap B = \{x: x\in A\ \text{and}\ x\in B\}.$$

* the **Cartesian product** or simply **product** of two sets $$A$$ and $$B$$ is the set of all pairs of elements

$$A\times B= \{(a,b): a\in A,\ b\in B\}.$$

* the **complement** of a set $$A$$ is the set of all the elements in the universe $$U$$ not in $$A$$

$$A' = \{x\in U: x\notin A\}.$$

Here $$U$$ is the universe that we are working inside, whose value should be determined from the context.

Put together, these operations satisfy several natural properties.  One such property is **distributivity**:

$$A\cap(B\cup C) = (A\cap B)\cup (A\cap C)$$

$$A\cup(B\cap C) = (A\cup B)\cap (A\cup C)$$

Additionally, taking complements swaps unions and intersections.  This is sometimes referred to as **De Morgan's law:**

$$(A\cup B)' = A'\cap B'$$

$$(A\cap B)' = A'\cup B'$$

**Question:** Decide if each of the following statements about algebra with sets is TRUE or FALSE.
* (A) the complement of $$A'$$ is $$A$$
* (B) $$A\cup B=B$$ if and only if $$B\subseteq A$$
* (C) $$A\cap B=B$$ if and only if $$B\subseteq A$$
<body>
<center>
<button class="collapsible">result for (A) </button>
<div class="content">
  <p>TRUE.  Carefully working through the definition, you should be able to see that taking the complement of a complement gets you back to where you started.</p>
</div>
<button class="collapsible">result for (B) </button>
<div class="content">
  <p>FALSE.  Actually the first statement is equivalent to A being a subset of B</p>
</div>
<button class="collapsible">result for (C) </button>
<div class="content">
  <p>TRUE.  Try drawing a Venn diagram to see that these two conditions are the same.</p>
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

We can take the union or intersection of a collection of sets at the same time.  In particular if $$\{A_i: i\in I\}$$ is a collection of sets indexed by $$I$$, then we define

$$\bigcup_{i\in I} A_i = \{x: x\in A_j\ \text{for some j\in I}\}.$$

$$\bigcap_{i\in I} A_i = \{x: x\in A_j\ \text{for all j\in I}\}.$$

Again, both **De Morgan's Laws** and **distributivity** hold:

$$B\cap \bigcup_{i\in I} A_i = \bigcup_{i\in I} (B\cap A_i)\quad\text{and}\quad B\cup \bigcap_{i\in I} A_i = \bigcap_{i\in I} (B\cup A_i)$$

$$\left(\bigcup_{i\in I} A_i\right)' =  \bigcap_{i\in I} A_i'\quad\text{and}\quad\left(\bigcap_{i\in I} A_i\right)' =  \bigcup_{i\in I} A_i'$$

## Bigger products

We can take the product of a collection of several sets

$$A_1\times A_2\times\dots A_n = \{(a_1,a_2,\dots,a_n): a_j\in A_j\ \forall 1\leq j\leq n\}.$$

We can even do this for an arbitrary collection of sets

$$\prod_{i\in I} A_i = \{(a_i)_{i\in I}: a_j\in A_j\ \forall j\in I\}.$$


