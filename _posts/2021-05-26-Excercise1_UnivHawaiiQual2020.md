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

[**University of Hawai'i at Mānoa: Analysis Qualifying Exam, Fall 2020, Problem 6**](http://math.hawaii.edu/home/graduate/qualifying-exams/analysis/Analysis_Fall_20.pdf)

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
<ol>
  <li>
    <em>Folland (p35,37)</em>: We define the <strong>Lebesgue measure</strong>, $m$, by 

      $$
       m(E) = \inf\left\{ \sum_{j=1}^\infty (b_j-a_j) : E \subset \bigcup_{j=1}^\infty (a_j,b_j)\right\}
      $$

      for any Lebesgue measurable set E (Borel $\sigma$-algebra on $\mathbb{R}$).
  </li>
  
  <br>
  
  <li>
    <em>Folland (p98)</em>: A family $(E_r)_{r>0}$ of Borel subsets of $\mathbb{R}^n$ is said to <strong>shrink nicely</strong> to some $x\in\mathbb{R}^n$ if 
     <ul>
       <li>
         $E_r\subset B_r(x)$ for each $r>0$
       </li>
       <li>
         There exists an $\alpha>0$, for all $r>0$, such that $m(E_r) > \alpha m(B_r(x))$.
       </li>
     </ul>
  </li>
  
  <br>
  
  <li>
    <em>Folland (p98)</em>: The <strong>Lebesgue Differentiation Theorem</strong>. Suppose $f\in L^1_{\text{loc}}$. For every $x$ in the Lebesgue set of $f$; in particular, for almost every $x$, we have
    
    $$
      \lim_{r\to0} \frac{1}{m(E_r)}\int_{E_r} f(y)dy = f(x)
    $$
    
    for every family $(E_r)_{r>0}$ that shrinks nicely to $x$.
  </li>
</ol>
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

Suppose such an $E$ exists. Then since $E\neq \varnothing$, for some $x\in E$, let's first consider the family of intervals $(I_r)_{r>0}$ where

$$ I_r = (x-r, x+r) $$

It is clear that $(I_r)$ shrinks nicely to $x$. Next, we note that the characteristic function $\mathcal{X}_E \in L^1(\mathbb{R})$. Thus, by the Lebesgue differentiation theorem, we have that

$$ 
\begin{align*}
    \mathcal{X}_E(x) &= \lim_{r\to0} \frac{1}{m(I_r)} \int_{I_r}\mathcal{X}_E dy \\
    &= \lim_{r\to0}\frac{1}{m(I_r)} \int_\mathbb{R} \mathcal{X}_{E\cap I_r}dy \\
    &= \lim_{r\to0} \frac{m(E\cap I_r)}{m(I_r)}\\
    &< \lim_{r\to 0} \frac{99}{100}\\
    &= \frac{99}{100}
\end{align*}
$$

Thus, $\mathcal{X}_E(x) < \frac{99}{100}$, but this contradicts that $\mathcal{X}_E(x) = 1$ since $x\in E$. Hence, no such $E$ exists.

</details>  
<br />


