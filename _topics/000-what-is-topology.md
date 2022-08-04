---
layout: page
title: What is topology?
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

The shapes of a cube, a sphere, and a torus are all different but of these three the torus is the *most* different in a very important way.
In particular, we can "morph" a cube into a sphere by smoothing the edges and pushing in the corners.

<p align="center"><img src="fig/cube-to-sphere.png"/></p>

However, no amount of squeezing, pulling, or massaging will allow us to transform a torus into a sphere or a cube, at least not without cutting and regluing parts of our shape.  The torus has some property that makes its shape fundamentally different from the other two.  Topology studies properties of different shapes, called **topological spaces**, which cannot be changed by squeezing and pulling.  At its heart, it tries to decide which topological spaces are topologically equivalent, called **homeomorphic**, or distinct.
Often this comes down to showing that two different topological spaces have different topological properties.

**Question:** Which of the following properties are *topological properties* of a surface (such as a sphere, cube, or torus), meaning that they don't change even if we change the shape by squeezing, pulling and massaging it?
<body>
<button class="collapsible">(A) the surface area</button>
<div class="content">
  <p>Careful!  The area changes as we shrink or expand our shape by squeezing or stretching it.</p>
</div>
<button class="collapsible">(B) the number of corners</button>
<div class="content">
  <p>Careful!  Corners can be smoothed away, just like when we make a cube into a sphere.</p>
</div>
<button class="collapsible">(C) the number of holes</button>
<div class="content">
  <p>Right!  Setting aside the important task of rigorously defining a "hole", intuitively we can understand that by squeezing or stretching a surface we cannot change the number of holes.</p>
</div>

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

In this class, we will be mostly concerned with *point set topology*, which focuses on local properties of different shapes and have strong relationships with topics in real analysis.  For example, a point at the center of the letter *X* is somehow very different from the point at the center *Y*.  For this reason, the letters *X* and *Y* are not homeomorphic.  Point set topology works to understand this by understanding what each letter looks like "close to", or in a **neighborhood** of the point.  In this way a notion of what points are close together, or what constitutes a neighborhood, is the key idea in the definition of a **topological space**.  Once we decide what the neighborhoods (also called **open sets**) are, we can understand what it means for functions between topological spaces to be **continuous**.  


