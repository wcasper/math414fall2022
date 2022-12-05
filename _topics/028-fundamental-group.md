---
layout: page
title: Fundamental group
---

### Groups

A group $$G$$ is a set with a binary operation $$ * $$ which takes any two elements $$g_1,g_2\in G$$ and makes another element $$g_1 * g_2$$ satisfying the following properties:
* (associativity) $$(g_1 * g_2) * g_3 = g_1 * (g_2 * g_3)$$
* (identity) there is a special element $$e\in G$$ with $$e * g = g * e = g$$ for all $$g\in G$$
* (inverses) for each $$g\in G$$ there is a special element $$g^{-1}$$ with $$gg^{-1} = g^{-1}g = e$$

The most important example for us is the **free group**.

**Definition:** A function $$\varphi: G\rightarrow H$$ from a group $$G$$ to a group $$H$$ satisfying $$\varphi(g_1 * g_2) = \varphi(g_1) * \varphi(g_2)$$ for all $$g_1, g_2\in G$$ is called a **homomorphism**.  Two groups are **isomorphic** if there exists a bijective homomorphism from one to another.

### Fundamental group

**Theorem:** Let $$\gamma,\eta,\mu$$ be loops based at $$a$$.  Then

$$[(\gamma * \eta) * \mu] = [\gamma * (\eta * \mu)].$$

**Theorem:**  

Let $$e_a: [0,1]\rightarrow X$$ be the constant loop based at $$a$$.  Then for all loops based at $$a$$

$$[\gamma * e_a] = [e_a * \gamma ] = [\gamma].$$

**Theorem:**

Let $$\gamma$$ based at $$a$$ and let $$\overline\gamma$$ be the reverse path.  Then

$$[\overline \gamma * \gamma ] = [\gamma * \overline\gamma ] = [e_a].$$

**Definition:** The **fundamental group based at a** is the set $$\pi_1(X;a)$$ is the set of homotopy classes of loops based at $$a$$, ie.

$$\pi_1(X;a) = \{[\gamma]:\ \text{$\gamma$ is a loop based at $a$}\}.$$


**Theorem:** The fundamental group $$\pi_1(X;a)$$ is a group with binary operation $$[\gamma] * [\eta] = [\gamma * \eta]$$, identity $$[e_a]$$, and inverses $$[\gamma]^{-1} = [\overline{\gamma}].$$

**Theorem:** Suppose that $$X$$ is path connected.  Then for any points $$a$$ and $$b$$, $$\pi_1(X;a)\cong\pi_1(X;b)$$.

Due to this, we will often omit the base point when talking about fundamental groups.

**Example:** Let $$X= \mathbb R$$.  Then $$\pi_1(X;a) = \{[e;a]\}$$ is the trivial group.

**Example:** Let $$X = S^1$$ be the unit circle in $$\mathbb R^2$$.  Then $$\pi_1(X)\cong\mathbb{Z}$$.

**Example:** Let $$X = \mathbb S^2$$ be the unit sphere in $$\mathbb R^3$$.  Then $$\pi_1(X)$$ is the trivial group.

**Example:** Let $$X = \mathbb S^1\times\mathbb S^1$$ be a torus.  Then $$\pi_1(X)\cong \mathbb{Z}\times\mathbb{Z}$$.

**Example:** Let $$X = \mathbb R^2\diff\{p_1,\dots,p_n\}$$. Then $$\pi_1(X)$$ is a free group with $$n$$ generators.

**Definition:** A path connected topological space whose fundamental group is trivial is called **simply connected**.

**Theorem:** Let $$f: X\rightarrow Y$$ be a continuous function of topological spaces.  Then $$f$$ induces a homomorphism

$$\varphi_f: \pi_1(X;a)\rightarrow \pi_1(X;f(a)),\quad [\gamma]\mapsto [f\circ\gamma].$$

If $$f$$ is a homeomorphism, then this is an isomorphism.

In particular, this implies that homeomorphic topological spaces must have the same fundamental groups!





