---
title: "Exercise 3" 
date: 2022-02-21
categories:
  - Real Analysis
  - Calculus
tags:
  - math
  - limits
  - stolz-cesaro
---

**Furdue - Limits, Series, and Fractional Part Integrals - Exercise 1.1**

--- 

> Let $\alpha$ be a positive number. Find the value of 
> $$
> \begin{align*} 
>   \lim_{n\to\infty} \sum_{k=1}^n \frac{1}{n+k^\alpha}
> \end{align*}
> $$

<br />
<details markdown="1">
  <summary><strong>Tools and Facts</strong></summary>
<ol>
  <li>
    <em>Stolz-Cesaro theorem</em>: If $(a_n)_{n=1}^\infty, (b_n)_{n=1}^\infty$ are sequences of real numbers such that $(b_n)$ is unbounded and monotone, then 
    
    $$
      \liminf_{n\to\infty} \frac{a_{n+1}-a_n}{b_{n+1}-b_n} \le \liminf_{n\to\infty} \frac{a_n}{b_n} \le \limsup_{n\to\infty}\frac{a_n}{b_n} \le \limsup_{n\to\infty} \frac{a_{n+1}-a_n}{b_{n+1}-b_n}
    $$
    
  </li>
  
</ol>
</details>  
<br />


<br />
<details markdown="1">
  <summary><strong>Solution: </strong></summary>
  We proceed by cases:
  
  1. If $\alpha=1$, then we simply evaluate,

  $$
  \begin{align*}
    \lim_{n\to\infty} \sum_{k=1}^n \frac{1}{n+k} = \lim_{n\to\infty} \frac{1}{n}\sum_{k=1}^n \frac{1}{1 + \frac{k}{n}} = \int_0^1 \frac{1}{1+x}dx = \ln(2)
  \end{align*}
  $$
  
  2. If $0<\alpha<1$, then 

  $$
    \lim_{n\to\infty} \sum_{k=1}^n \frac{1}{n+k^\alpha} = \lim_{n\to\infty} \frac{1}{n} \sum_{k=1}^n \frac{1}{1+\frac{k^\alpha}{n}} \le \lim_{n\to\infty} \frac{1}{n}\sum_{k=1}^n \frac{1}{1+\frac{1}{n}} = \lim_{n\to\infty} \frac{1}{1+1/n} = 1
  $$
  
</details>  
<br />
