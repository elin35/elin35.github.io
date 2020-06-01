---
title: "$m\\mathbb{Z} + n\\mathbb{Z} = \\text{gcd}(m,n)\\mathbb{Z}$"
date: 2020-06-01
categories:
  - Math
  - Algebra
  - Number Theory
tags:
  - math
  - principal ideals
  - rings
  - number theory
  - algebra
---

This problem is fairly well known, but as a reference please see Keith Conrad's [Introduction](https://kconrad.math.uconn.edu/blurbs/ringtheory/ideals.pdf) for a brief hinting at the topic at hand. 

Prove that $m\mathbb{Z} + n\mathbb{Z} = \text{gcd}(m,n)\mathbb{Z}$ where $m,n\in\mathbb{Z}^+$. Note that $\alpha\mathbb{Z}$ denotes the principal ideal generated from $\alpha$.
{: .notice}

At first glance, beyond the notions and properties surrounding principal ideals, this seems like a direct set equality problem. 


<details markdown="1">
  <summary>Click to Reveal Set Equality Method</summary>
## Proof
  For convenience, we'll denote gcd$$(m,n) \equiv (m,n)$$
    
  $$(\subseteq)$$
        Let $x\in \mathbb{Z} + n\mathbb{Z}$. Then, $x = am + bm$ for $a,b\in\mathbb{Z}$. Since $(m,n) \mid m$ and $(m,n)\mid n$, we have that $m = k(m,n)$ and $n = l(m,n)$ for $k,l\in\mathbb{Z}$. Thus, 
        \\[ x = am+bn = (m,n)(ak+bl)\in (m,n)\mathbb{Z}. \\]

  $$(\supseteq)$$
        Let $x \in (m,n)\mathbb{Z}$. Then $x= k(m,n).$ By [*Bezout's Identity*](https://en.wikipedia.org/wiki/B%C3%A9zout%27s_identity), we know that there exists integers $r,s$ such that $(m,n) = rm+sn$. Thus, 
        \\[x= k(m,n) = k(rm+sn) = (kr)m + (ks)n \in m\mathbb{Z} + n\mathbb{Z}. \hspace{1cm}\blacksquare\\]
</details>


