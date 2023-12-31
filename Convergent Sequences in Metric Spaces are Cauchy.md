---
tag: topology
mathLink: convergent sequences in metric spaces are cauchy
---
>[!prop] 
>Let $(X, d)$ be a [[Metric Space]], let $\{x_{n}\}$ be a [[Sequence]] in $X$. Then if $x_{n}$ [[Converges (Sequence)]]s, then $x_{n}$ is [[Cauchy Sequence]]. 

>[!proof]
>Let $\epsilon>0$ be given. Let $x_{n}\rightarrow x\in X$. Pick $N\in \mathbb{N}$ such that 
>$$\forall n\ge N: d(x,x_{n})<\frac{\epsilon}{2}$$
>Then, if $n,m\ge N$, 
>$$d(x_{n},x_{m})\le d(x_{n},x)+d(x_{m},x)$$
>by the [[Triangle Inequality]]. As $n,m\ge N$,
>$$d(x_{n},x)+d(x,x_{m})<\frac{\epsilon}{2}+\frac{\epsilon}{2}=\epsilon$$
>So, $x_{n}$ is [[Cauchy Sequence]]. 

