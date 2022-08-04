---
layout: page
title: What is topology?
---


The shapes of a cube, a sphere, and a torus are all different but of these three the torus is the *most* different in a very important way.
In particular, we can "morph" a cube into a sphere by smoothing the edges and pushing in the corners.

<p align="center"><img src="fig/cube-to-sphere.png"/></p>

However, no amount of squeezing, pulling, or massaging will allow us to transform a torus into a sphere or a cube, at least not without cutting and regluing parts of our shape.  The torus has some property that makes its shape fundamentally different from the other two.  Topology studies properties of different shapes, called **topological spaces**, which cannot be changed by squeezing and pulling.  At its heart, it tries to decide which topological spaces are topologically equivalent, called **homeomorphic**, or distinct.

**Question:** Which of the following properties are *topological properties* of a surface (such as a sphere, cube, or torus), meaning that they don't change even if we change the shape by squeezing, pulling and massaging it?


<style>
.collapsible {
  background-color: #777;
  color: white;
  cursor: pointer;
  padding: 18px;
  width: 100%;
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
  background-color: #f1f1f1;
}
</style>

<button class="collapsible">the surface area</button>
<div class="content">
  <p>Careful!  The surface area can definitely change as we squeeze and pull the object.</p>
</div>
<button class="collapsible">the number of corners on the surface</button>
<div class="content">
  <p>Careful!  Things like corners can be smoothed out.</p>
</div>
<button class="collapsible">the number of holes in the surface</button>
<div class="content">
  <p>Right!  Setting aside the important step of rigorously defining a "hole", there's no way to repair a hole by pulling or squeezing the surface.  Nor is there a way to make new holes, without ripping our surface.</p>
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




