---
title: Proof Dissection 1
date: 2022-10-11
---

This post will describe the process of solving a problem which came up in my reading course. In excruciating detail, I will go through my thought process on how I developed the idea to solve the problem, as well as the many blunders I made. We begin with the statement to be proved as well as some basic defintitions. 

This problem is taken from the text "Optimal Transport for Applied Mathematicians" by Filippo Santambrogio.

--- 

>Let $X,Y$ be topological spaces, $\mu$ be a Borel measure on $X$, and $T:X\to Y$ be a measurable map. If $A$ is an atom of $\mu$, then the pushforward measure $T_\sharp\mu$ is also atomic such that there exists an atom $B$ of $T_\sharp\mu$ where $T_\sharp \mu(B) \ge \mu(A)$.

<br />
<details markdown="1">
  <summary><strong>Definitions</strong></summary>
<ol>
  <li>
    A measure $\mu$ is atomic if there exists a measurable set $A\subseteq X$ such that $\mu(A)>0$ and for any measurable subset $A'\subset A$ with $\mu(A')<\mu(A)$, it must be that $\mu(A')=0$.
  </li>
  
  <br>
  
  <li>
    If $T:X\to Y$, then the pushforward measure, denoted $T_\sharp\mu$ is a measure on $Y$ defined by 
    $$ 
        T_\sharp\mu(B) = \mu( T^{-1}(B)) \qquad B \subseteq Y, \hspace{2mm} B \text{ measureable.}
    $$
  </li>
  
</ol>
</details>  
<br />

