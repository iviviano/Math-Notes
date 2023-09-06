---
tag: topology
mathLink: $\epsilon$-chain
---
>[!def]
Let $(X,d)$ be a [[Metric Space]]. If $E\subseteq X, y\in E$, and $\epsilon>0$, we say there is an *$\epsilon$-chain* from $x$ to $y$ in $E$ when there is a finite number of points $x_{1},\ldots,x_{n}$ in $E$ such that:
>1. for $1≤k≤n, B_{d}(x_k,\epsilon)\subseteq E$
>2. for $2≤k≤n, x_{k-1}\in B_{d}(x_{k},\epsilon)$
>3. $x_{1}=x$ and $x_{n}=y$
