---
title: "Exercise 2"
date: 2021-12-12
categories:
  - Real Analysis
tags:
  - math
  - measure theory
---

**Folland - Real Analysis: Modern Techniques and Their Applications** 

---

>Let $\mathcal{M}$ be an infinite $\sigma$-algebra.
><ol type = "a">
>  <li>$\mathcal{M}$ contains an infinite sequence of disjoint sets.</li>
>  <li>card($\mathcal{M}$)$\ge$ card$(\mathbb{R})$</li>
></ol>

<br />
<details markdown="1">
  <summary><strong>Tools and Facts</strong></summary>
<ol>
  <li>
    <em>Folland (p21)</em>: We define a <strong>$\sigma$-algebra</strong> on a nonempty set $X$, is a non empty collection, $\mathcal{M}$, of subsets of $X$ such that $\mathcal{M}$ is closed under complement and countable union.
  </li>
  
  <br>
  
  <li>
    Let $\mathcal M$ be a $\sigma$-algebra on a set $X$ and let $F\subseteq X$ ($E$ is not necessarily contained in $\mathcal M$). Then the collection of sets
    $$
      \mathcal M' := \{E\cap F: E\in \mathcal M\}
    $$
    is a $\sigma$-algebra.
    
    <details markdown="1">
      <summary><strong>Proof</strong></summary>
    </details>
  </li>
  
</ol>
</details>  
<br />




<br />
<details markdown="1">
  <summary><strong>Solution: </strong></summary>
Suppose that $\mathcal{M}$ is an infinite $\sigma$-algebra on a set $X$. Then, we know that there must exist some $E_1\in\mathcal{M}$ such that $\varnothing \subsetneq E_1\subsetneq X$. It must be that either 
$$
  \mathcal{M}_1 = \{E \cap E_1 : E\in \mathcal{M}\} \quad \text{ or } \quad \mathcal{M}_1' =\{E\cap E_1^c: E\in \mathcal{M}\}
$$
is infinite; otherwise, if both are finite, then since
$$
  \mathcal{M} \subseteq \{A\cup A': A\in \mathcal M, A' \in \mathcal{M}'\}
$$
we have that card$(\mathcal{M}) \le$ card$( \{ A\cup A': A\in \mathcal M, A' \in \mathcal{M}' \} ) \le$ card$(\mathcal{M}) \cdot$card$(\mathcal{M}')$ which is finite, contradicting that $\mathcal{M}$ is infinite.

Thus, without loss of generality, suppose that $\mathcal{M}_1 = \{E\cap E_1: E\in \mathcal M\} is infinite. 

</details>  
<br />

