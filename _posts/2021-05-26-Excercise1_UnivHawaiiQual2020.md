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

> Show that there is no measurable set $ E \subset \mathbb{R} $ that satisfies
$$
  \begin{align*}
    \frac{1}{100} < \frac{m(E\cap I)}{m(I)} < \frac{99}{100}
  \end{align*}
$$
for every interval $I\subset \mathbb{R}$ where $m$ denotes the Lebesgue measure on $\mathbb{R}$.

Note that this problem can easily be generalized to the following:
> Let $0< \epsilon < 1$. Show that there is no measurable set $ E \subset \mathbb{R} $ that satisfies
$$
  \begin{align*}
    \epsilon < \frac{m(E\cap I)}{m(I)} < 1-\epsilon
  \end{align*}
$$
for every interval $I\subset \mathbb{R}$ where $m$ denotes the Lebesgue measure on $\mathbb{R}$.


<br />
<details markdown="1">
  <summary><strong>Intuition and Potential Traps</strong></summary>

Since the goal is to show that no such set $E$ exists, one will likely assume by contradiction that such an $E$ does exist. This is fine, but the next step is to see what might lead to a contradiction. My initial thought was that something must go wrong with the unique property that the set holds. That is, when intersected with any interval on the real line, it is not too similar to $I$ ($m(E\cap I) < (1-\epsilon)m(I)$) and not too dissimilar from $I$ ($m(E\cap I) > \epsilon m(I)$). If you begin to try to pick out a smart interval to try and see if you can break through the bound then that endeavor will be fruitless (unless it is possible and I'm just wrong). Intervals, under the Lebesgue measure, are too nice with their rescaling properties. Essentially, any interval will just be the same as $(0,1)$, so anything one might try will just reinforce that the property works as intended.  

Another way to think about it is that the above attempt is to try and use $E$ to reach a contradiction, but the correct method is not to use $E$, but to look at $E$ itself since that is the object that should not exist. This is what the two solutions below demonstrate. 

</details>  
<br />




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



</details>  
<br />




<br />
<details markdown="1">
  <summary><strong>Solution 2: Lebesgue Differentiation Theorem</strong></summary>



</details>  
<br />
