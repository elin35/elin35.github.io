---
title: "Exercise 1"
date: 2021-05-26
categories:
  - Real Analysis
tags:
  - math
  - measure theory
  - lebesgue
---

**University of Hawai'i at Mānoa: Analysis Qualifying Exam, Fall 2020, Problem 6**

---

>Show that there is no measurable set $ E \subset \mathbb{R} $ that satisfies
>
>$$
>    \frac{1}{100} < \frac{m(E\cap I)}{m(I)} < \frac{99}{100}
>$$
>
>for every interval $I\subset \mathbb{R}$ where $m$ denotes the Lebesgue measure on $\mathbb{R}$.



<br />
<details markdown="1">
  <summary><strong>Tools and Facts</strong></summary>
1. From Folland (p35,37), we define the Lebesgue measure, $m$, by 

  $$
    m(E) = \inf\left\{ \sum_{j=1}^\infty (b_j-a_j) : E \subset \bigcup_{j=1}^\infty (a_j,b_j)\right\}
  $$

  for any Lebesgue measurable set E (Borel $\sigma$-algebra on $\mathbb{R}$.

</details>  
<br />




<br />
<details markdown="1">
  <summary><strong>Solution 1: From Definition</strong></summary>
Suppose such an $E$ exists. Then first instead consider the set $E_N = E\cap [-N,N]$, $N\in \mathbb{N}$, so that

$$m(E_N) \leq m([-N,N]) = 2N< \infty$$

Since $E_N$ is Lebesgue measurable, then for any family of intervals, $(I_k)_{k=1}^\infty$ such that 

$$ E_N \subset \bigcup_{k=1}^\infty I_k \quad \text{and} \quad m(E_N) \leq \sum_{k=1}^\infty m(I_k)$$

we know that 

$$
\begin{align*}
    m(E_N) &\leq m\left( E_N \cap \bigcup_{k=1}^\infty I_k\right)\\
    &\leq m\left ( E \cap \bigcup_{k=1}^\infty I_k\right)\\
    &= m\left( \bigcup_{k=1}^\infty E\cap I_k\right)\\
    &\leq \sum_{k=1}^\infty m(E\cap I_k)\\
    &< \frac{99}{100}\sum_{k=1}^\infty m(I_k)
\end{align*}
$$

Thus, we have that $\tfrac{100}{99}m(E_N) < \sum_{k=1}^\infty m(I_k)$. Hence,

$$ \frac{100}{99}m(E_N) \leq \inf\left\{ \sum_{k=1}^\infty m(I_k) : E_N \subset \bigcup_{k=1}^\infty I_k\right\} = m(E_N)$$

which implies that $m(E_N) = m(E\cap [-N,N]) = 0 < \frac{1}{100}m([-N,N])$, a contradiction.

</details>  
<br />




<br />
<details markdown="1">
  <summary><strong>Solution 2: Lebesgue Differentiation Theorem</strong></summary>



</details>  
<br />
