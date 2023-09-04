---
tag: topology
mathLink: cauchy sequence converges $\implies$ sequence converges
---
>[!prop]
>Let $(X,d)$ be a [[Metric Space]]. Then, if $\{x_{n}\}$ is a [[Cauchy Sequence]] [[Sequence]] in $X$, and some [[Subsequence]] of $\{x_{n}\}$ [[Converges]] to $x\in X$, then $x_{n}\rightarrow x$.

>[!proof]
>Let $\epsilon>0$ be given. Then, pick $N_{1}\in \mathbb{N}$ such that if $k\ge N_{1}$, 
>$$d(x_{n_{k}},x)<\frac{\epsilon}{2}$$
>Pick $N_{2}\in \mathbb{N}$ such that if $m,n\ge N$,
>$$d(x_{n},x_{m})<\frac{\epsilon}{2}$$
>Let $N=\max\{N_{1},N_{2}\}$. Then, if $n\ge N$,
>$$d(x_{n},x)\le d(x_{n},x_{n_{n}})+d(x_{n_{n}},x)<\frac{\epsilon}{2}+\frac{\epsilon}{2}=\epsilon$$
>So, $x_{n}\rightarrow x$.
>
