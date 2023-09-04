---
tag: topology
mathLink: subsequences of convergent sequences converge
---
>[!prop]
>Let $(X, d)$ be a [[Metric Space]]. If $x_{n}$ [[notation for converges]] $x\in X$ and $\{x_{n_{k}}\}$ is a [[Subsequence]], then $x_{n_{k}} \rightarrow x$. 

>[!prop] Lemma
>If $\{x_{n}\}$ is a [[Sequence]] and $\{x_{n_{k}}\}$ is a [[Subsequence]] of $x_n$, then $$n_{k}≥k$$

>[!proof] Prove Lemma
>Base case: $k=0$
>$n_0≥0$ as $n_{0}\in \mathbb{N}$
>Inductive step: 
>Suppose $n_{k}≥k$ for some $k≥0$. Then, $n_{k+1}≥n_{k}+1≥k+1$
>So, by the [[Principle of Mathematical Induction]], $n_{k}≥k$ for all $k\in \mathbb{N}$.

>[!proof]
>Let $\epsilon>0$ be given. Pick $N\in \mathbb{N}$ such that if $n≥N$, 
>$$d(x,x_{n})<\epsilon$$
>Then, if $k≥N$, $n_{k}≥k≥N$, 
>$$d(x,x_{n_{k}})<\epsilon$$
>so $x_{n_{k}}\rightarrow x$.
