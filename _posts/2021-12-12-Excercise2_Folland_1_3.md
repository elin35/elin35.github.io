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
    Let $\mathcal M$ be a $\sigma$-algebra on a set $X$ and let $\varnothing \neq F\subseteq X$ ($E$ is not necessarily contained in $\mathcal M$). Then the collection of sets
    $$
      \mathcal M' := \{E\cap F: E\in \mathcal M\}
    $$
    is a $\sigma$-algebra on $F$.
    <details markdown="1">
      <summary><strong>Proof</strong></summary>
      Let $E\cap F \in \mathcal M'$. Then taking the complement with respect to $F$, we have
      $$
      \begin{align*}
        (E\cap F)^c &= E^{c}\cup F^c =E^c \cup \varnothing = E^{c_X} \cap F \in \mathcal M'
      \end{align*}
      $$
      where $E^{c_X}$ denotes the complement of $E$ taken with respect to $X$. Next, consider $(E_j\cap F)_1^\infty \subset \mathcal M'$. Then we see that
      $$
        \bigcup_{j=1}^\infty E_j\cap F = \left(\bigcup_{j=1}^\infty E_j\right)\cap F \in \M'
      $$
      since $\bigcup_1^\infty E_j \in \mathcal M.$ Thus, $\mathcal M'$ is indeed a $\sigma$-algebra over $F$.
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

