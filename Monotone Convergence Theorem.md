---
tag: analysis
mathLink: (MC)
---
>[!thm]
Let $\{x_{n}\}$ be a [[Bounded Metric Space]] [[Sequence]] of real numbers. 
>1. If for all $n$, $x_{n}≥x_{n+1}$, then $\lim x_{n}=\inf\{x_{n}\}$
>2. If for all $n$, $x_{n}≤x_{n+1}$, then $\lim x_{n}=\sup\{x_{n}\}$

>[!proof]
(1) As $\{x_{n}\}$ is a [[Bounded Metric Space]] [[Set]] and $x_{1}\in\{x_{n}\}$, $x=\inf\{x_{n}\}\in \mathbb{R}$ as $\mathbb{R}$ is [[Complete]]. Suppose $x_{n}\not\rightarrow x$. Pick $\epsilon>0$ such that for all $N\in \mathbb{N}$, there exists $n≥N$ such that $|x_{n}-x|≥\epsilon$. Then, $x_{n}≥x+\epsilon>x$, so $x$ is not the [[infinum]] of $\{x_{n}\}$ as it is not the greatest lower bound. By contradiction, $x_{n}\rightarrow x$.
