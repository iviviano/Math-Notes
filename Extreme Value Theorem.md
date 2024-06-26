---
tag: analysis, topology
mathLink: EVT
---
>[!thm]
>Let $X$ be a [[Compactness]] [[Topological Space]]. If $f:X \mapsto \mathbb{R}$ is [[Continuous]], then there exist $a,b\in X$ such that for all $x\in X$, $$f(a)≤f(x)≤f(b)$$

>[!proof]
>By the [[Characterizations of Compactness]], $f(X)$ is [[Closed Set]] and [[Bounded Metric Space]]. Let $\alpha=\sup(f(X)),\beta=\inf(f(X))$. Clearly, $f(\beta)≤f(x)≤f(\alpha)$ for all $x\in X$. Since $f(X)$ is [[Closed Set]], it contains its [[Limit Point]]s ([[Closed Sets in Metric Spaces contain Sequence Limits]]). [[therefore]] there are $a,b\in X$ such that $f(a)=\alpha,f(b)=\beta$.
