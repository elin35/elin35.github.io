---
title: Proof Dissection 1
date: 2022-10-11
---

This post will describe the process of solving a problem which came up in my reading course. In excruciating detail, we will go through my thought process on how we developed the idea to solve the problem, as well as the many (necessary) blunders we made. We begin with the statement to be proved as well as some basic defintitions.

This problem is taken from the text "Optimal Transport for Applied Mathematicians" by Filippo Santambrogio.

---

>Let $X,Y$ be topological spaces, $\mu$ be a Borel measure on $X$ and $T:X\to Y$ be a measurable map. If $A$ is an atom of $\mu$, then the pushforward measure $T_\sharp\mu$ is also atomic such that there exists an atom $B$ of $T_\sharp\mu$ where $T_\sharp \mu(B) \ge \mu(A)$.

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

---

### 1. Initial Intuition

Starting off, the problem may not seem too bad. Ignoring all details about the space and measure, the most natural guess we immediately came to was that, since $T_\sharp\mu$ was a measure on the output space $Y$, $T$ maps $X\to Y$ and all we're given is that $A$ is an atom of $\mu$, then certainly the only identifiable subset of $Y$ was the image $T(A)$. Surely, this had to be the atom of $T_\sharp\mu$. Let's first show that $T(A)$ has measure at least $\mu(A)$.

$$ T_\sharp\mu(T(A)) = \mu(T^{-1}(T(A))) \ge \mu(A)$$

since $T^{-1}(T(A)) \supseteq A$. So far so good. Already, one of the key issues has already arisen, but let us proceed. We now want to show that $T(A)$ doesn't have a proper subset with smaller measure. Indeed let $B\subset T(A)$. Then 

$$ T_\sharp\mu(B) = \mu(T^{-1}(B)).$$

Where do we go from here? One possibility was to say that $B = T(A')$ for some $A' \subset A$. This isn't necessarily true, but even if it were, the best we can do is

$$ T_\sharp\mu(T(A')) = \mu(T^{-1}(T(A'))) \le \mu(T^{-1}(T(A))) = T_\sharp\mu(T(A))$$

we have no way of showing that $T_\sharp\mu(B) = 0$. This illuminates the first key issue, but already from the very beginning, we stumbled at the second key issue.

### 2. Key Issues

Here are the two major problems which this exercise poses:

1. It is difficult to control the size of $T_\sharp\mu$ because it is defined via the preimage. For example, $T^{-1}(T(A)) \supseteq A$, and we have no idea what the difference between the two sets is.
2. The second, more subtle, issue is that we don't even know if $T(A)$ is a measurable subset of $Y$. So already from the start, we were doomed.

### 3. Crisis

Once the two issues were identified, the problem seemed quite hopeless. After discussion with my advisor and a few classmates, a few options presented themselves:

1. The result is not actually true. There was some initial concern that this was a mistake by the author, especially considering how general the assumptions were on the topological spaces and the map.
2. Try attacking via contrapositive or contradiction
3. Perhaps we should start with some stronger assumptions on $X,Y$ and $T$. 

and here is how each of those suggestions ended up:

1. This was not really an option.
2. There were some good ideas suggested by my peers, but the suggested ideas ran into the key issues above, just from a different perspective.
3. I didn't even attempt this because I don't remember much topology and assuming anything which would help the preimage issue seemed like overkill.

Thus, we fought on.

### 4. First Idea: Forcing Measurability

This first thing we did was come to terms with the fact that $T(A)$ was not exactly the atom. It was simply not feasible to work with as it led to both key issues. Thus, we had to start looking for another measurable set. We still had the conviction that the atom of $T_\sharp\mu$ was going to be a set that was "close" to $T(A)$, so there was a question of whether we could approximate $T(A)$ from above via measurable sets (think outer regularity).  In other words, we wanted to look at a set like

$$ \{ B'\subseteq Y: \text{$B'$ measurable, } T(A) \subseteq B'  \} $$

We certainly had that such a set was nonempty as $Y$ was contained within, and we could easily show that it was closed under countable intersection. We then wanted to employ the following technique:

1. Define $c:= \inf\{T_\sharp\mu(B'):B' \text{ is contained in the set above}\}$
2. Take a sequence $$(B_n)_{n=1}^\infty$$ in the set above such that $$T_\sharp\mu(B_n)\to c$$ as $n\to\infty$.
3. Using closure, define the set $B:= \bigcap_{n=1}^\infty B_n$.

With $B$ measurable and the fact that $T_\sharp\mu(B) = c \ge \mu(A)$, we were now very hopeful that $B$ was the atom of $T_\sharp\mu$. 

Moving ahead with our calculation to prove it was indeed an atom, we considered a strict subset $\tilde B \subset B$, with $T^{-1}(\tilde B) < T^{-1}(B)$, and wanted to analyze $T_\sharp\mu(\tilde B) = \mu(T^{-1}(\tilde B))$. This is where we again ran into our first key issue. If we try to push ahead with this set, we can say that $T(A) \not \subset \tilde B$, otherwise we'd contradict $c$ being the infimum. This led to a lot of trial and error of considering cases of what the set $T^{-1}(\tilde B) \cap A$ looked like (many venn-diagrams were drawn).

Here is what happened. We solved the second key issue on the measurability of the atom candidate. Although $T(A)$ was an unknown quantity, approximating it was the right idea as it gave us a foundation to build upon. It gave us a *little bit of structure*, but it was not enough to overcome the first key issue. This issue was the biggest factor in our problem feeling **structureless**. We still had no way of controlling the pushforward measure as the preimage continued to cause issues of **location**, i.e. how $T^{-1}(\tilde B)$ and $A$ intersect. 

Thus, we had to create structure from what we were given.

### 5. Second Idea: Creating Structure

After pondering venn-diagrams, we recognized that it was not possible to locate the intersection of $T^{-1}(\tilde B)$ and $A$. The reason we were even doing this was because of how we defined our measurable set as being the intersection of sets which contained $T(A)$, but perhaps, just using $T(A)$ wasn't enough to give us a strong enough foundation to work upon. However, what other sets could we consider if the only identifiable sets are $A$ and $T(A)$? This is where a nuance in the definition of atom came to play. Atoms are defined as these minimal positive measure sets, so that any subset which *does not* have the same measure, must have measure zero. The "does not" is important as it means we can have strict subsets which have the same measure as the atom. These equal-measure sets are also atoms on their own, so when we give the existence of an atom $A$, we can think of $A$ as being a representative of an equivalence class of all sets of equal measure. 

Thus, we wanted to now consider the following set 

$$ S = \{A'\subseteq A: A' \text{ measurable, } \mu(A') = \mu(A)\} $$

and repeat our idea in step 4. However, this time we would consider 

$$ \Gamma = \{ B\subseteq Y: B\text{ measurable, } T(A') \subseteq B, A'\in S\} $$
