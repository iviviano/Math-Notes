---
tag: topology
mathLink: sequential formulation of continuity
---
>[!thm] Theorem (for metric spaces)
>Let $(X,d_{X}),(Y,d_{Y})$ be [[Metric Space]]s. Let $f:X \rightarrow Y$ be a [[Function]]. Then, $f$ is [[Continuity at a Point]] $x\in X$ [[iff]] whenever $\{x_{n}\}$ is a [[Sequence]] in $X$ and $x_{n}\rightarrow x$, $f(x_{n})\rightarrow f(x)$ in $Y$.

>[!proof] (for metric spaces)
Suppose $f$ is [[Continuous]] at $x\in X$ and $\{x_{n}\}$ is a [[Sequence]] in $X$ [[Converges]]ing to $x$. Let $\epsilon>0$ be given. Pick $\delta>0$ such that for $d_{X}(x,y)<\delta$ [[implies]] $d_{Y}(x,y)<\epsilon$ by the [[Ep-de Formulation of Continuity]]. Pick $N\in \mathbb{N}$ such that for all $n≥N$, $x_{n}\in B_{d_{X}}(x,\delta)$. Then, if $n≥N$, 
$$d_{Y}(f(x),f(x_{n}))<\epsilon$$
so $f(x_{n})\rightarrow f(x)$.
>
Suppose the implication holds. Let $x\in X$ and suppose $f$ is not [[Continuity at a Point]] $x$. Pick $\epsilon>0$ such that for all $\delta>0$, there exists $x_{0}\in B_{d_{X}}(x,\delta)$ such that $d_{Y}(f(x),f(x_{0}))≥\epsilon$. Let $\{x_n\}$ be a [[Sequence]] in $X$ converging to $x$. Let $\delta=\frac{1}{n}$. Then, let $x_{n}\in B_{d_{X}}(x,\delta_{n})$ such that $f(x_{n})\notin B_{d_{Y}}(f(x),\epsilon)$. Clearly, $x_{n}\rightarrow x$, but $f(x_{n})$ does not converge to $f(x)$. This is a contradiction proving the reverse implication.
