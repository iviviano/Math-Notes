---
tags:
  - topology
mathLink: subsequence of Cauchy sequence converges $\implies$ sequence converges
---
>[!prop]
Let $(X,d)$ be a [[Metric Space]]. Let $\{x_{n}\}$ be a [[Cauchy Sequence]] [[Sequence]] in $X$ and let $\{x_{n_{k}}\}$ be a [[Converges (Sequence)]]nt [[Subsequence]]. Then, $\{x_{n}\}$ is a [[Converges (Sequence)]]nt [[Sequence]].

>[!proof]
Let $x_{n_{k}}\rightarrow x\in X$. Let $\epsilon>0$ be given. Pick $N_{1}\in \mathbb{N}$ such that if $n,m≥N_1$, $$d(x_{n},x_{m})< \frac{\epsilon}{2}$$Pick $N_{2}\in \mathbb{N}$ such that if $n≥N_2$, $$d(x_{n},x)< \frac{\epsilon}{2}$$Let $N=\max\{N_{1},N_2\}$. Then if $n≥N$, $$d(x_{n},x)≤d(x_{N},x)+d(x_{N},x_{n})≤ \frac{\epsilon}{2}+ \frac{\epsilon}{2}=\epsilon$$